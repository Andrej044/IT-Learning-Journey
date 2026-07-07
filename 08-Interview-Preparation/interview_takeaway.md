If an interviewer asks:

"What does DNS do?"

Don't answer:

"DNS translates names into IP addresses."

That's correct, but it's very textbook.

Instead, answer like this:

"DNS works like the Internet's phone book. People remember names like google.com, 
but computers communicate using IP addresses. 
DNS translates the name into an IP address so the computer knows where to send the request."

That's a clear explanation that both technical and non-technical people can understand.


Interviewer:

"A user has IP address 169.254.45.18. What is your first suspicion?"

A strong answer would be:

"A 169.254.x.x address usually indicates that the computer could not obtain an IP address from the DHCP server.
 I would check whether the DHCP service is available, verify the network connection, 
 and confirm that the device can reach the DHCP server."
 
 
 
 Imagine an interviewer asks:

"The user has a 169.254.x.x address. Does that always mean the DHCP server is broken?"

The answer is:

No. It means the computer couldn't obtain a lease from DHCP. That could be because the DHCP server is unavailable, 
but it could also be caused by a disconnected cable, a disabled network adapter, 
a faulty switch port, or another issue preventing communication with the DHCP server.

That answer would impress me because you're avoiding assumptions and thinking about multiple possible causes.
 
 