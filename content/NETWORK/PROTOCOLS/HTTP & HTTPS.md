---
lastSync: Fri Mar 13 2026 09:15:40 GMT+0300 (Moscow Standard Time)
---
HTTPS stands for HyperText Transfer Protocol Secure. It is the most common protocol for sending data between a web browser and a website. HTTPS is the secure variant of HTTP and is used to communicate between the user's browser and the website, ensuring that data transfer is encrypted for added security.

# Working of HTTPS

HTTPS establishes the communication between the browser and the web server. It uses the Secure Socket Layer (SSL) and Transport Layer Security (TLS) protocol for establishing communication. The new version of SSL is TLS(Transport Layer Security).

![[Working of HTTPS.png]]
- HTTPS uses the conventional HTTP protocol and adds a layer of SSL/TLS over it.
- The workflow of HTTP and HTTPS remains the same, the browsers and servers still communicate with each other using the HTTP protocol.
- However, this is done over a secure SSL connection. The SSL connection is responsible for the encryption and decryption of the data that is being exchanged to ensure data safety.


# Why HTTPS Matters and What Happens Without It?

- HTTPS is important because it keeps the information on websites safe from being easily viewed or stolen by anyone who might be spying on the network.
- When a website uses regular HTTP, data is sent in small chunks called packets that can easily be intercepted using free software.
- This makes communication, especially over public Wi-Fi, very vulnerable to attacks.
- On the other hand, HTTPS encrypts the data, so even if someone manages to intercept the packets, they will appear as random, unreadable characters.



# HTTP vs HTTPS

| HTTP                                        | HTTPS                                                                        |
| ------------------------------------------- | ---------------------------------------------------------------------------- |
| HTTP stands for HyperText Transfer Protocol | HTTPS stands for HyperText Transfer Protocol Secure                          |
| URL begins with "http://"                   | URL starts with "https://"                                                   |
| HTTP Works at the Application Layer         | Also works at the Application Layer (HTTP over TLS)                          |
| Data is sent in plain text                  | Data is encrypted using TLS                                                  |
| No encryption or security                   | Provides encryption, authentication, and integrity                           |
| Faster in theory (no encryption)            | Nearly same speed in modern systems (TLS optimized, HTTP/2 & HTTP/3 support) |


# Source: 
https://www.geeksforgeeks.org/html/explain-working-of-https/