---
lastSync: Tue Feb 24 2026 14:44:23 GMT+0300 (Moscow Standard Time)
---
# What is the Simple Mail Transfer Protocol (SMTP)?

The Simple Mail Transfer Protocol (SMTP) is a technical standard for transmitting electronic mail (email) over a network. Like other networking protocols, SMTP allows computers and servers to exchange data regardless of their underlying hardware or software. Just as the use of a standardized form of addressing an envelope allows the postal service to operate, SMTP standardizes the way email travels from sender to recipient, making widespread email delivery possible.

SMTP is a mail delivery protocol, not a mail retrieval protocol. A postal service delivers mail to a mailbox, but the recipient still has to retrieve the mail from the mailbox. Similarly, SMTP delivers an email to an email provider's mail server, but separate protocols are used to retrieve that email from the mail server so the recipient can read it.

# How does SMTP work?

All networking protocols follow a predefined process for exchanging data. SMTP defines a process for exchanging data between an email client and a mail server. An email client is what a user interacts with: the computer or web application where they access and send emails. A mail server is a specialized computer for sending, receiving, and forwarding emails; users do not interact directly with mail servers.

Here is a summary of what passes between the email client and the mail server for an email to begin sending:

- **SMTP connection opened:** Since SMTP uses the Transmission Control Protocol (TCP) as its transport protocol, this first step begins with a TCP connection between client and server. Next, the email client begins the email sending process with a specialized "Hello" command (HELO or EHLO, described below).
- **Email data transferred:** The client sends the server a series of commands accompanied with the actual content of the email: the email header (including its destination and subject line), the email body, and any additional components.
- **Mail Transfer Agent (MTA):** The server runs a program called a Mail Transfer Agent (MTA). The MTA checks the domain of the recipient's email address, and if it differs from the sender's, it queries the Domain Name System (DNS) to find the recipient's IP address.
- **Connection closed:** The client alerts the server when transmission of data is complete, and the server closes the connection. At this point the server will not receive additional email data from the client unless the client opens a new SMTP connection.

Usually, this first email server is not the actual email's final destination. The server, having received the email from the client, repeats this SMTP connection process with another mail server. That second server does the same, until finally the email reaches the recipient's inbox on a mail server controlled by the recipient's email provider.

Compare this process to the way a piece of mail travels from sender to recipient. A mail carrier does not take a letter directly from the sender to its recipient. Instead, the mail carrier brings the letter back to their post office. The post office ships the letter to another post office in another town, then another, and so on until the letter reaches the recipient. Similarly, emails go from server to server via SMTP until they arrive at the recipient's inbox.

# What are SMTP commands?

SMTP commands are predefined text-based instructions that tell a client or server what to do and how to handle any accompanying data. Think of them as buttons the client can press to get the server to accept data correctly.

- `HELO/EHLO`: These commands say "Hello" and start off the SMTP connection between client and server. "`HELO`" is the basic version of this command; "`EHLO`" is for a specialized type of SMTP.
- `MAIL FROM`: This tells the server who is sending the email. If Alice were trying to email her friend Bob, a client might send "MAIL FROM: alice@example.com.
- `RCPT TO`: This command is for listing the email's recipients. A client can send this command multiple times if there are multiple recipients. In the example above, Alice's email client would send "RCPT TO: bob@example.com.
- `DATA`: This precedes the content of the email.
-  RSET: This command resets the connection, removing all previously transferred information without closing the SMTP connection. `RSET` is used if the client sent incorrect information.
- `QUIT`: This ends the connection.


# What is an SMTP server?

An SMTP server is a mail server that can send and receive emails using the SMTP protocol. Email clients connect directly with the email provider's SMTP server to begin sending an email. Several different software programs run on an SMTP server:

- **Mail submission agent (MSA):** The MSA receives emails from the email client.
- **Mail transfer agent (MTA):** The MTA transfers emails to the next server in the delivery chain. As described above, it may query the DNS to find the recipient domain's [mail exchange (MX) DNS record](https://www.cloudflare.com/learning/dns/dns-records/dns-mx-record/) if necessary.
- **Mail delivery agent (MDA):** The MDA receives emails from MTAs and stores them in the recipient's email inbox.


# SMTP vs. IMAP and POP

The Internet Message Access Protocol (IMAP) and Post Office Protocol (POP) are used to deliver the email to its final destination. The email client has to retrieve email from the final mail server in the chain in order to display the email to the user. The client uses IMAP or POP instead of SMTP for this purpose.

To understand the difference between SMTP and IMAP/POP, consider the difference between a plank of wood and a rope. A length of wood can be used to push something forward, but not pull it in. A rope can pull an item, but cannot push it. Similarly, SMTP "pushes" email to a mail server, but IMAP and POP "pull" it the rest of the way to the user's application.

# What is Extended SMTP (ESMTP)?

Extended Simple Mail Transfer Protocol (ESMTP) is a version of the protocol that expands upon its original capabilities, enabling the sending of email attachments, the use of TLS, and other capabilities. Almost all email clients and email services use ESMTP, not basic SMTP.

ESMTP has some additional commands, including "`EHLO`", an "extended hello" message that enables the use of ESMTP at the start of the connection.

# Source: 
https://www.cloudflare.com/learning/email-security/what-is-smtp/