---
lastSync: Fri Mar 13 2026 09:33:45 GMT+0300 (Moscow Standard Time)
---
Domain Name System (DNS) is an important part of how the internet function. It translates human-readable domain names into machine-readable IP addresses (like 192.0.2.1) that computers use to communicate with each other.



1. **User Request**

When we type a domain name into our browser, our computer starts the process of finding the corresponding IP address needed to connect to the website.

2. **Check Local Cache**

The first place our system looks is in its local cache, which may include:

- ****Browser Cache:**** The browser might have recently stored the IP address if we’ve visited the site before.
- ****Operating System (OS) Cache:**** The OS maintains a DNS cache to speed up lookups.
- ****Router Cache:**** Our router might also store previously requested IP addresses.

If the IP address is found in any of these caches, the process ends here and the browser connects to the website. Otherwise, the process moves forward.

3. **Check Host Files**

If the IP address is not in the local cache, the system may check host files, which are manually configured mappings of domain names to IP addresses. This is rare in modern systems, but it might still be used for certain network configurations.

4. **Query DNS Resolver**

If no IP address is found locally, the request is sent to a DNS Resolver. The Resolver is a server provided by our Internet Service Provider (ISP) or a public DNS service like Google DNS (8.8.8.8) or Cloudflare (1.1.1.1). The Resolver acts as the intermediary that communicates with various DNS servers to find the IP address.

5. **Contact the Root Server**

Resolver first contacts the Root DNS Server which is the starting point for DNS lookups. The Root server doesn’t know the exact IP address but directs the query to the Top-Level Domain (TLD) Server responsible for .org.

6. **Query TLD Server**

Resolver sends the query to the TLD Server for .org domains. The TLD server handles domain names ending in .org and knows where to find the authoritative nameserver.

7. **Query the Authoritative Server**

The Resolver then queries the authoritative nameserver. This server is responsible for storing DNS records for the domain, including the mapping of the domain name to its IP address.

8. **Retrieve the IP Address**

Authoritative nameserver responds to the Resolver with the exact IP address (e.g., 192.0.2.1)

9. **Return IP Address to Computer**

Resolver receives the IP address from the authoritative nameserver and sends it back to our computer. At this point, our computer knows how to connect to the website.

10. **Connect to the Real Server**

With the IP address in hand, our browser sends a request to the real server. This server processes the request and sends the necessary data back to our browser.

11. **Website Loads**

Our browser receives the response from the real server and the website content is displayed on our screen. All of this happens in just milliseconds, making the process seamless for the user.


****What are the 3 zones of DNS?****

> The three DNS zones are:
> 
> 1. ****Zone Authority**** : The authoritative server for a domain.
> 2. ****Reverse Lookup Zone:**** Resolves IP addresses back to domain names.
> 3. ****Forward Lookup Zone**** : Resolves domain names to IP addresses.



Source: 
https://www.geeksforgeeks.org/computer-networks/working-of-domain-name-system-dns-server/