Q1. Explain how a website opens on the screen after typing a URL.
When a user types a URL (Uniform Resource Locator) into a web browser like Google Chrome and presses Enter, the browser uses DNS (Domain Name System) to find the IP address of the website. The browser acts as a client and sends a request to the web server using HTTP or HTTPS. The server processes the request and may communicate with a database to retrieve the required information. It then sends a response containing files such as HTML, CSS, JavaScript, and images to the browser. The browser processes these files and displays the webpage on the screen. This process is called the request-response cycle. A static website displays mostly fixed content, while a dynamic website can change its content according to user input or database information.


Q2. Write the meanings of HTTP and HTTPS.
HTTP: Hypertext Transfer Protocol. It is used for communication between a web browser and a web server.

HTTPS: Hypertext Transfer Protocol Secure. It provides a secure connection by encrypting data exchanged between the browser and server.


Q3. Explain the request-response cycle.
The request-response cycle is the process through which a browser communicates with a web server to load a website.
The user enters a URL in the browser.
The browser finds the server's IP address using DNS.
The browser sends an HTTP or HTTPS request to the server.
The server processes the request and may access a database.
The server sends a response containing the requested resources.
The browser processes the response and displays the webpage.


Q4. Write the differences between a static and a dynamic website.
Static Website

Dynamic Website

Displays mostly fixed content.

Content can change according to user input or other conditions.

Usually uses pre-written HTML, CSS, and JavaScript files.

May use server-side programming and databases.

Generally simpler to develop.

May require more complex programming.

Example: A simple portfolio website.

Example: An online shopping website.


Q5. Open Chrome DevTools and inspect requests in the Network tab of any website.
Procedure:

Open Google Chrome.

Visit https://example.com.

Right-click on the webpage and select Inspect.

Click the Network tab in Chrome DevTools.

Reload the webpage by pressing Ctrl + R.

Observe the requests and their status codes, resource types, and loading times.

Click on a request to view its details, including headers.

Take a screenshot of the Network tab and save it as network-tab.png.


Q6. Conclusion
A website opens when a browser sends a request to a server and receives a response. HTTP and HTTPS enable communication between the browser and server, while databases provide information when required. Static and dynamic websites differ in how their content is delivered and updated. Chrome DevTools helps us inspect network requests and understand how websites work.