---
description: RAID to change your disk serial. This guide is for AMD CPUs only.
icon: windows
---

# RAID Reinstallation (AMD)

Before continuing, we firstly **require** you to remove:

* DMA cards from inside your PC (Yes, it doesn't matter if your firmware is good, undetected, whatever, and no, the killswitch is not enough)
* Aim devices such as MAKCUs, ARDUINOs etc (unplug them)
* Your WIFI card from inside your PC if you use Ethernet and your motherboard is GIGABYTE + has AX or AC at the end of the model (e.g. B760 DS3H AC): [Helpful Video](https://www.youtube.com/watch?v=9j83rixFHxw) (On newer models such as the X870 they may give you the option to disable in BIOS. If this available to you, you don't need to take out the card).

You are EITHER following this reinstallation guide, or [Windows Reinstall](blitz-perm/preparation/windows-reinstall.md). You are **not** following both, or a mix of both. Got that? Let's get your USB drive all set up with the necessary files. Firstly, run the [Windows 10 Media Creation Tool](https://go.microsoft.com/fwlink/?LinkId=2265055) (Yes, it has to be Windows 10 for RAIDing), and select all the usual options (Media Creation, USB Flashdrive).

{% hint style="danger" %}
_**Please note, it MUST be Windows 10 for the media creation drive, not Windows 11. You are allowed to upgrade to Windows 11 via Windows Update AFTER you have fully reinstalled Windows 10 into your RAID array.**_
{% endhint %}

After the Media Creation Tool has finished, please click "Finish", wait for the window to close, then download [this file](https://mega.nz/file/47BEFIYQ#ayjjlRsHVNCNxKU0_cYxg357LCPhWAnOo1NZjl_jDRQ), and drag it to your USB flash drive along with the other Windows files. Now, your USB should look like this:

<figure><img src="https://perm-1.gitbook.io/blitz-perm/~gitbook/image?url=https%3A%2F%2Fcontent.gitbook.com%2Fcontent%2F9HSXS76SFRyfDd0dACNs%2Fblobs%2FOPMBou7NHgGCGDnixWXb%2Fimage.png&#x26;width=768&#x26;dpr=1&#x26;quality=100&#x26;sign=43cadbb4&#x26;sv=2" alt=""><figcaption><p>This is how the inside of your USB drive should look right now. This autounattend file will do a few things. It will debloat your Windows of useless apps, automatically make a local account under the username "admin", disable BitLocker which is automatically enabled on Windows 11 installations, and set your region to the US unless you set it otherwise. Feel free to tweak the configuration of the autounattend to your liking on <a href="https://schneegans.de/windows/unattend-generator/">this site</a>.</p></figcaption></figure>

Now, go to [this link](https://mega.nz/file/cvAyjKab#CDgGatPKLGKj70HOlh5pwwupUnc93W_YdXwXxI-Jd1I) and download the file, "raid.7z". Then extract it, and run the "nvme sata checker.exe" and the "chipset checker.exe". (Note: If you get an error, install [VCRuntimes](https://www.techpowerup.com/download/visual-c-redistributable-runtime-package-all-in-one/)). This will tell you two important pieces of info:

The "nvme sata checker.exe" will tell you:

* How many disks you have
* If they are NVMe or SATA disks

The "chipset checker.exe" will tell you:

* What your AMD chipset is, either AM4 or AM5

Using this information, continue to your corresponding RAID driver folder setup.

### AM4

If the chipset checker has told you that you are AM4, head into the "am4" folder. If you have only NVMe disk(s), drag the "nvme" folder to your USB. If you only have SATA disk(s), drag the "sata" folder to your USB. If you have both types of disks, drag both folders to your USB. It should look the same as one of these pictures, if done correctly:

<figure><img src="https://perm-1.gitbook.io/blitz-perm/~gitbook/image?url=https%3A%2F%2Fcontent.gitbook.com%2Fcontent%2F9HSXS76SFRyfDd0dACNs%2Fblobs%2FWgFF0uSVPlVRsJZobXvP%2Fimage.png&#x26;width=768&#x26;dpr=1&#x26;quality=100&#x26;sign=d267ad3&#x26;sv=2" alt=""><figcaption><p>How your USB drive should look if you have only NVMe disks, and you are AM4</p></figcaption></figure>

<figure><img src="https://perm-1.gitbook.io/blitz-perm/~gitbook/image?url=https%3A%2F%2Fcontent.gitbook.com%2Fcontent%2F9HSXS76SFRyfDd0dACNs%2Fblobs%2FDnjuvOcoIa7fQqHFcOtL%2Fimage.png&#x26;width=768&#x26;dpr=1&#x26;quality=100&#x26;sign=eee16f50&#x26;sv=2" alt=""><figcaption><p>How your USB drive should look if you have only SATA disks, and you are AM4</p></figcaption></figure>

<figure><img src="https://perm-1.gitbook.io/blitz-perm/~gitbook/image?url=https%3A%2F%2Fcontent.gitbook.com%2Fcontent%2F9HSXS76SFRyfDd0dACNs%2Fblobs%2FI1Ew6lsCwwz2LC5m3X4T%2Fimage.png&#x26;width=768&#x26;dpr=1&#x26;quality=100&#x26;sign=aae50ff5&#x26;sv=2" alt=""><figcaption><p>How your USB drive should look if you have both SATA and NVMe disks, and you are AM4</p></figcaption></figure>

### AM5

If the chipset checker has told you that you are AM5, head into the "am5" folder. Drag the "windows 10" folder to your USB drive. Should look like the below image:

<figure><img src="https://perm-1.gitbook.io/blitz-perm/~gitbook/image?url=https%3A%2F%2Fcontent.gitbook.com%2Fcontent%2F9HSXS76SFRyfDd0dACNs%2Fblobs%2FrfS9bx5v1tJS5nqGpI4d%2Fimage.png&#x26;width=768&#x26;dpr=1&#x26;quality=100&#x26;sign=2ad65198&#x26;sv=2" alt=""><figcaption></figcaption></figure>

Lastly, you should go to your motherboard's site, click on "Support/Drivers", find your WLAN (if you use WiFI) or LAN driver (if you use Ethernet), then download and place it onto your USB flash drive as well. This is because the driver may not automatically install after reinstalling Windows, leaving you without internet (guaranteed to happen with WIFI (WLAN). For LAN users, this happens often for INTEL ethernet cards. Usually, REALTEK Ethernet drivers install automatically, but there are cases in which it does not, so this is recommended in any case).

Before we start the BIOS settings, save your current disk serial with [this checker](https://mega.nz/file/szYByCzL#IPauPyk4JpunLvLpFPxghV5BKlrRLbHmCNGLUKv7FZc) and send the screenshot in the ticket. The screenshot should look something like this:

<figure><img src="https://perm-1.gitbook.io/blitz-perm/~gitbook/image?url=https%3A%2F%2Fcontent.gitbook.com%2Fcontent%2F9HSXS76SFRyfDd0dACNs%2Fblobs%2FNp1Aef1xBpCh0jOM0Ns2%2Fimage.png&#x26;width=768&#x26;dpr=1&#x26;quality=100&#x26;sign=b66f6ad3&#x26;sv=2" alt=""><figcaption></figcaption></figure>

Now, follow your corresponding BIOS and driver loading guide in one of the drop-downs below.

<details>

<summary>MSI Guide</summary>

1. Enter the BIOS. Make sure the CSM/UEFI indicator has UEFI as bold.
2. Go to **Settings > Advanced > Integrated Peripherals**.
3. Set **SATA Mode** to **RAID**, save and exit, then immediately re-enter the BIOS.
4. Go back to **Integrated Peripherals**.
5. Scroll down and open the **RAIDXpert Utility**.
6. Go into **Array Management**.
7. Select **Delete Arrays**.
8. Enable your disk, click Delete Array(s) (use the image and caption below as reference);
9. Then enable the "Confirm" option and click Apply Changes/Confirm
10. It should now display: **No arrays found on system**.
11. Go back and select **Create Array**.
12. The RAID type should default to **Volume** (leave it as is, if it is not on Volume, change it to be Volume. If Volume is not available at all, set it to RAIDABLE).
13. Go into **Select Physical Disks**.
14. Enable your disk and click **Apply Changes**.
15. Click **Create Array** at the bottom. (if you have multiple disks, repeat steps 5-14 for each disk you have)
16. Boot from the Windows USB by setting it to #1 in Boot Priority, then saving and exiting.
17. When you reach the partitions screen, there will be allocated disks if you are NVMe (**Disk 0 Partition 1 and/or Disk 1 Partition 1 depending on the amount of disks you have**). Select it, click **Delete**, and make it **Unallocated** (**Disk 0 Unallocated**).
18. Follow these driver installation steps (NOTE: DO NOT UNTICK THE CHECKBOX THAT SAYS "Hide drivers that are incompatible with this system"):

* **Load Driver > Browse > Expand the "ESD-USB" > Select your folder containing the raid drivers (will be named "sata" or "nvme" or "window 10") > OK > Select the top driver, `rcbottom.inf` > Next**
* **Load Driver > Browse > Expand the "ESD-USB" > Select your folder containing the raid drivers (will be named "sata" or "nvme" or "window 10") > OK > Select the driver with `rcraid.inf` > Next**
* **Load Driver > Browse > Expand the "ESD-USB" > Select your folder containing the raid drivers (will be named "sata" or "nvme" or "window 10") > OK > Select the driver with `rccfg.inf` > Next**

⚠️ **Important:** Make sure you install all three drivers — the last one is especially critical to ensure no flags and the correct RAID configuration is installed.

</details>

<details>

<summary>GIGABYTE Guide</summary>

1. Go to the BIOS.
2. Enter **Advanced Mode**, make sure CSM is disabled in the **Boot** tab, then go to the **Settings** tab.
3. Open **IO Ports**.
4. Go into **SATA Configuration**.
5. Enable **NVMe RAID Mode (if needed)** and set **SATA Mode** to **RAID**.
6. Save and exit, then immediately re-enter the BIOS.
7. Go back into **IO Ports**.
8. Scroll down and open the **RAIDXpert Utility**.
9. Go into **Array Management**.
10. Select **Delete Arrays**.
11. Enable your disk, click Delete Array(s) (use the image and caption below as reference);
12. Then enable the "Confirm" option and click Apply Changes/Confirm.
13. It should now display: **No arrays found on system**.
14. Go back and select **Create Array**. (if you have multiple disks, repeat steps 8-13 for each disk you have)
15. The RAID type should default to **Volume** (leave it as is, if it is not on Volume, change it to be Volume. If Volume is not available at all, set it to RAIDABLE).
16. Go into **Select Physical Disks**.
17. Enable your disk and click **Apply Changes**.
18. Click **Create Array** at the bottom. (if you have multiple disks, repeat steps 5-15 for each disk you have)
19. Boot from the Windows USB by setting it to #1 in Boot Priority, then saving and exiting.
20. When you reach the partitions screen, there will be allocated disks if you are NVMe (**Disk 0 Partition 1 and/or Disk 1 Partition 1 depending on the amount of disks you have**). Select it, click **Delete**, and make it **Unallocated** (**Disk 0 Unallocated**).
21. Follow these driver installation steps: (NOTE: DO NOT UNTICK THE CHECKBOX THAT SAYS "Hide drivers that are incompatible with this system")

* **Load Driver > Browse > Expand the "ESD-USB" > Select your folder containing the raid drivers (will be named "sata" or "nvme" or "window 10") > OK > Select the top driver, `rcbottom.inf` > Next**
* **Load Driver > Browse > Expand the "ESD-USB" > Select your folder containing the raid drivers (will be named "sata" or "nvme" or "window 10") > OK > Select the driver with `rcraid.inf` > Next**
* **Load Driver > Browse > Expand the "ESD-USB" > Select your folder containing the raid drivers (will be named "sata" or "nvme" or "window 10") > OK > Select the driver with `rccfg.inf` > Next**

⚠️ **Important:** Make sure you install all three drivers — the last one is especially critical to ensure no flags and the correct RAID configuration is installed.

</details>

<details>

<summary>ASUS Guide</summary>

1. Go to the BIOS.
2. Go from **EZ MODE** to **Advanced Mode**, make sure CSM is disabled in the **Boot** tab, then go to the **Settings** tab.
3. Open **SATA Configuration**.
4. Enable **NVMe RAID Mode (if needed)** and set **SATA Mode** to **RAID**.
5. Save and exit, then immediately re-enter the BIOS.
6. Go back to the **Advanced** tab.
7. Scroll down and open the **RAIDXpert Utility**.
8. Go into **Array Management**.
9. Select **Delete Arrays**.
10. Enable your disk, click Delete Array(s) (use the image and caption below as reference);
11. Then enable the "Confirm" option and click Apply Changes/Confirm.
12. It should now display: **No arrays found on system**.
13. Go back and select **Create Array**.
14. The RAID type should default to **Volume** (leave it as is, if it is not on Volume, change it to be Volume. If Volume is not available at all, set it to RAIDABLE).
15. Go into **Select Physical Disks**.
16. Enable your disk and click **Apply Changes**.
17. Click **Create Array** at the bottom (if you have multiple disks, repeat steps 8-17 for each disk you have)
18. Boot from the Windows USB by setting it to #1 in Boot Priority, then saving and exiting.
19. When you reach the partitions screen, there will be allocated disks if you are NVMe (**Disk 0 Partition 1 and/or Disk 1 Partition 1 depending on the amount of disks you have**). Select it, click **Delete**, and make it **Unallocated** (**Disk 0 Unallocated**).
20. Follow these driver installation steps: (NOTE: DO NOT UNTICK THE CHECKBOX THAT SAYS "Hide drivers that are incompatible with this system")

* **Load Driver > Browse > Expand the "ESD-USB" > Select your folder containing the raid drivers (will be named "sata" or "nvme" or "window 10") > OK > Select the top driver, `rcbottom.inf` > Next**
* **Load Driver > Browse > Expand the "ESD-USB" > Select your folder containing the raid drivers (will be named "sata" or "nvme" or "window 10") > OK > Select the driver with `rcraid.inf` > Next**
* **Load Driver > Browse > Expand the "ESD-USB" > Select your folder containing the raid drivers (will be named "sata" or "nvme" or "window 10") > OK > Select the driver with `rccfg.inf` > Next**

⚠️ **Important:** Make sure you install all three drivers — the last one is especially critical to ensure no flags and the correct RAID configuration is installed.

</details>

<details>

<summary>ASROCK Guide</summary>

1. Go to the BIOS.
2. Enter **Advanced Mode**, make sure CSM is disabled in the **Boot** tab, then go to the **Advanced** tab.
3. Open **Storage Configuration**.
4. Enable **NVMe RAID Mode** and set **SATA Mode** to **RAID**.
5. Save and exit, then immediately re-enter the BIOS.
6. Go back to the **Advanced** tab.
7. Scroll down and open the **RAIDXpert Utility**.
8. Go into **Array Management**.
9. Select **Delete Arrays**.
10. Enable your disk, click Delete Array(s) (use the image and caption below as reference);
11. Then enable the "Confirm" option and click Apply Changes/Confirm.
12. It should now display: **No arrays found on system**.
13. Go back and select **Create Array**.
14. The RAID type should default to **Volume** (leave it as is, if it is not on Volume, change it to be Volume. If Volume is not available at all, set it to RAIDABLE).
15. Go into **Select Physical Disks**.
16. Enable your disk and click **Apply Changes**.
17. Click **Create Array** at the bottom (if you have multiple disks, repeat steps 8-17 for each disk you have)
18. Boot from the Windows USB by setting it to #1 in Boot Priority, then saving and exiting.
19. When you reach the partitions screen, there will be allocated disks if you are NVMe (**Disk 0 Partition 1 and/or Disk 1 Partition 1 depending on the amount of disks you have**). Select it, click **Delete**, and make it **Unallocated** (**Disk 0 Unallocated**).
20. Follow these driver installation steps: (NOTE: DO NOT UNTICK THE CHECKBOX THAT SAYS "Hide drivers that are incompatible with this system")

* **Load Driver > Browse > Expand the "ESD-USB" > Select your folder containing the raid drivers (will be named "sata" or "nvme" or "window 10") > OK > Select the top driver, `rcbottom.inf` > Next**
* **Load Driver > Browse > Expand the "ESD-USB" > Select your folder containing the raid drivers (will be named "sata" or "nvme" or "window 10") > OK > Select the driver with `rcraid.inf` > Next**
* **Load Driver > Browse > Expand the "ESD-USB" > Select your folder containing the raid drivers (will be named "sata" or "nvme" or "window 10") > OK > Select the driver with `rccfg.inf` > Next**

⚠️ **Important:** Make sure you install all three drivers — the last one is especially critical to ensure no flags and the correct RAID configuration is installed.

</details>

After you click Next/Install Now, wait for your installation to fully finish. Once you are in Windows, install your NIC drivers that you saved on your USB if needed for your internet to work.

IF YOU WANT TO GO TO WINDOWS 11, NOW IS THE TIME TO DO SO, BEFORE CONTINUING. PLEASE USE THE INSTALLATION ASSISTANT, DO NOT USE A USB: [Download](https://go.microsoft.com/fwlink/?linkid=2171764)

After you finish upgrading to Windows 11, OR if you are going to stay on Windows 10, please send a screenshot of your new disk serials in the ticket, then wait for staff to confirm before continuing to the next step.

{% hint style="danger" %}
Important Notes:

1. Do not login to Microsoft, OneDrive. Do not install the following apps: SteelSeries, Logitech G Hub, Razer, NVIDIA App, GeForce Experience and any similar apps that interact with your peripherals/hardware. They are all potential flags. A substitute for Logitech G Hub is the [Onboard Memory Manager](https://download01.logi.com/web/ftp/pub/techsupport/gaming/OnboardMemoryManager_2.5.358.exe).
2. Do NOT install the game(s) that you are spoofing for, please follow the rest of the guide and acquire EXPLICIT confirmation from staff before doing so.
{% endhint %}
