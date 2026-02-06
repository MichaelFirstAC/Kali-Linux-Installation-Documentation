## Kali Linux 2025.1 Installation Documentation

This documentation outlines the standard procedure for installing **Kali Linux 2025.1** using the graphical installer.

---

### **1. Initial Boot & Localization**

* **Boot Menu:** Select **Graphical Install** to begin the interactive setup.
* **Language:** Select your preferred language (e.g., English).
* **Location:** Choose your country or region to set the local time zone.
* **Keyboard:** Select the appropriate keyboard layout (e.g., American English).

### **2. Network Configuration**

* **Hostname:** Enter a name for the system (default is `kali`).
* **Domain Name:** Leave blank unless the system is being joined to a specific network domain.

### **3. User Account Setup**

* **User Identity:** Provide the full name for the new non-root user.
* **Username:** Define the account username used for logging in and `sudo` commands.
* **Password:** Set a strong password. **Note:** This password is required for administrative tasks.

### **4. Disk Partitioning**

* **Method:** For most installations, select **Guided - use entire disk**.
* **Scheme:** Select **All files in one partition** (recommended for new users and standard environments).
* **Commitment:** Select **Finish partitioning and write changes to disk**, then confirm by selecting **Yes**.

### **5. Software Selection**

* **Desktop Environment:** The default is **XFCE** (recommended for performance). Alternatives include GNOME or KDE Plasma.
* **Collection of Tools:** It is recommended to keep the default "Top 10" and "Default selection" of tools checked to ensure standard penetration testing utilities are installed.

### **6. Bootloader Installation**

* **GRUB Installation:** When prompted to install the GRUB bootloader to the primary drive, select **Yes**.
* **Device Selection:** Manually select the primary storage device (typically `/dev/sda`) to finalize the bootloader path.

### **7. Post-Installation Steps**

* **Reboot:** Once the installation is complete, remove the installation media and select **Continue** to reboot.
* **System Update:** Immediately after logging in, open a terminal and run the following command to synchronize the package index and upgrade the system:
```bash
sudo apt update && sudo apt upgrade -y

```



---

**Would you like me to generate a checklist of the essential security tools included in this version of Kali?**
