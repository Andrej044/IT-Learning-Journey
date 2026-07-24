# Telnet lab - Learn about the core TCP/IP protocols


# Lab_1
## Targets
    - Reach to remote Server(10.64.157.148)
    - Use metod GET
    - Get access to file flag.thml
    - Find a flag hidden in file.

## Used tools
    -Host machine with Ubuntu OS (VM)
    -Server nginx/1.18.0 (Ubuntu)
    -Telnet:  is an older network protocol that 
              allows to control a remote computer 
              or server over a TCP/IP network via 
              a text-based, command-line interface
              
## Terminal promts
    - telnet 10.64.157.148 80
    - GET /flag.html HTTP/1.1

# Lab_2
## Targets
    - Learn how to SMTP works

## Terminal promts
    - telnet 10.67.173.92 25
    - HELO client.thm
    - RCPT TO: strategos@server.thm
    - DATA
            