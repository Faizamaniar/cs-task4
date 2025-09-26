## cs-task4
Setup and Use a Firewall on Windows/Linux

## Objective : Configure and test basic firewall rules to allow or block traffic.
## Tools : Windows Firewall / UFW (Uncomplicated Firewall) on Linux.
## Deliverables : Screenshot/configuration file showing firewall rules applied.


# Steps Performed

**1. Open Windows Firewall**
- Opened **Windows Defender Firewall with Advanced Security** using `wf.msc`.  
- Navigated to **Inbound Rules** to view existing rules.  



**2. Create a New Rule to Block Port 23**
- Selected **Inbound Rules → New Rule**.  
- Chose **Port → TCP → Specific Port: 23**.  
- Action: **Blocking the connection**.  
- Applied to **Domain, Private, Public** profiles.  
- Named the rule: `Block Telnet (Port 23)`.  



**3. Test the Rule**
- Used PowerShell command to test connectivity on port 23:
  
  Test-NetConnection -ComputerName localhost -Port 23


## Key Concepts: Firewall configuration, network traffic filtering, ports, UFW, Windows Firewall.  


# GUI Steps :

1. Opened cmd type "wf.msc" to launch Windows Defender Firewall with Advanced Security.
2. Navigated to Inbound Rules → New Rule.
3. Selected Port → TCP → Specific local port : 23.
4. Chose Block the connection.
5. Applied the rule to Domain, Private, Public profiles.
6. Named the rule Block Telnet (Port 23).
7. Verified the rule in the Inbound Rules list.
8. Tested the rule using Windows PowerShell:
   type "Test-NetConnection -ComputerName localhost -Port 23".

# Screenshots Added

1. Current firewall rules
2. Blocking Telnet (Port 23)
3. Blocked telnet (Port 23)
4. Failed Telnet test
5. Removing the test block rule

# How Firewall Filters Traffic

A firewall is a network security device, either hardware or software-based, which monitors all incoming and outgoing traffic and, based on a defined set of security rules, accepts, rejects, or drops that specific traffic. It acts like a security guard that helps keep your digital world safe from unwanted visitors and potential threats. A firewall filters network traffic by acting as a "gatekeeper" that inspects incoming and outgoing data packets against a set of predefined security rules.

**Working**
- Placement: A firewall is positioned between a trusted internal network and an untrusted external network, such as the internet. 
- Packet Inspection: All data packets traveling to or from the network must pass through the firewall. 
- Rule Comparison: The firewall examines the header information of each packet and compares it against a set of pre-established security rules. 
- Decision-Making:
    Allow: If the packet matches the rules for safe and legitimate traffic, it is allowed to pass. 
    Block: If the packet is deemed suspicious, comes from a blacklisted source, or contains malicious code, it is denied access and blocked.
- Logging: Blocked or unusual traffic is recorded, providing security teams with data to review and potentially trigger real-time alerts. 


## Outcome : Basic firewall management skills and understanding of network traffic filtering.   
