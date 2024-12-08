# tp-link-t2u-plus
not detecting
Fixing USB WiFi Adapter Archer T2U V3 Issues on Kali Linux
2024-07-15 00:40:28
Tags: #Linux Driver #Installation
Model: Archer T2U  
Hardware Version: V3
Firmware Version:

If you're experiencing issues with your USB WiFi adapter on Kali Linux, you're not alone. After a recent upgrade, my adapter stopped working. Here's how I resolved the issue by installing a different driver.

 

Step 1: Remove the Old, Defective Driver


First, identify and remove the old driver.

    Get the status of the old driver:

   
   sudo dkms status
   

2. Remove the old driver:


   Replace `old-driver-name` with the actual name of your old driver


   sudo dkms remove -m old-driver-name --all

 

Step 2: Install a Newer Driver


Next, install a newer driver.

1. Clone the Repository:


   git clone https://github.com/morrownr/8821au-20210708.git

 

2. Navigate to the Directory:
   
   cd 8821au-20210708


3. Install the Driver:


   sudo ./install-driver.sh

 

note: after finishing the installation it will ask you if you want to modify the configuration, i didn't change anything. after exiting the configuration file it will ask for a reboot.

 

Step 3: Reboot
Reboot your system to apply the changes.


