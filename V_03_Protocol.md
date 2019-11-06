## JSON:
###### Pros:
- JavaScript Object Notation lightlightweight data-interchange format. 
- It is easy for humans to read and write. 
- It is easy for machines to parse and generate.  
- JSON is a text format that is completely language independent but uses conventions that are familiar to programmers of the C-family of languages, including C, C++, C#, Java, JavaScript, Perl, Python, and many others. 
- These properties make JSON an ideal data-interchange language.
###### Cons:
Plain text

## Text:
- can easilly be implemented
- no complex data structures possible
- easy human-readable
- more suitable for one to a few parameters
- a letter, character, number, etc. represents 1 byte
- with an internetspeed of 1MByte/s -> 1M characters per second
- Example: sending temperature to display

## YAML
- stands for "YAML Ain't Markup Language"
- used for data serialisation
- easy readability for human
- less verbose than JSON and XML
- uses linebreacks and indention --> tabs are not suported use space
- UTF-8 text format
- YAML is case sensitive
- can be used with most programming languages
- working with:
+ mappings (hashes / dictionaries)
+ sequences (arrays / lists)
+ scalars (strings / numbers)
###### Advantage:
+ no extra delimeter
+ reading is light and simple
+ makes understanding easy
+ can be used for configuration and data transfer
###### Disatvantage:
+ there are so many applications using XML and JSON --> replacing it is hard
+ the indention musst match or the code will stop working
+ there are many ways to represent data in YAML
###### Example:
+ it is used for the [MQTT](#https://www.home-assistant.io/integrations/mqtt/) configuration

### Binary 
###### Advantages: 
- Simple structure, simple to write and convert
###### Disadvantages: 
IT’s not human readable, more Memory
Example: monitoring GPS data in high rate and low latency

## XML:
###### Usage:
- XML is used in many aspects of web development.
- XML is often used to separate data from presentation.
- In many HTML applications, XML is used to store or transport data, while HTML is used to format and display the same data.
###### Pros:
- XML is platform independent and programming language independent, thus it can be used on any system and supports the technology change when that happens.
- The data stored and transported using XML can be changed at any point of time without affecting the data presentation.
- XML allows validation using DTD and Schema. This validation ensures that the XML document is free from any syntax error.

###### Cons:
- XML syntax is verbose and redundant compared to other text-based data transmission formats such as JSON.
- XML document is less readable compared to other text-based data transmission formats such as JSON.
- XML doesn’t support array.

## CoAP:
Constrained Application Protocol
is a specialized web transfer protocol for use with constrained nodes and constrained networks in the Internet of Things
- Like HTTP, CoAP is a document transfer protocol. Unlike HTTP, CoAP is designed for the needs of constrained devices.
- Like HTTP, CoAP is based on the wildly successful REST model: Servers make resources available under a URL, and clients access these resources using methods such as GET, PUT, POST, and DELETE.
- CoAP packets are much smaller than HTTP TCP flows. Bitfields and mappings from strings to integers are used extensively to save space. Packets are simple to generate and can be parsed in place without consuming extra RAM in constrained devices.
- CoAP runs over UDP, not TCP. Clients and servers communicate through connectionless datagrams. Retries and reordering are implemented in the application stack. Removing the need for TCP may allow full IP networking in small microcontrollers. CoAP allows UDP broadcast and multicast to be used for addressing.

* “The Constrained Application Protocol (CoAP) is a specialized web transfer protocol for use with constrained nodes and constrained networks in the Internet of Things. The protocol is designed for machine-to-machine (M2M) applications such as smart energy and building automation.”

* REST model for small devices
* Like HTTP, CoAP is based on the wildly successful REST model: Servers make resources available under a URL, and clients access these resources using methods such as GET, PUT, POST, and DELETE.

. CoAP has been designed to work on microcontrollers with as low as 10 KiB of RAM and 100 KiB of code space

###### Advantages:
*It is simple protocol and uses less overhead due to operation over UDP. 
*It allows short wake up times and long sleepy states. This helps in achieving long battery life.
*It uses IPSEC or DTLS to provide secure communication.
*It has lower latency compare to HTTP.
*It consumes less power than HTTP.
*It uses ACK message and hence it becomes reliable like HTTP. Moreover it avoids unnecessary retransmissions.


###### Disadvantages:
*CoAP is unreliable protocol due to use of UDP. Hence CoAP messages reach unordered or will get lost when they arrive at destination. To make CoAP as reliable protocol, stop and wait with exponential backoff retransmission feature is incorporated in it. Duplicate detection is also introduced.
*It acknowledges each receipt of the message and hence increases processing time. Moreover it does not verify whether the received message has been decoded properly or not.
*It is unencrypted protocol like MQTT and uses DTLS to provide security at the cost of implementation overhead.
CoAP has communication issues for devices behind NAT (Network Address Translation).


* Example
* Constrained devices - Implementations for constrained devices are typically written in Cs.
* Server-side -> Java -> One significant Java-based implementation of CoAP is Californium.
* Browser-based -> Copper is an extension for Firefox to enable direct access to CoAP resources from a browser.
* Smartphones -> Some implementations are specifically targeting mobile devices such as smartphones and tablets.
* Ikea

## MQTT
- MQTT is a publish/subscribe messaging protocol designed for lightweight M2M communications.
- MQTT clients can register a custom “last will and testament” message to be sent by the broker if they disconnect. 
- These messages can be used to signal to subscribers when a device disconnects.
- MQTT brokers may require username and password authentication from clients to connect. 
- To ensure privacy, the TCP connection may be encrypted with SSL/TLS

## OSC (Open Sound Control)
OSC is used for multimedia devices for purposes such as musical performance.
###### Supports:
- XML 
- WDDX
- JSON
Is used as an aletnative to the midi standard.
Using UDP/IP but can also use an serial bus (USB).
Use Cases: 
- web player
- iot music player
- music boxes
###### Software:
- Nuendo
- Reaktor
- Veejay
- and many more
###### Features:
- Open-ended, dynamic, URL-style symbolic naming scheme
- Symbolic and high-resolution numeric argument data
- Pattern matching language to specify multiple recipients of a single message
- High resolution time tags
- "Bundles" of messages whose effects must occur simultaneously
- Query system to dynamically find out the capabilities of an OSC server and get documentation

## HTTP Post
The Hypertext Transfer Protocol (HTTP) is designed to enable communications between clients and servers.

HTTP works as a request-response protocol between a client and server.

A web browser may be the client, and an application on a computer that 
hosts a web site may be the server.

POST is used to send data to a server to create/update a resource.
POST is one of the most common HTTP methods.

Some other notes on POST requests:
- POST requests are never cached
- POST requests do not remain in the browser history
- POST requests cannot be bookmarked
- POST requests have no restrictions on data length
