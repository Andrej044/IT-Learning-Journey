# Networking Core Protocols
  ## HTTP(S)
    HTTP - Hypertext Transfer Protocol; S - Secure
    Protocol relies on TCP and defines how browser communicates with web servers.
    
     - GET retrivies data from a server;
     - POST allows to submit new data to the server;
     - PUT allows create a new resource on the server and to update and overwrite existing information
     - DELETE used to delete a specified file or resource on the server.     
     
     HTTP and HTTP(S) commonly use 80 and 443 TCP ports.
   
  ## FTP
     File Transfer Protocol (FTP) is designed to transfer files.
     
     - USER is used to input username
     - PASS is used to enter the password
     - RETR(retrieve) is used to download a file from the FTP server to the client
     - STOR(store) is used to upload a file from the client tto the FTP server
     
     FTP server listens on TCP port 21 by default 
  
  ## SMTP
     Simple Mail Transfer Protocol (SMTP) defines howe a mail client
     talks with a mail server and how a mail server talks with another
     
     - HELO or EHLO initiates an SMTP session
     - MAIL FROM specifies the sender's email address
     - RCPT TO specifies the recipient's email address
     - DATA indicates that the client will begin sending 
       the content of the email message
     - . is sent on a line by itself to indicate the end of
       the email message
      
      The SMTP server listens on TCP port 25 default.