🔥 Firewall Configuration Task using UFW on Kali Linux

🎯 Objective
To configure and test basic firewall rules using UFW (Uncomplicated Firewall) on Kali Linux by:
- Blocking Telnet (port 23)
- Allowing SSH (port 22)
- Testing and validating rule behavior

🛠 Tools Used
- Kali Linux
- UFW (Uncomplicated Firewall)
- Telnet / Netcat for testing port access

📋 Steps Performed

1. 📦 Install UFW
sudo apt update
sudo apt install ufw

2. ✅ Enable UFW
sudo ufw enable

3. 🔍 Check Current Rules
sudo ufw status numbered

4. ⛔ Block Telnet (Port 23)
sudo ufw deny 23

5. 🧪 Test the Block
telnet localhost 23
# or
nc -zv localhost 23
✅ Expected Result: Connection refused

6. 🔓 Allow SSH (Port 22)
sudo ufw allow 22

7. 🧹 Remove Telnet Block Rule
sudo ufw delete deny 23

8. 📊 Final Rule Check
sudo ufw status numbered
✅ Expected Result: Only port 22 should be allowed

📸 Screenshots (Attach Separately)
- Enabling UFW
- Blocking port 23
- Telnet test result
- Allowing port 22
- Final firewall status

🧾 Summary
This task demonstrates basic firewall configuration using UFW. Port 23 (Telnet) was blocked to prevent insecure access and verified with Telnet/Netcat tools. SSH (port 22) was allowed for secure remote access. UFW rules filter incoming traffic based on specified ports, reducing system exposure and enhancing network security.

🧠 Key Commands Reference
sudo apt install ufw
sudo ufw enable
sudo ufw deny <port>
sudo ufw allow <port>
sudo ufw delete deny <port>
sudo ufw status numbered
