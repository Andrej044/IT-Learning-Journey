##Case File #001 Summary

#Initial Symptom
No Internet
No Printing
Evidence
APIPA (169.254.x.x)
No Gateway
No DNS
Other users unaffected
Cleaning staff moved cables

#Root Cause

Ethernet cable not fully seated in the wall jack.

#Why APIPA appeared

The computer couldn't reach the DHCP server, so Windows assigned itself an APIPA address.

#Lesson Learned

A 169.254.x.x address doesn't automatically mean the DHCP server is broken. It means the client failed to obtain a DHCP lease.

#The reason could be:

DHCP server down
Loose cable
Faulty network adapter
Bad switch port
Disabled adapter
VLAN issue