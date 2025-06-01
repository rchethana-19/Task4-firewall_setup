
# 🔐 Task 4 – Firewall Configuration using UFW on Kali Linux

## 🎯 Objective
Configure and test basic firewall rules using UFW on Kali Linux to understand how firewalls control inbound and outbound traffic.

---

## 🛠 Tools Used
- Kali Linux (2023 or later)
- UFW (Uncomplicated Firewall)
- Terminal
- Telnet (for test)

---

## ⚙️ Steps Performed

```bash
# Step 1: Check if UFW is installed and its status
sudo ufw status

# Step 2: If not installed
sudo apt update
sudo apt install ufw

# Step 3: Enable UFW
sudo ufw enable

# Step 4: Allow SSH (port 22) to prevent lockout
sudo ufw allow 22

# Step 5: Block Telnet (port 23)
sudo ufw deny 23

# Step 6: Verify rules
sudo ufw status numbered

# Step 7: Test Telnet block
sudo apt install telnet
telnet localhost 23

# Step 8: Remove the rule after test
sudo ufw delete deny 23

# Step 9: Disable UFW to restore system
sudo ufw disable
