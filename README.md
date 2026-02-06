# Documentation

## Phase 1: Pre-Installation Setup
- Enable Virtualization: Ensure Virtualization is enabled in your BIOS (look for Intel VT-x or AMD-V). You can verify this in the Windows Task Manager under the Performance tab.

- Disable Hyper-V: Windows Hyper-V can interfere with VirtualBox. Run the specific disable command in Command Prompt as an administrator and restart your PC.

### Download Software:

- Download and install VirtualBox from the official website.

- Download the VirtualBox Extension Pack for features like USB 3.0 and clipboard sharing.

- Download the Kali Linux Installer Image (64-bit ISO) from the official Kali website.

## Phase 2: Creating the Virtual Machine
- VM Configuration: In VirtualBox, create a new machine named "Kali Linux" with the type set to "Linux" and version "Debian (64-bit)."

### Resource Allocation:

- RAM: Allocate at least 4GB (8GB is recommended if your system allows).

- CPU: Assign at least 2 cores for better performance.

- Storage: Create a virtual hard disk with at least 25GB to 50GB of space.

### Advanced Settings:

- Set Shared Clipboard and Drag and Drop to "Bidirectional."

- Increase Video Memory to 128MB.

- In the Storage settings, select the empty optical drive and load your downloaded Kali Linux ISO.

### Phase 3: Installing Kali Linux
- Booting: Start the VM and select Graphical Install from the boot menu.

- Initial Setup: Follow the prompts to choose your language, location, and keyboard layout.

- User Account: Set a hostname, create a new user account, and set a strong password.

- Partitioning: For beginners, choose "Guided - use entire disk" as the simplest setup.

- Software Selection: Stick with the default XFCE desktop environment, as it is lightweight and ideal for virtual machines.

- GRUB Bootloader: When prompted, select "Yes" to install the GRUB bootloader to ensure the system boots properly.

### Phase 4: Post-Installation Optimization
- Update System: Open the terminal and run the update and upgrade commands to ensure all tools and security patches are current.

- Guest Additions: Install VirtualBox Guest Additions using the terminal to enable full-screen mode, better display scaling, and smooth mouse integration.

- Shared Folders: Configure a shared folder in VirtualBox settings to easily transfer files between your host OS and the Kali Linux VM.
