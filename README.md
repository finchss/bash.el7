# bash.el7

<strong>Q: What is this? </strong><br>
A: bash RPM package for CentOS 7/x86_64 with (forced, feature cannot be turned off) history logging to syslog enabled. 

<strong>Q: How does the output look like? </strong><br>
A: All bash comands will be logged in /var/log/messages by default:
<pre>
[root@localhost steve]# tail -f /var/log/messages 
Jul  7 21:36:38 localhost -bash: HISTORY: PID=1268 UID=0 ip a
Jul  7 21:36:44 localhost systemd: Created slice User Slice of steve.
Jul  7 21:36:44 localhost systemd: Started Session 2 of user steve.
Jul  7 21:36:44 localhost systemd-logind: New session 2 of user steve.
Jul  7 21:36:45 localhost -bash: HISTORY: PID=1301 UID=1000 w
Jul  7 21:36:45 localhost chronyd[678]: Selected source 162.159.200.123
Jul  7 21:36:46 localhost -bash: HISTORY: PID=1301 UID=1000 dmesg
Jul  7 21:36:49 localhost -bash: HISTORY: PID=1301 UID=1000 sudo bash
Jul  7 21:36:53 localhost bash: HISTORY: PID=1324 UID=0 tail -f /var/log/messages
Jul  7 21:37:46 localhost bash: HISTORY: PID=1324 UID=0 tail -f /var/log/messages
</pre>

<strong>Q: Why? </strong><br>
A: Surveillance, security, honeypots, etc.

<strong>Q: How to (short, insecure, do not run unsigned binaries)? </strong><br>
A: <pre>
