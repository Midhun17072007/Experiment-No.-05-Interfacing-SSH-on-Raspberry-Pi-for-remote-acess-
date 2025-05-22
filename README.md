# Experiment-No.-05-Interfacing-SSH-on-Raspberry-Pi-for-remote-access-
### NAME:MIDHUN S
### ROLL NO:212224230158
### DEPARTMENT:AIDS
 ## AIM:
To enable and establish a secure SSH (Secure Shell) connection with the Raspberry Pi, allowing remote terminal access for configuration and control.
## APPARATUS REQUIRED:
S.No	Component	Quantity
1	Raspberry Pi board (any model)	1
2	MicroSD card with Raspberry Pi OS	1
3	Computer or Laptop	1
4	Power adapter for Raspberry Pi	1
5	Ethernet cable or Wi-Fi network	1
6	SSH Client (e.g., PuTTY/Terminal)	1
## THEORY:
SSH (Secure Shell) is a cryptographic network protocol used for secure data communication, remote command-line login, and remote command execution. Enabling SSH on a Raspberry Pi allows users to access and control the device remotely through a terminal or command prompt from another system on the same network.

There are several methods to enable SSH:
- Via Raspberry Pi Configuration Tool
- Using raspi-config on the terminal
- Creating a blank “ssh” file in the boot partition (headless setup)

SSH uses port 22 by default and requires an IP address of the Raspberry Pi to connect from a remote system. This is extremely useful for headless operation (without monitor/keyboard) and remote project development.

## PROCEDURE:
Step 1: Enabling SSH on Raspberry Pi
Method A – GUI (Graphical Mode):
1. Boot up the Raspberry Pi with desktop mode.
2. Open Preferences > Raspberry Pi Configuration.
3. Go to the Interfaces tab.
4. Enable the SSH option and click OK.
Method B – Terminal (CLI):
1. Open Terminal on the Pi.
2. Type: sudo raspi-config
3. Navigate to Interfacing Options > SSH, and choose Yes.
4. Exit and reboot if required.
Method C – Headless Mode:
1. Insert the microSD card into a PC.
2. Open the boot partition.
3. Create a new empty file named ssh (no extension).
4. Safely eject the card, insert into Raspberry Pi, and power it on.
Step 2: Finding Raspberry Pi IP Address
- In terminal: hostname -I
- Or check connected devices in your router's admin page.
Step 3: Connecting via SSH
On Windows (using PuTTY):
1. Open PuTTY.
2. Enter Raspberry Pi IP in the Host Name field.
3. Set Port to 22 and connection type to SSH.
4. Click Open.
5. Login using:
   - Username: pi
   - Password: raspberry (default)
On Linux/macOS:
1. Open terminal.
2. Type: ssh pi@<IP_ADDRESS>
3. Accept the fingerprint (first-time only).
4. Enter the password when prompted.
## SCREEN SHOTS OF THE INTERFACE 


![image](https://github.com/user-attachments/assets/5b54d7b3-7ab4-4936-a689-5d06f0e56b5b)



![image](https://github.com/user-attachments/assets/76a7f0f9-ba9a-40e4-bea7-cecf80ecd82b)


![image](https://github.com/user-attachments/assets/0ca3336d-608d-4490-a4a8-fe751b99c3e5)



## RESULT:
SSH was successfully enabled on the Raspberry Pi and a secure terminal connection was established using PuTTY (Windows) or Terminal (macOS/Linux). The Raspberry Pi was accessed remotely, and commands were executed through SSH.
