# PUBSUB

Publish–subscribe pattern
From Wikipedia, the free encyclopedia
Jump to navigationJump to search
For the Macintosh feature introduced with System 7, see Publish and Subscribe (Mac OS). For the practice of paying before a work is complete, see Subscription business model.
"PubSub" redirects here. For the defunct search website, see PubSub (website).
"Pub sub" redirects here. For the sandwich sold at Publix, see Publix § Stores.

This article needs additional citations for verification. Please help improve this article by adding citations to reliable sources. Unsourced material may be challenged and removed.
Find sources: "Publish–subscribe pattern" – news · newspapers · books · scholar · JSTOR (March 2010) (Learn how and when to remove this template message)
In software architecture, publish–subscribe is a messaging pattern where senders of messages, called publishers, do not program the messages to be sent directly to specific receivers, called subscribers, but instead categorize published messages into classes without knowledge of which subscribers, if any, there may be. Similarly, subscribers express interest in one or more classes and only receive messages that are of interest, without knowledge of which publishers, if any, there are.

Publish–subscribe is a sibling of the message queue paradigm, and is typically one part of a larger message-oriented middleware system. Most messaging systems support both the pub/sub and message queue models in their API; e.g., Java Message Service (JMS).

This pattern provides greater network scalability and a more dynamic network topology, with a resulting decreased flexibility to modify the publisher and the structure of the published data.


 

JavaScript implementation of the Publish/Subscribe pattern with TypeScript support.

[](#install)Install
===================

### [](#npm)npm

$ npm install awesome-pubsub-js

### [](#yarn)yarn

$ yarn add awesome-pubsub-js

[](#a-quick-example)A quick example
===================================

Do you want to know more? Go to the [Documentation](#API) section

##### [](#javascript)JavaScript:

import PubSub from "awesome-pubsub-js";

const pubSub \= PubSub();

pubSub.subscribe("event.example", (data) \=> {
    // data = { name: "John", email: "john@gmail.com" }
    // ... your logic
});

pubSub.publish("event.example", { name: "John", email: "john@gmail.com" });

### [](#api)API

**List of all available methods:**

Each of the following methods takes one or two arguments

*   Subscribe

Method name

Payload

Return value

subscribe

`pubSub.subscribe("eventName", (data) => {});`

HashKey (string) - is needed for use in the 'unsubscribe' method

unsubscribe

`pubSub.unsubscribe('hashKey')`  
hashKey (string) is always returned from the subscribe method

true - when the event has been successfully unsubscribed  
false - when the event does not exists

publish

`pubSub.publish('eventName', any)`  
any = literally anything you want to pass :)  
If you don't pass anything, the default value will be undefined

true - when the event has published successfully  
false - when the event has not been published (e.g. due to the lack of a registered subscriber)

getAllSubscribers

\-

returns the current subscription list

### [](#roadmap)Roadmap:

*    subscribe and publish method
*    unsubscribe method
*    getAllSubscribers method
*    Wildcard support
*    Logger