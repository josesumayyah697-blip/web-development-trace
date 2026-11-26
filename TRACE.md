# The URL


The URL I used is https://www.dorsu.edu.ph. The protocol is https, which means the website uses a secure connection, while the domain name is www.dorsu.edu.ph. The path is / because I am visiting the website's homepage.
www.dorsu.edu.ph


When I type https://www.dorsu.edu.ph into my browser and press Enter, several steps happen before the finished page appears.
1. I enter the URL. The browser reads the address. https tells it to use a secure connection, and www.dorsu.edu.ph is the website's hostname.
2. The browser checks its cache. It may already have information about the website, such as its IP address or some files. If the information is still valid, the browser may reuse it. Otherwise, it needs to look up the address.
3. DNS finds the IP address. DNS (Domain Name System) works like the internet's address book. My computer asks a DNS resolver for the IP address connected to www.dorsu.edu.ph. The resolver may check its cache or ask other DNS servers. The answer can contain an IPv4 address, an IPv6 address, or more than one address.
4. My computer connects to the server. Using the IP address, the browser starts a network connection to the website. Because the URL uses HTTPS, it normally connects using port 443.
5. The browser and website secure the connection. They perform a TLS handshake. The website presents a digital certificate, and the browser checks that it is valid for the website's hostname. They also agree on encryption keys so the information sent between them is protected.
6. The browser requests the page. The browser sends an HTTPS request asking for the webpage. The request includes details such as the page it wants and information about the browser.
7. The server processes the request. The web server receives the request and finds or generates the requested page. It may communicate with an application or database to get the information needed.
8. The server sends the response. The website sends back a response, usually containing HTML and possibly links to other files such as CSS, JavaScript, images, and fonts.
9. The browser downloads the other resources. It reads the HTML and requests the extra files needed to display the page. Some files may come from the browser cache or a content delivery network.
10. The browser builds and displays the page. The browser parses the HTML to create the page structure, uses CSS to apply the design, and runs JavaScript to add interactive behavior. It also loads and places images and other resources. After these steps, I can see and use the finished webpage.


# DNS Lookup


When I enter the domain name, my browser needs to find its IP address. It asks a DNS resolver to translate www.dorsu.edu.ph into an IP address, just like looking up a contact number in a phonebook. The DNS result is the address I found using the nslookup command in A1.
www.dorsu.edu.ph

C:\Users\user>nslookup www.dorsu.edu.ph
Server:  homerouter.cpe
Address:  fe80::d4aa:b0:4932:300b

Non-authoritative answer:
Name:    www.dorsu.edu.ph
Addresses:  2606:4700:3036::6815:1e68
          2606:4700:3036::ac43:acbf
          172.67.172.191
          104.21.30.104


# Connection

After finding the IP address, my browser connects to the website's server using HTTPS, usually through port 443. The "S" in HTTPS stands for Secure, which means the connection uses encryption to protect the information being exchanged between my browser and the website.

# HTTP Request

Once the secure connection is established, my browser sends an HTTP request to the server. It usually uses the GET method to request the homepage, and the requested path is /. This tells the server that I want to view the website's main page.

# HTTP Response

After receiving the request, the server sends an HTTP response back to my browser. The response contains a status code, headers, and HTML content; for example, status code 200 OK means the request was successful. The browser reads the HTML and uses it to display the webpage.


# URL TRACE DIAGRAM

<img width="3264" height="2448" alt="image" src="https://github.com/user-attachments/assets/12be7f57-047d-4371-985e-d97ed86c380d" />


# Questions and Answers

**#1. In your trace, which computer is the client and which is the server?**


The client is my computer, where I use a web browser to access the DOrSU website. The server is the computer that hosts the DOrSU website and sends the requested webpage files to my browser.

**#2. If the DNS lookup fails, what does the user see in the browser?**


If the DNS lookup fails, the browser cannot find the IP address of the website. As a result, the webpage will not load, and the browser may display an error message such as "DNS_PROBE_FINISHED_NXDOMAIN" or "This site can't be reached."

**#3. What is the difference between status codes 200, 301 and 404? Give a real-life situation for each.**


200 OK – This means the request was successful, and the server returned the requested webpage. For example, when I successfully open the DOrSU homepage.

301 Moved Permanently – This means the webpage has permanently moved to another URL. For example, when an old website address automatically redirects visitors to its new address.

404 Not Found – This means the server cannot find the requested webpage. For example, when I enter a website link to a page that has been deleted or does not exist.
