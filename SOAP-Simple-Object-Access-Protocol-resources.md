SOAP  (formerly an acronym for Simple Object Access Protocol) is a messaging protocol specification for exchanging structured information in the implementation of web services in computer networks. It uses XML Information Set for its message format, and relies on application layer protocols, most often Hypertext Transfer Protocol (HTTP), although some legacy systems communicate over Simple Mail Transfer Protocol (SMTP), for message negotiation and transmission.

SOAP allows developers to invoke processes running on disparate operating systems (such as Windows, macOS, and Linux) to authenticate, authorize, and communicate using Extensible Markup Language (XML). Since Web protocols like HTTP are installed and running on all operating systems, SOAP allows clients to invoke web services and receive responses independent of language and platforms.


SOAP Vs. REST: Difference between Web API Services 
https://www.guru99.com/comparison-between-web-services.html#:~:text=KEY%20DIFFERENCE,stands%20for%20Representational%20State%20Transfer.&text=SOAP%20needs%20more%20bandwidth%20for,%2C%20XML%2C%20HTML%20and%20JSON.


KEY DIFFERENCE
SOAP stands for Simple Object Access Protocol whereas REST stands for Representational State Transfer.
SOAP is a protocol whereas REST is an architectural pattern.
SOAP uses service interfaces to expose its functionality to client applications while REST uses Uniform Service locators to access to the components on the hardware device.
SOAP needs more bandwidth for its usage whereas REST doesn’t need much bandwidth.
Comparing SOAP vs REST API, SOAP only works with XML formats whereas REST work with plain text, XML, HTML and JSON.
SOAP cannot make use of REST whereas REST can make use of SOAP.



Difference Between SOAP and REST
Each technique has its own advantages and disadvantages. Hence, it’s always good to understand in which situations each design should be used. This REST and SOAP API difference tutorial will go into some of the key difference between REST and SOAP API as well as what challenges you might encounter while using them.


SOAP requires more bandwidth for its usage. Since SOAP Messages contain a lot of information inside of it, the amount of data transfer using SOAP is generally a lot.

<?xml version="1.0"?>
<SOAP-ENV:Envelope 
xmlns:SOAP-ENV
="http://www.w3.org/2001/12/soap-envelope" 
SOAP-ENV:encodingStyle
=" http://www.w3.org/2001/12/soap-encoding">
<soap:Body>
 <Demo.guru99WebService
 xmlns="http://tempuri.org/">
   <EmployeeID>int</EmployeeID>
   </Demo.guru99WebService>
 </soap:Body>
</SOAP-ENV:Envelope>


REST does not need much bandwidth when requests are sent to the server. REST messages mostly just consist of JSON messages. Below is an example of a JSON message passed to a web server. You can see that the size of the message is comparatively smaller to SOAP.


{"city":"Mumbai","state":"Maharastra"}