---
name: Tamanna Tasnim
course: cis106
semeseter: fall 2022
---

# Deliverable 1
> Tutorial can be found [here](https://www.digitalocean.com/community/tutorials/how-to-install-the-apache-web-server-on-ubuntu-22-04)

## Concepts I don't understand:

* Apache: Apache is the most widely used webserver software and runs on 67% of all websites in the world. Developed and maintained by Apache Software Foundation, Apache is open source software and available for free.
* Systemctl: The systemctl command is a utility which is responsible for examining and controlling the systemd system and service manager.
* Firewall: A Linux firewall is defined as a solution or service that regulates, protects, and blocks network traffic as it passes to and from a Linux-based environment. 
* Encapsulate: In object-oriented computer programming (OOP) languages, the notion of encapsulation (or OOP Encapsulation) refers to the bundling of data, along with the methods that operate on that data, into a single unit.
* Server Admin: A server administrator configures and maintains servers and makes sure IT infrastructure runs smoothly in the following ways: Creates new user accounts, recovers lost passwords and keeps data secure. Develops and implements network maintenance standard operating procedures. 
* Server Alias:  Alternate names for a host used when matching requests to name-virtual hosts. Most people simply use ServerName to set the 'main' address of the website (eg. 'mywebsite.com') and ServerAlias to add additional addresses the website will be bound to (eg. 'www.mywebsite.com').

##  What is a web server? Hardware and software side
A web server is basically a computer that hosts a website on the Internet.
The term web server can refer to hardware or software, or both of them working together.

On the hardware side, a web server is a computer that stores web server software and a website's component files (for example, HTML documents, images, CSS stylesheets, and JavaScript files). A web server connects to the Internet and supports physical data interchange with other devices connected to the web.

On the software side, a web server includes several parts that control how web users access hosted files. At a minimum, this is an HTTP server. An HTTP server is software that understands URLs (web addresses) and HTTP (the protocol your browser uses to view webpages). An HTTP server can be accessed through the domain names of the websites it stores, and it delivers the content of these hosted websites to the end user's device.

 ##  What are some different web server applications?
Some different web server applications are,

## Apache
It’s almost synonymous to the World Wide Web, and still powers the majority of websites in the world.The reason for Apache’s dominance is threefold: an open license, early entry (this thing was released way back in 1995!), and easy deployment of PHP. The last point was made possible through the mod_php module, which meant that installing Apache was all you needed to do for developing with PHP. Apache is great because it is available on all platforms – Linux, Windows, MacOS, and other platforms,
it’s the default server for all CPanel shared hosting, making it effortless to set up and change sites, it supports for HTTP/2, compression, static files, and load balancing, MPM and FastCGI modes for delivering high concurrency, easy scripting through Lua.

## Nginx
It was released as a project in 2002 by a Russian engineer who got fed up with the then-present solutions’ inability to beat the CK10 problem (basically, handling thousands of concurrent connections).Nginx offered some stunning improvements that helped it win asynchronous architecture for handling high loads, Best-in-the-class static file handling, load balancing, and reverse proxy capabilities,FastCGI caching, Support for uwsgi, SCGI, and other server protocols, with caching,Gzipping, image transformation, byte ranges, chunked responses, etc., with FLV and MKV streaming.WebSockets, keepalive and pipelined connections, access control, error redirection, etc.

## Caddy
One of the hottest new frameworks making splashes in the open-source community recent is Caddy. Caddy is an Nginx-like web server (similar syntax and all) but everything is simplified to a pleasant extreme. For instance, Let’s Encrypt integration for SSL can be done in a mere three lines of config.Caddy is drawing a ton of attention because it is HTTPS enabled by default, you don’t need to do anything for installing or renewing SSL certificates. HTTP/2 gets primary focus.
Rotates TLS session ticket keys by default. This makes for a much more secure TLS connection management that is not vulnerable to the likes of Heartbleed.No dependencies (it’s a Golang-compiled binary codebase that doesn’t depend on any underlying system libraries). Also it serves static files in the current directory by default!

## Lighthttpd
The one area where most modern web servers fail is resource usage. Lighthttpd was designed to overcome these challenges in low-memory and low-CPU environments.Lighthttpd is built on the asynchronous request handling model, and so essentially mirrors how Nginx works. But there’s one catch — Lighthttpd works in a single thread, so if you have a more capable machine, it’s going to ignore other CPU cores. 
  
## MonkeyServer
Despite the odd name, the Monkey web server is an interesting project that continues to be actively developed and supported.The main attraction of the MonkeyServer is the support for embedded platforms. You’d need to compile the server yourself, but you can squeeze out all the frills and end up with a lightweight, fast web server that targets Linux mainly, but is supported on MacOS as well, has full support for ARM-based processors, works perfectly on Android, Raspberry Pi, and other embedded platforms,minimal runtime (100 KB without plugins), supports IPv6 and TLS, works with CGI and FastCGI, has basic authentication, security rules, etc.
  
## OpenLiteSpeed 
OpenLiteSpeed is the open source flavor of the enterprise web server offered by LiteSpeed Technologies.There are many reasons to like OpenLiteSpeed, like it is compatible with Apache’s mod_rewrite, which means if you have a ton of existing Apache files, migrating will be minimal pain, event-driven architecture in the vein of Nginx, resulting in high throughput,GUI-based admin interface, offering a pleasant configuration experience, native SAPI for PHP, resulting in higher performance.

## Cherokee
The Cherokee project was a personal itch of a developer, which has grown into a decent web server platform. While it doesn’t have cutting-edge features like Nginx’s, it does provide an easy, fun and performant alternative to the mainstream web servers.The biggest win for Cherokee is simplicity — there’s no need to break a sweat with the command line for configuring the server. A friendly web-based interface comes packaged and is a delight to use for those who prefer the point-and-click method of getting things done.

##  What is virtualization?
Virtualization is the process of running a virtual instance of a computer system in a layer abstracted from the actual hardware. Most commonly, it refers to running multiple operating systems on a computer system simultaneously. To the applications running on top of the virtualized machine, it can appear as if they are on their own dedicated machine, where the operating system, libraries, and other programs are unique to the guest virtualized system and unconnected to the host operating system which sits below it.

##  What is virtualbox?
VirtualBox is software that is provided by Oracle to install virtual machines onto your system. It was introduced in the year 2007 by Innotek Gmbh and later was developed by Oracle. It is also called a software virtualization package that is capable to load multiple operating systems.

 ##  What is a virtual machine?
A virtual machine (VM) is a digital version of a physical computer. Virtual machine software can run programs and operating systems, store data, connect to networks, and do other computing functions, and requires maintenance such as updates and system monitoring.

 ##  What is Ubuntu Server?
Ubuntu Server is a part of the larger set of Ubuntu products and operating system developed by Canonical Ltd. Ubuntu server is a specific addition that differs a little bit from Ubuntu desktop, in order to facilitate installation on servers.

 ##  What is a firewall?
A firewall is a network security device that monitors traffic to or from your network. It allows or blocks traffic based on a defined set of security rules.

 ##  What is SSH?
 SSH, also known as Secure Shell or Secure Socket Shell, is a network protocol that gives users, particularly system administrators, a secure way to access a computer over an unsecured network. SSH also refers to the suite of utilities that implement the SSH protocol. Secure Shell provides strong password authentication and public key authentication, as well as encrypted data communications between two computers connecting over an open network, such as the internet.SSH refers both to the cryptographic network protocol and to the suite of utilities that implement that protocol. SSH uses the client-server model, connecting a Secure Shell client application, which is the end where the session is displayed, with an SSH server, which is the end where the session runs. SSH implementations often include support for application protocols used for terminal emulation or file transfers. SSH can also be used to create secure tunnels for other application protocols, for example, to securely run X Window System graphical sessions remotely. An SSH server, by default, listens on the standard Transmission Control Protocol (TCP) port 22.
