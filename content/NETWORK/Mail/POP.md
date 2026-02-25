---
lastSync: Wed Feb 25 2026 15:37:45 GMT+0300 (Moscow Standard Time)
---
![](https://github.com/IserviceBY/KnowledgeBase/blob/v4/Images/Mail%20route.png?raw=true)
# Introduction to POP

POP stands for Post Office Protocol. The POP protocol was published in the year 1984. POP has been updated two times namely "POP2" and "POP3". The POP protocol is an Internet Standard Protocol that works on the application layer. It is used to get an access email from the mail server. The need for POP mainly arises when the user or client does not have a continuous internet connection and wants to receive email messages. The Pop client makes use of POP to pull email messages from the POP server. POP3 is the updated version of POP.

# What is POP3?

Post Office Protocol Version 3 is known as POP 3. Access to the mail inbox that is kept on the email server is made possible via the POP3 protocol. Messages can be downloaded and deleted via POP3 protocol. The POP3 client may quickly retrieve all of the messages from the mail server after it has established a connection with it. Even when the user is not connected, they can still view the messages locally. The protocol does not inherently support real-time synchronization or automatic checking for new messages; users can configure their email clients to check for new messages at intervals or manually. Many email programs, including Apple Mail, Gmail, and Microsoft Outlook, support the POP3 protocol, although IMAP is often preferred for its synchronization features.

# Working of POP3

- Initially POP3 needs to establish a connection between the POP client and the POP server.
- Once a secure connection is established several commands are exchanged between them to perform the task.
- Once a connection is established client requests available email messages.
- The Server sends the available messages along with their size and unique identifier number.
- Once the client receives the message, it makes a request to the server for downloading the messages. The user marks such messages and sends them to the server.
- Upon receiving from the client-server sends the messages selected by the client and accordingly marks them as read or unread.
- The client if want sends a request for deleting the messages.
- Once the tasks are completed the client sends a close connection request to the server
- The server then sends an acknowledgment to the client and closes the connection.
# Features of POP3

- Emails are kept on a single device.
- Emails can only be accessed by one device.
- Additionally, every message sent is stored on the same device.
- The user must enable "Keep email on server" in the settings if they wish to save their messages on their device; otherwise, POP3 will erase them as soon as an app or piece of software installs.

# Advantages of POP3

- You can read the message offline as well.
- POP3 uses less space in storage.
- POP3 is simple to set up and utilize.
- Numerous email programs support POP3.
- The emails are already on our PC, so accessing them is quick and easy.
- We have no restrictions on the size of emails we send and receive.
- There is less requirement for server storage capacity because all emails are stored locally.

# Disadvantages of POP3

- It is not possible to achieve real-time synchronization with POP3.
- An email with malicious attachments can quickly compromise the system.
- POP3 does not allow simultaneous access to the same email on many platforms.
- You can delete a whole email folder at once.
- The email folder that is downloaded from the mail server could potentially become corrupted.
- Anyone utilizing your computer can access the email folder because the emails are stored locally.


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
# Source: 
https://www.geeksforgeeks.org/computer-networks/what-is-pop3-post-office-protocol-version-3/

