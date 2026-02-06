# Documentation

To install Kali Linux as your primary operating system (Bare Metal) rather than in a virtual machine, follow this official documentation guide. This process will replace your current OS or can be used for dual-booting.

### **1. Prerequisites**

* **A USB Drive:** At least 8GB capacity.
* **Kali Linux ISO:** Download the **"Installer Image"** from the [official Kali download page](https://www.google.com/search?q=https://www.kali.org/get-kali/%23kali-platforms).
* **Flashing Tool:** Download [BalenaEtcher](https://www.balena.io/etcher/) or [Rufus](https://rufus.ie/) to create the bootable drive.

### **2. Create Bootable Media**

1. Plug in your USB drive.
2. Open your flashing tool (e.g., Rufus).
3. Select the **Kali Linux ISO** you downloaded.
4. Select your **USB drive** as the target.
5. Click **Start/Flash** and wait for the process to complete.

### **3. Boot from USB**

1. Plug the flashed USB into the computer where you want to install Kali.
2. Restart the computer and repeatedly press the **BIOS/Boot Menu key** (usually F2, F10, F12, or DEL).
3. Select your **USB Drive** from the boot list.
4. When the Kali boot menu appears, select **Graphical Install**.

### **4. System Configuration**

1. **Language & Region:** Select your preferred language, location, and keyboard layout (e.g., American English).
2. **Network:** * Enter a **Hostname** (e.g., "kali").
* Leave **Domain Name** blank unless you are on a professional network.


3. **Users and Passwords:** * Enter your full name and a **Username**.
* Set a strong **Password**. You will need this for `sudo` commands later.



### **5. Disk Partitioning**

* **Option A (Single Boot):** Select **Guided - use entire disk**. This will wipe everything on the hard drive and install Kali as the only OS.
* **Option B (Dual Boot):** Select **Guided - use largest continuous free space** (Note: You must have shrunk your Windows partition beforehand to create this space).
* Confirm the changes by selecting **Finish partitioning and write changes to disk**, then select **Yes**.

### **6. Software Selection**

A window will appear asking which desktop environment and tools to install:

* **Desktop Environment:** XFCE is the default and recommended for performance. GNOME and KDE Plasma are also available.
* **Tools:** Keep the default "Top 10" or "Default" tools selected. You can always install more later.
* Click **Continue** to start the installation (this may take 10–20 minutes).

### **7. Finalizing**

1. **GRUB Bootloader:** When asked to install the GRUB bootloader to the primary drive, select **Yes**.
2. Select your hard drive (usually `/dev/sda` or `/dev/nvme0n1`) as the device for bootloader installation.
3. Once the "Installation Complete" message appears, remove the USB drive and click **Continue**.

### **8. Post-Installation**

Once the system reboots and you log in, open the terminal and run these commands to ensure your system is up to date:

```bash
sudo apt update
sudo apt full-upgrade -y

```

**Warning:** Installing Kali Linux as a primary OS on hardware requires caution, as it will erase data on the target partition. Always back up important files before proceeding.
