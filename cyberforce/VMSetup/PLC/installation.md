# PLC VM – Full Installation Guide

This guide explains how to set up the PLC VM from scratch in Proxmox and configure its network.

---

## 1. Create the VM in Proxmox

2. **Upload Ubuntu ISO (if not already uploaded)**
   - Select desired storage for iso
   - Select `Download from URL.`
   - Paste `https://releases.ubuntu.com/jammy/ubuntu-22.04.5-live-server-amd64.iso` into the URL slot
   - Press `Download`

3. **Create the VM**
   - Click **Create VM** (top right)
   - **General:**
     - Node: Select host node
     - VM ID: Auto or custom
     - Name: `PLC`
   - **OS:**
     - ISO Image: Select Ubuntu 22.04 Server ISO
   - **System:**
     - BIOS: `OVMF (UEFI)`
     - Machine: `q35`
     - SCSI Controller: VirtIO SCSI
   - **Disks:**
     - Bus/Device: `VirtIO Block`
     - Size: `20GB` (adjust as needed)
   - **CPU:**
     - Sockets: `1`
     - Cores: `2` (or more if needed)
   - **Memory:**
     - 2GB minimum (4GB recommended)
   - **Network:**
     - Bridge: `vmbr0` (same bridge as your LAN)
     - Model: `VirtIO (paravirtualized)`

4. **Finish creation**
   - Review settings and click **Finish**
   - Start the VM

---

## 2. Install Ubuntu Server 22.04

1. **Boot the VM**
   - Select the Ubuntu installer from the boot menu

2. **Language & Keyboard**
   - Choose your language and keyboard layout

3. **Network Configuration**
   - Select the network interface (`ens18`)
   - Set to **Manual**
   - Configure:
     - Address: `192.168.1.210/24`
     - Gateway: `192.168.1.1`
     - DNS: `192.168.1.1` (or `8.8.8.8`)

4. **Storage**
   - Select entire disk (guided install)

5. **Profile Setup**
   - Username: `blueteam`
   - Password: `BlueTeam2024!`
   - Hostname: `plc`

6. **SSH Setup**
   - Enable OpenSSH server

7. **Snap Packages**
   - Skip (no snaps required initially)

8. **Begin Install**
   - Wait for installation to complete
   - When done, reboot the VM

---

## 3. Post-Installation Setup

1. **Login**
   ```bash
   login: blueteam
   password: BlueTeam2024!