# Task-4-Setup-and-Use-a-Firewall-on-Windows-Linux
# Windows Firewall Configuration and Testing

This project demonstrates how to configure and test basic firewall rules on a Windows system using **Windows Defender Firewall with Advanced Security**.

---

## Objective

- Configure firewall rules to allow or block specific traffic
- Test the firewall rules using tools like Telnet
- Restore firewall to original state after testing


## Tools Used

- **Windows 10/11**
- **Windows Defender Firewall with Advanced Security**
- **Command Prompt**
- **Telnet Client** 

## Steps Performed

### 1. Open Firewall Configuration Tool
- Open *Control Panel*
- Navigate to:  
  `System and Security > Windows Defender Firewall > Advanced Settings`

### 2. List Current Rules
- In the left panel, select *Inbound Rules*
- Reviewed existing rules applied to the system

---

### 3. Block Inbound Traffic on Port 23 (Telnet)
- Created a *new inbound rule*
  - Type: Port
  - Protocol: TCP
  - Port: `23`
  - Action: *Block the connection*
  - Applied to all profiles (Domain, Private, Public)
  - Named: `Block Telnet Port 23`

### 4. Test the Rule
- Installed *Telnet Client*:
  - Control Panel > Programs > Turn Windows features on or off > Check **Telnet Client**
  - Restarted system if required
- Opened Command Prompt:
  ```bash
  telnet localhost 23

---

### 5. Allow SSH (Port 22)

- Created a new **Inbound Rule**:
  - **Type**: Port
  - **Protocol**: TCP
  - **Port**: 22
  - **Action**: Allow the connection
  - **Applied To**: Domain, Private, and Public profiles
  - **Name**: `Allow SSH Port 22`
 SSH is commonly used for remote secure access. On Windows, this rule has no effect unless an SSH server is running (e.g., OpenSSH).

### 6. Remove Telnet Block Rule

- Opened **Windows Defender Firewall with Advanced Security**
- Went to **Inbound Rules**
- Found the rule named `Block Telnet Port 23`
- **Right-clicked and deleted** the rule
- Result: Firewall returned to its **original state**

### 7.  Document What Was Done

- **Tools Used**:
  - Windows Defender Firewall with Advanced Security
  - Command Prompt (`cmd`)
  - Telnet Client (installed via Windows Features)

- **Rules Created**:
  1. Blocked TCP port `23` (Telnet) → tested and confirmed blocked
  2. Allowed TCP port `22` (SSH) → added for secure access

- **Test Performed**:
  ```bash
  telnet localhost 23
  

### 8.  Summary: How Firewall Filters Traffic
A firewall filters network traffic by checking every connection request against a set of rules

Rules can be set to Allow or Block traffic based on:

Port number

IP address

Application

Protocol (TCP/UDP)

In this example:

Telnet (port 23) was blocked, preventing unsecure access

SSH (port 22) was allowed, enabling secure access if needed'


![Screenshot 1](https://user-images.githubusercontent.com/xxxx/Task 4.1.png)
![Screenshot 1](https://user-images.githubusercontent.com/xxxx/Task 4.2.png)
![Screenshot 1](https://user-images.githubusercontent.com/xxxx/Task 4.3.png)
![Screenshot 1](https://user-images.githubusercontent.com/xxxx/Task 4.4.png)
![Screenshot 1](https://user-images.githubusercontent.com/xxxx/Task 4.5.png)
![Screenshot 1](https://user-images.githubusercontent.com/xxxx/Task 4.6.png)
![Screenshot 1](https://user-images.githubusercontent.com/xxxx/Task 4.7.png)








  
