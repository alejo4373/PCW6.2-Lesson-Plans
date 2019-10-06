# Lesson Plan: NPM & Modules

## Exit ticket asks:
* Server definition
* DNS, HTTP, IP, URL definitions
* What happens when server created with `http.createServer()`
  * Clients can be anything that can make a requests a resource.
* `http` sever listening.

## Anticipating Fellow Needs:

1. What will fellows be most likely to struggle with and why? 

<!-- * Jargon. 
  * Package vs Module 
  * Module sources: Core modules vs Local modules vs Third Party modules
* Trying to import a module that is not being exported
* Install a module outside a node project and not having a `package.json`

2. What simpler assignment will you give to a struggling fellow: 
   * Create a local module, make sure to export it and the import it somewhere else 

3. What challenge assignment will you give to a fellow who is following along and ready for the next step: 
  * Explore npmjs.com and find 2 more modules and learn how to use them. Build a CLI app with them
  * Explore the `http` core module and make a network request with it to an API -->

## Lesson Breakdown

### Motivation
  * Interviewing
  * Understanding
  * Sharing information
  * [Question] What are some of the benefits of the mentioned above?

### What is the Internet
  * [Inter] = reciprocal, mutual. [net] = network.
  * 1960s as a US military funded research project 4 universities connected their computers
  * The backbone of the web
  * Global network of inter connected computers which communicate

### Clients & Servers
  * Computers connected to a network become clients and servers
  * They interact trough requests and responses messages
  * Severs are servants who offer resources or services
  * Clients are consumers
  * [QUESTION] A real world example of a client server interaction? How is the communication, what is the medium, who are the actors?
  * [QUESTION] When I make a network request to the pokemon api who is the server and who is the client?

#### How does it happen
  * When you type an address in your browser
  * DNS
  * Browser Send request to server ip
  * If server approves replies with packets
  * Browser assemble packets and displays it

### What is a Server?
  * Computer receives requests and send back responses
  * Server is mostly understood to mean a web server
  * Types:
    * Web Server. Web  pages, content. Examples?
    * Email Server. 
    * FTP Server. Uploading, downloading, from computers server. i.e Dropbox. Another example?.

### What is a Client?
  * A computer or program that requests a resource
  * Anything that can make a request and consume a reponse
  * Types:
    * Web Browser, aka user agent
    * Mobile App makes requests

### IP Addresses & DNS
  * The computers needs to know to what computer to send a request
  * Need of a way to uniquely identify a computer in the network
  * IP address. 4 numbers separated by dots. 0 >= n <= 255
  * Ip addresses are not easy to read and remember by humans
  * We have a computer remember the addresses associated with names

### A server must
  * Always be running on a certain IP address
  * Listen for and recognize upcoming requests arriving at that ip or url
  * Process a request, do some work based on it's content of that request. Endpoint, request payload etc.
  * Send back a response

### Our first server with the `http` Node.js module
  * The http module allow us to make requests and create simle web servers
  * What are we doing here?
    * Declaring a port. 

## Planning Activities:

Describe in detail. What are the instructions you will give? What will be the example you offer? How long will fellows spend on each component? How will you wrap up the activity?
  * Using the `nslookup` command find the IP address of 5 websites of your liking. Copy those ip to your browser address bar and hit enter.
  * Send a network request to `<instructors_lan_ip>:port/<your_name>`
  * Find your friend's ip address by asking them to type `ifconfig | grep inet` it should look somthing like `192.168.1.60` make a network request to `<classmate_ip>:port/<your_name>`

### Activities for this lesson 

* In pairs: Draw “how you would solve this problem” (without telling what a LL looks like/how it works). Conclusion: One person draws their solution for the class
For class: 
3.

### Schedule: 

Time: 07:00 - 08:00 pm
Instructors Are:
Fellows are:
Pass through lesson material while asking them to implement the small examples.
Listening, asking questions

### Possible questions
* [HTTP vs HTTPS](https://www.cloudflare.com/learning/ssl/why-is-http-not-secure/)
* [HTTP vs FTP](https://techdifferences.com/difference-between-http-and-ftp.html)
* How many ports does a computer have?


## Resources
Vox - https://www.youtube.com/watch?v=Ve810FHZ1CQ
Motherboard - https://www.youtube.com/watch?v=iMAThVcqzuk
[ARPANET - The basis for the internet](https://searchnetworking.techtarget.com/definition/ARPANET)
