This file shows a simple case where a rule is used to block all the traffic coming from a specific IP.
Here are reported the different phases where, initially the rule is not se and then is applied showing the different behaviours of the traffic.

 
- Before applying the rule:

###########################################################
/ # ping 172.16.0.1
--- 172.16.0.1 ping statistics ---
10 packets transmitted, 10 packets received, 0% packet loss
round-trip min/avg/max = 0.128/0.566/0.798 ms
###########################################################

- After applying the rule in the iptables-sf pod:

############################################################
"iptables -I input -s 172.16.0.1 -j DROP"
############################################################

- The result is:

############################################################
/ # ping 172.16.0.1
--- 172.16.0.1 ping statistics ---
10 packets transmitted, 0 packets received, 100% packet loss
############################################################

So actually all the packets coming from the specific IP are dropped.
