# 🚀 LAMP Stack Deployment with Ansible

This project automates the installation and configuration of the **LAMP Stack** (Linux, Apache, MySQL, PHP) using **Ansible**.  
It is designed for DevOps training and can be used to deploy on multiple servers.

---

## 📂 Project Structure
```
LAMP-Ansible/
│── roles/
│   ├── apache/        # Apache role
│   ├── mysql/         # MySQL role
│   └── php/           # PHP role
│── inventory          # Hosts file
│── lamp.yml           # Main playbook
```

---

## ⚙️ Requirements
- Ansible installed on the control node  
- SSH access to target servers  
- Linux environment (Ubuntu recommended)  

Install Ansible:
```bash
sudo apt update
sudo apt install ansible -y
```

---

## 🚀 Usage
1. Clone this repository:
   ```bash
   git clone https://github.com/<your-username>/LAMP-Ansible.git
   cd LAMP-Ansible
   ```

2. Update the `inventory` file with your server IPs:
   ```ini
   [webservers]
   192.168.1.10
   192.168.1.11
   ```

3. Run the playbook:
   ```bash
   ansible-playbook -i inventory lamp.yml
   ```

---

## 📸 Example Run
```bash
PLAY [Install and Configure LAMP Stack] ***************************

TASK [apache : Install Apache] ************************************
changed: [192.168.1.10]

TASK [mysql : Install MySQL] **************************************
changed: [192.168.1.10]

TASK [php : Install PHP] ******************************************
changed: [192.168.1.10]

PLAY RECAP ********************************************************
192.168.1.10              : ok=6    changed=5    unreachable=0    failed=0
```

---

## 👨‍💻 Author
- **Mahmoud Hossam Azouz**  
- ID: 42023141  
- Higher Technological Institute – Computer Science  
- Training Course: DevOps  

---
