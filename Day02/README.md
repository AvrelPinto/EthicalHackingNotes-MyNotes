# **Day 2 – Cybersecurity Notes**

## **Topic: Cyber Range Setup**

### **1. Overview**

Today focused on setting up a functional cyber range environment using **Kali Linux**. This environment will be used for penetration testing, ethical hacking, and cybersecurity lab exercises in upcoming sessions.

---

### **2. Setting up Kali Linux**

#### **Step-by-Step Process:**

1. **Download Kali Linux:**

   * We downloaded the official Kali Linux ISO from the [official website](https://www.kali.org/get-kali/).
   * Version downloaded: *Kali Linux 2024.2 (or current stable)* – 64-bit installer.

2. **Virtualization Software:**

   * We used **VirtualBox** (Oracle VM VirtualBox) as the virtualization platform.
   * Alternative mentioned: VMware Workstation Player (for those who preferred it).

3. **Creating a New Virtual Machine (VM):**

   * Opened VirtualBox → New → Named it “KaliLinux”.
   * Chose **Linux** as the OS type and **Debian (64-bit)** as the version.
   * Allocated:

     * RAM: **2 GB (minimum)**, preferred **4 GB+**
     * Virtual Hard Disk: **20 GB+**, dynamically allocated.

4. **Mounting ISO:**

   * Attached the Kali Linux ISO to the VM’s optical drive under **Settings → Storage**.

5. **Boot & Installation:**

   * Started the VM.
   * Chose “Graphical Install”.
   * Followed steps to set region, keyboard, user account, and partitioning.
   * Installed system packages and bootloader.

---

### **3. Problems Faced and Solutions**

#### **Problem 1: ISO Not Booting**

* **Issue:** VM started with a black screen or didn’t detect ISO.
* **Cause:** ISO file not correctly mounted.
* **Solution:**

  * Went to **Settings → Storage** and re-attached ISO correctly.
  * Ensured that the boot order had **Optical Drive** set as the first boot option.

#### **Problem 2: Slow Performance**

* **Issue:** System was extremely laggy after boot.
* **Cause:** Not enough RAM/CPU allocated.
* **Solution:**

  * Increased RAM to 4 GB and CPU to 2 cores via **Settings → System**.
  * Enabled **VT-x/AMD-V** in BIOS (some systems had this disabled).

#### **Problem 3: Network Issues in Kali**

* **Issue:** No internet connection inside the Kali VM.
* **Cause:** Wrong network adapter setting.
* **Solution:**

  * Changed **Network Adapter** to **Bridged Adapter** or **NAT** under **Settings → Network**.
  * Restarted network manager inside Kali using:

    ```bash
    sudo systemctl restart NetworkManager
    ```

#### **Problem 4: Download Corruption / Incomplete ISO**

* **Issue:** Some users had corrupted ISO downloads.
* **Cause:** Interrupted downloads or wrong mirror.
* **Solution:**

  * Re-downloaded ISO from a faster and verified mirror.
  * Verified checksum using:

    ```bash
    sha256sum kali-linux-*.iso
    ```
  * Compared it with the checksum provided on Kali's official site.

---

### **4. Key Takeaways**

* Importance of verifying ISO files before installation.
* Understanding virtualization basics and system requirements.
* Learning basic troubleshooting related to networking, BIOS settings, and system resource allocation.

---

