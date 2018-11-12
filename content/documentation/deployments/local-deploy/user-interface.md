---
title: The User Interface
description: Interacting with our microservices using a visual interface.
weight: 50
---

## The Dashboard

{{% notice warning %}} Service here should not be confused with our type of "*service*" our *authentication* is, though it does share similar intents. 
{{% /notice %}}

Now this example is an [Angular6](https://angular.io) application, and in my opinion the most complicated piece of the puzzle. Going over the *Angluar* framework is out of scope for this guide but it will demonstrate a call made to an *RPC* we set up in the last chapter. A simpler example of building *clients* can be found in **AURA's** [examples](https://github.com/CodeForPortland/ctl-aura/tree/master/examples) directory.
The *Angular service* is using an [Autobahn-Browser](https://github.com/crossbario/autobahn-js-browser) library which is maintained by [Crossbar.io](https://crossbar.io) an excellent resource for finding a library that connects to a *WAMPv2* router in your preferred language. 

## Building the client

In the file [autobahn-routing.service.ts](https://github.com/CodeForPortland/a2j-front-end_dashboard/blob/master/src/a2j/services/autobahn-routing.service.ts) we can see a very similar pattern that we just used for building our *RPC's* client...

```typescript
public getSession(opts: Autobahn.IConnectionOptions): Observable<Autobahn.Session> {
    return Observable.create((obs: Observer<Autobahn.Session>) => {
      const connection = new autobahn.Connection(opts);
      connection.onopen = function(session: Autobahn.Session){
        obs.next(session);
      };
      connection.open();
    });
}
```

Here we are creating a connection object, which is the *client* and when we open it, the router returns a *session object* which we will use to make a **call** to our *RPC* which we can see in the [login.component.ts](https://github.com/CodeForPortland/a2j-front-end_dashboard/blob/master/src/a2j/login-component/login.component.ts) file.

```typescript
this.aura.call('ctl.authentication', null, {username: this.formValues.username, password: this.formValues.password})
      .subscribe(loginResponse => {
        console.log('Auth responded\n', loginResponse);
        if (loginResponse.kwargs && loginResponse.kwargs.jwt) {
          const jwt = loginResponse.kwargs.jwt;
          sessionStorage.setItem('JWT', jwt);
        }

      })
      .unsubscribe();
```

Notice, our `aura.call()` method takes a string argument, `ctl.authentication`. This is our *procedure name* and the `{username: this.formValues.username, password: this.formValues.password}` is the payload we are sending to the *authentication service*.

## Launch the Dashboard!

Now open yet again another command prompt and step into the *a2j-front-end_dashboard* project directory, from there run the following command, `npm start` or if you have the **angular-cli**, `ng serve`.

When the application is initialized, you will want to navigate to [localhost:4200](http://localhost:4200) and pop open your developer console so we can see the browsers output. 

Now navigate to the Login and put in an arbitrary string for the *username* and the *password*.

Before you hit submit navigate in your developers console, to the *Networks* tab and select the **ws** filter.

Now hit submit. 

You should see something like the following screen cap, I'm using *Chrome* but the views should be similar in each major browser. 

![Network Screen Capture](/access2justicePDX/documentation/deployments/local-deploy/user-interface/network-screen-cap.png)

The `127.0.0.1` is our *Angular Service* connecting to *the Router* if you select it, it should now show a screen similar to this...

![Frame Screen Capture](/access2justicePDX/documentation/deployments/local-deploy/user-interface/frame-screen-cap.png)

Two things to note here, look at frames with the green arrows pointing up, the first one shows our realm we are connecting to, and the second has the *RPC procedure name* with our payload and bunch of other nifty meta data we can take advantage of to customize the behavior and state of our application.

{{% notice info %}}Websockets use frames, they are like packets but they allow for multiplexing and bi-directional communication. You can check out more on it in the [HTTP2 spec](https://httpwg.org/specs/rfc7540.html#FramingLayer) or in this [deep dive](https://blog.sessionstack.com/how-javascript-works-deep-dive-into-websockets-and-http-2-with-sse-how-to-pick-the-right-path-584e6b8e3bf7). 
{{% /notice %}}

Ok, now let's checkout our *JWT*, pop open the console for the browser. You should now be able to view the response to the procedure call and it should look something similar to this.

![Frame Screen Capture](/access2justicePDX/documentation/deployments/local-deploy/user-interface/jwt-screen-cap.png)

## Viola!

Congrats! You just made a call to a function in a microservice using a WAMPv2 router from an Angular Service. 


## Recap

You just learned how to set up a router using **Nexus** implemented in the **AURA** project. You also learned how to create a connection *client* and an *RPC* with Go how to register the *RPC* with *the router*. You then learned how to create a connect to the router with an *Angular service* using the *Autobahn-browser* library and then made a call to the *RPC* using an interface. You saw that this used a *procedure name* related to the *RPC* we registered and a payload of *credentials* was sent to receive a *JWT* in a response.

I hope this helps you in building the components you want to make, please feel free to make this guide better or leave comments below. I'm always happy to share what I've learned and I always learn more from everyone I share with. 

    And always..
    
# DFTBA! 

    -Rex