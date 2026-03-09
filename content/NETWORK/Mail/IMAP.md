---
lastSync: Fri Feb 27 2026 11:32:00 GMT+0300 (Moscow Standard Time)
---

![](https://github.com/IserviceBY/KnowledgeBase/blob/v4/Images/Mail%20route.png?raw=true)

# What is IMAP?

An application layer protocol called Internet Message Access Protocol (IMAP) functions as a contract to receive emails from the mail server. IMAP, which is currently on version IMAP4, was created by Mark Crispin in 1986 as a remote access mailbox protocol. It is the protocol that is most frequently used to retrieve emails. Interim mail access protocol, Interactive mail access protocol, and Internet mail access protocol are some other names for this phrase. IMAP contacts your email provider to obtain a copy of all of your recent messages. Once you download them to your Mac or PC, they are immediately deleted from the email service.


# Features of IMAP

- ****Multi-Mailbox Management****: It supports the management of multiple mailboxes, allowing users to organize their emails into various categories or folders.
- ****Message Flags****: It provides the ability to add message flags, helping users keep track of the status of emails, such as whether they have been read.
- ****Selective Email Retrieval****: It allows users to decide whether to download the full content of an email or just retrieve the headers and decide later.
- ****Efficient Media Management****: When multiple files are attached to an email, IMAP simplifies the process of downloading media files by handling attachments efficiently.


# Working of IMAP

MAP follows Client-server Architecture and is the most commonly used email protocol. It is a combination of client and server process running on other computers that are connected through a network.

This protocol resides over the TCP/IP protocol for communication. Once the communication is set up the server listens on port 143 by default which is non-encrypted. For the secure encrypted communication port, 993 is used.

- ****Port 143****: Default non encrypted IMAP communication.
- ****Port 993****: Secure IMAP communication with encryption (SSL/TLS).

The following steps are taken for the working of the IMAP :

- Email client Gmail establishes a connection with Gmail's SMTP server.
- By approving the sender's and recipient's email addresses, the SMTP server verifies (authenticates) that the email can be sent.
- The email is sent to the Outlook SMTP server by Gmail's SMTP server.
- The recipient's email address is authenticated by the Outlook SMTP server.
- IMAP or POP is used by the Outlook SMTP server to deliver the email to the Outlook email client.


# Architecture of IMAP

he Internet Message Access Protocol (IMAP) is a client–server model that allows users to access and view email messages stored on remote servers. Here is a summary of the events:

- ****IMAP Clients:**** An IMAP client is an email application or software that users use to communicate with their email accounts. Examples include Microsoft Outlook, Mozilla Thunderbird, Apple Mail, and mobile email applications. The client communicates with the server to receive, manage, and send email messages.
- ****IMAP Server:**** The IMAP server stores email messages and manages user mailboxes. It responds to requests from IMAP clients and provides access to email folders and messages. The server stores emails in a structured format, usually organized in user-defined folders or mailboxes. Common IMAP server software includes Dovecot, Courier IMAP, Cyrus IMAP, and Microsoft Exchange Server.
- ****Network Protocols:**** It works over TCP/IP (Transmission Control Protocol/Internet Protocol) networks, and allows an client to connect to a server over the Internet or local area networks.

# Difference between POP3 and IMAP

| Post Office Protocol (POP3)                                                                                                                                                                     | Internet Message Access Protocol (IMAP)                                                                                                             |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| POP is a simple protocol that only allows downloading messages from your Inbox to your local computer.                                                                                          | IMAP is much more advanced and allows the user to see all the folders on the mail server.                                                           |
| The POP server listens on port 110, and the POP with SSL secure(POP3DS) server listens on port 995                                                                                              | The IMAP server listens on port 143, and the IMAP with SSL secure(IMAPDS) server listens on port 993.                                               |
| In POP3 the mail can only be accessed from a single device at a time.                                                                                                                           | Messages can be accessed across multiple devices                                                                                                    |
| To read the mail it has to be downloaded on the local system.                                                                                                                                   | The mail content can be read partially before downloading.                                                                                          |
| The user can not organize mail in the mailbox of the mail server.                                                                                                                               | On the mail server, the user can directly arrange the email.                                                                                        |
| The user can not create, delete,e or rename email on the mail server.                                                                                                                           | The user can create, delete,e or rename an email on the mail server.                                                                                |
| It is unidirectional i.e. all the changes made on a device do not affect the content present on the server.                                                                                     | It is Bi-directional i.e. all the changes made on the server or device are made on the other side too.                                              |
| It does not allow a user to sync emails.                                                                                                                                                        | It allows a user to sync their emails.                                                                                                              |
| It is fast.                                                                                                                                                                                     | It is slower as compared to POP3.                                                                                                                   |
| A user can not search the content of mail before downloading it to the local system.                                                                                                            | A user can search the content of mail for a specific string before downloading.                                                                     |
| It has two modes: delete mode and keep mode.<br><br>- In delete mode, the mail is deleted from the mailbox after retrieval.<br>- In keep mode, the mail remains in the mailbox after retrieval. | Multiple redundant copies of the message are kept at the mail server, in case of loss of message on a local server, the mail can still be retrieved |
| Changes in the mail can be done using local email software.                                                                                                                                     | Changes made to the web interface or email software stay in sync with the server.                                                                   |
| All the messages are downloaded at once.                                                                                                                                                        | The Message header can be viewed before downloading.                                                                                                |

Source: 
https://www.geeksforgeeks.org/computer-networks/internet-message-access-protocol-imap/