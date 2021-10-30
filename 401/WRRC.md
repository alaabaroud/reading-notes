# Read: 09 - WRRC and Java


## HTTP Request

**First Step : Local Processing**

- Your browser extracts the "scheme"/protocol, host , and optional port number, resource path, and query strings that are specified in the form.

- The browser will then look through its own cache of recently requested URLs, the operating system’s cache of recent queries, your router’s cache, and your DNS cache.

**Second Step: Resolve an IP**

- if your browser fires off a DNS request using UDP3, the cache lookup will fail.

- the request will  travel to many network devices.

-the server looks for the address associated with the requested hostname once the request arrives at your configured  serve. 

- once you has the IP needed. It will receive a piece of information as part of the answer that will let it know how long the returned answer can be cached for.

**Third Step:  Establish a TCP Connection**

- delivery and ordered data transmission. using a sequence number for every byte sent.

- TCP connections are opened using what’s known as a three-way handshake.

- concurrent communication along the connection, which is also known as full duplex communication.

**Step 4: Send an HTTP Request**

- Send a request made up of a "request line", request header, and a body. The header of the request is made up of pairs in the form name:value `<CR><LF>`. Two consecutive `<CR><LF>` pairs indicate the end of the header section.

- The request follows a similar routing procedure, with the difference being that using TCPs magic sequence number powers.

- Once the server receives the request, processes it, and finds the resource being requested, it generates an HTTP response.

- Once the response is generated, the server responds to the request. At the TCP layer, the client receives the first data packet, the first byte of which should contain the HTTP response header.

**Step 5: Tearing Down and Cleaning Up**

1. The client sends a FIN packet, to which the server responds, and then generally sends a FIN of its own, which the client responds to. The client then waits for a brief timeout, during which it cannot accept new connections, to prevent delayed packets from previous connections arriving during subsequent activities on the port.

2. At this point, the browser begins processing what it has received. If it is an image, data, or other media file that is being consumed by some application inside the browser, a variety of things can happen.

# Simple HTTP Request

The `HttpUrlConnection` class allows us to perform basic HTTP requests without the use of any additional libraries. All the classes that we need are part of the java.net package.

**disadvantages**:

> - the code can be more cumbersome than other HTTP libraries.
> - does not provide more advanced functionalities.
1. Creating a Request .
2. Adding Request Parameters.
3. Setting Request Headers.
4. Configuring Timeouts.
5. Handling Cookies.
6. Handling Redirects.
7. Reading the Response.
8. Reading the Response on Failed Requests.
9. Building the Full Response.



