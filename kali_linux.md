### Kali Linux black screen in Virtual Box

**<u>Problem:</u>**

I installed a fresh 2020.3 Kali 64 bit on to a VirtualBox Windows host. Initial desktop login worked fine. But after the initial apt update / apt upgrade and reboot, subsequent login sends me straight to a black screen.



**<u>Solutions:</u>**

1. Ctrl + Alt + F2 to bring up tty2 console

2. Login using your credential

3. Insert Guest Additions media (from VirtualBox menu)

4. `sudo apt install -y dkms build-essential linux-headers-generic linux-headers-$(uname -r)`

5. `sudo mount /dev/cdrom /media/cdrom`

6. `sudo /media/cdrom/VBoxLinuxAdditions.run`

7. Then restart the machine

---
