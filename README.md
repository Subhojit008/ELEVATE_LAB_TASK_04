# 🔥 Task 4: Setup and Use a Firewall on Windows/Linux

## 📌 Objective
Configure and test basic firewall rules to **allow** or **block** specific network traffic, then document the process.  
This task demonstrates the ability to secure systems by controlling network connections.

---

## 🛠 Tools Used
- **Windows**: Windows Defender Firewall with Advanced Security  
- **Linux**: UFW (Uncomplicated Firewall)  
- **Testing Tool**: Telnet (for port connectivity testing)

---

## 📋 Task Steps

### **1. View Current Firewall Rules**
- **Windows**:  
  - Open firewall configuration: `Win + R` → `wf.msc`
  - Check **Inbound Rules** and **Outbound Rules**
- **Linux**:
  ```bash
  sudo ufw status numbered
### **2. Block Inbound Traffic on Port 23 (Telnet)
Windows:

New Rule → Port → TCP → 23 → Block Connection → Apply to All Profiles.

Name the rule: Block Telnet Port 23.

Linux:

bash
Copy
Edit
sudo ufw deny 23/tcp
### **3. Test the Rule
bash
Copy
Edit
telnet localhost 23
Expected result: Connection refused.
### **4. Allow SSH (Linux Only)
bash
Copy
Edit
sudo ufw allow 22/tcp
### **5. Remove Test Block Rule
Windows:

Right-click the rule → Delete.

Linux:

bash
Copy
Edit
sudo ufw delete deny 23/tcp
📜 Summary
Firewalls filter network traffic based on rules.

Inbound Rules control incoming connections.

Outbound Rules control outgoing connections.

Blocking Port 23 (Telnet) helps prevent insecure, unencrypted remote access.
Allowing Port 22 (SSH) ensures secure remote management remains possible.

⚠️ Security Note
Always test firewall rules carefully to avoid locking yourself out of the system.

Avoid exposing unnecessary ports to the internet.

📂 Repository Structure
bash
Copy
Edit
Task4_Firewall/
│
├── README.md   # Project documentation
├── screenshots/ # Images showing steps and results
└── Network_Flitering_Steps.txt report # List of firewall commands used
