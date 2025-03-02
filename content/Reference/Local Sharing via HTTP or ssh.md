---
title: ⌨️ Local Sharing via HTTP or ssh
tags:
  - shell
---
### **Step 1: Connect the Ethernet Cable**

1.  Use a standard Ethernet cable to connect the two machines.
2.  Modern computers don't require a crossover cable, as most Ethernet ports auto-detect the connection type.

------------------------------------------------------------------------

### **Step 2: Configure IP Addresses**

You need to assign static IP addresses to both machines so they can communicate.

#### On Linux:

1.  Open a terminal.

2.  Use the following commands to set a static IP address:

    ``` bash
    sudo ip addr add 192.168.1.1/24 dev eth0
    sudo ip link set eth0 up
    ```

- Replace `eth0` with the correct interface name for your Ethernet adapter. You can find it using:

  ``` bash
   ip link
  ```
#### On macOS:

1.  Go to **System Preferences** \> **Network**.
2.  Select **Ethernet** in the left sidebar.
3.  Set **Configure IPv4** to **Manually**.
4.  Enter the following:
    - **IP Address**: `192.168.1.2`
    - **Subnet Mask**: `255.255.255.0`
5.  Click **Apply**.

------------------------------------------------------------------------

## **Using HTTP Server**

### **Step 3: Use Python's HTTP Server on Linux**

Linux typically has Python pre-installed, which can be used to create a simple HTTP server.

#### Steps:

**On the Linux Machine**:
- Open a terminal.
- Navigate to the directory containing the files you want to share:

`cd /path/to/share`

- Start a Python HTTP server:

`python3 -m http.server 8000`

- This will make the directory accessible via HTTP on port `8000`.

**On the macOS Machine**:

- Open a web browser.
- Enter the Linux machine's IP address and port:

http://192.168.1.1:8000

- Browse and download the files directly from the browser.

## **Using ssh-server**

### **Step 3: Enable File Sharing**

#### On Linux:

1.  Install and configure an SSH server to enable file transfers:

    ``` bash
    sudo apt update
    sudo apt install openssh-server
    sudo systemctl start ssh
    ```

2.  Note the username of the Linux system (you'll need it later).

#### On macOS:

No additional setup is required, as macOS has SSH and SCP (Secure Copy Protocol) built-in.

------------------------------------------------------------------------

### **Step 4: Transfer Files**

You can transfer files using the `scp` command.

#### From macOS to Linux:

1.  Open Terminal on the Mac.

2.  Run the command:

    ``` bash
    scp /path/to/file username@192.168.1.1:/destination/path
    ```

    - Replace `/path/to/file` with the file you want to transfer.
    - Replace `username` with the Linux username.
    - Replace `/destination/path` with the target directory on the Linux machine.

#### From Linux to macOS:

1.  Run this command on the Linux machine:

    ``` bash
    scp /path/to/file username@192.168.1.2:/destination/path
    ```

    - Replace `username` with your macOS username.

------------------------------------------------------------------------

### **Step 5: Verify the Transfer**

Check the destination folder on the target machine to ensure the files were transferred successfully.

------------------------------------------------------------------------
