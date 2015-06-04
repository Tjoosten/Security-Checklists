Server security checklist.
======================

## Secure network and Physical Environment

- [ ] Server is secured in locked rack or in an area with restricted access. 
- [ ] All non-removeable media is configured with file systems with access controls enabled. 
- [ ] The server displays a trespassing banner at login.

## Patching / Server Maintenance 

- [ ] There is a documented maintenance process to keep applications and operating systems at the latest practical patch levels.
- [ ] Vender-supported operating systems and application patches are readily aviable to RIT.
- [ ] Operating systems or applications that are no longer supported by the vendor or an open source community have an exception request pending or granted by the ISO.
- [ ] There is a documentedb maintenance process which includes a reasonable timetable for routine application of patches and patch clusters (service packs and patch rollups.)
- [ ] Systems supported by vendor patches have the patch application integrated into a documented server maintenance process.
- [ ] There is a process to inventory the current level of patches specific to this server. 
- [ ] There is a process for monitoring patch installation failures.

## Logging 

- [ ] Server is configured with appropiate real-time OS/application logging turned on. 
- [ ] There is a documented process for routine log monitoring and analysis.
- [ ] Reviews are concluded periodically to ensure the effectiveness of the server logging process. 
- [ ] There is a schedule for log monitoring of the server. 
- [ ] Logging has been configured to include at least 2 weeks of relevant OP/application information. 
  - [ ] All authencation.
  - [ ] Privilege escalation. 
  - [ ] User additions and deletions. 
  - [ ] Access control changes. 
  - [ ] Job schedule start-up 
  - [ ] System integrity information 
  - [ ] Log entries must be time and date stamped
- [ ] Intentional logging of private information, such as passwords, has been disabled.
- [ ] Logging is mirrored in real time and stored on another secure server. 

## System integrity controls

- [ ] System is configured to restrict changes to start-up procedures.
- [ ] There is a documented change control process for system configurations. 
- [ ] All unused services are disabled. 
- [ ] If availble, anti-virus software and definitions are current and up-to-date. 
- [ ] Server has a host firewall installed and enabled. 
