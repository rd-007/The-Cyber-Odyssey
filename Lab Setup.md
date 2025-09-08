# 🧪 Cybersecurity Lab Setup

- This document explains how to set up a safe penetration testing lab using **VMware Workstation**, **Kali Linux** (attacker), and multiple vulnerable machines (victims).  
- All projects in this repo will run inside this isolated lab.

---

## 🛠 Requirements
- Host OS: Windows / Linux / macOS
- Virtualization: [VMware Workstation](https://www.vmware.com/products/workstation-pro.html) / VMware Fusion
- Attacker VM: [Kali Linux](https://www.kali.org/get-kali/#kali-virtual-machines)
- Victim VMs:  
  - [Metasploitable2](https://sourceforge.net/projects/metasploitable/)  
  - [DVWA (Damn Vulnerable Web App)](http://www.dvwa.co.uk/)  
  - [OWASP Juice Shop](https://owasp.org/www-project-juice-shop/)  
- At least **8 GB RAM** and **50 GB free disk space**

---

## ⚙️ Step 1: Install VMware Workstation
1. Download & install VMware Workstation Player or Pro.
2. Enable virtualization in BIOS (Intel VT-x / AMD-V).

---

## ⚙️ Step 2: Import Virtual Machines
### Kali Linux (Attacker)
- Download Kali pre-built VMware image.
- Extract `.7z` and open the `.vmx` in VMware.

### Metasploitable2 (Victim)
- Download Metasploitable2 VM.
- Open `.vmx` in VMware.

### DVWA (Victim)
- DVWA can be set up on a lightweight Ubuntu VM or Docker container.
- **Option 1: Docker (Recommended)**

  ```bash
  docker run --rm -it -p 8081:80 vulnerables/web-dvwa


- Access at http://<DVWA-IP>:8081
---

- **Option 2: Manual Setup (Ubuntu/VM)**

- 1. Install LAMP stack.

- 2. Download DVWA.

- 3. Configure config.inc.php inside DVWA.

- 4. Start Apache & MySQL.

  
  ```bash
    git clone https://github.com/digininja/DVWA.git /var/www/html/dvwa
---

### OWASP Juice Shop (Victim)

- 1. Juice Shop runs perfectly in Docker.

- 2. Access at http://<JuiceShop-IP>:3000

    
    ```bash
    docker run --rm -p 3000:3000 bkimminich/juice-shop
---

### ✅ Lab Ready

### ⚠️ Note: 
- This lab is for education and practice only. 
- Never attack systems you don’t own or have permission for.
