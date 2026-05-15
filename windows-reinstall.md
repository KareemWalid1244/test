# Windows Reinstall

NOTE: if you would like to RAID to change your disk serial, please go to [RAID Reinstallation (AMD)](/blitz-perm/preparation/raid-reinstallation-amd.md) RAID is only possible AND recommended if:&#x20;

* You are AMD (on Intel, it is not recommended to RAID)
* Number of disks doesn't matter, one is fine
* Recommended to only have NVMe drives installed if RAIDing

Before continuing, we firstly **require** you to remove:

* DMA cards from inside your PC (Yes, it doesn't matter if your firmware is good, undetected, whatever, and no, the killswitch is not enough)
* Aim devices such as MAKCUs, ARDUINOs etc (unplug them)
* This following note only applies to GIGABYTE motherboards: You must remove your WIFI card from inside your PC if you use Ethernet AND your motherboard has AX or AC at the end of the model (e.g. B760 DS3H **AC**): [Helpful Video](https://www.youtube.com/watch?v=9j83rixFHxw) (On newer models such as the X870 they may give you the option to disable in BIOS. If this available to you, you don't need to take out the card).

You are EITHER following this reinstallation guide, or [RAID Reinstallation (AMD)](/blitz-perm/preparation/raid-reinstallation-amd.md). You are **not** doing both, or a mix of both. Got that? Let's get your USB drive all set up with the necessary files. Firstly, download and run either of the two tools below, depending on your preference.

[Windows 10 Media Creation Tool](https://go.microsoft.com/fwlink/?LinkId=2265055)\
\
[Windows 11 Media Creation tool](https://go.microsoft.com/fwlink/?linkid=2156295)<br>

* To download the Media Creation Tool, click your preferred version above.
* Run the **Media Creation Tool**
* Select **Create Installation Media (USB Flash Drive)**
* **Select the option shown below**

<figure><img src="https://alexzeel.gitbook.io/~gitbook/image?url=https%3A%2F%2F2510878693-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F97LB4aFg4eLrczV2s3HQ%252Fuploads%252FkTwy4t36VXjCh63LxlQH%252Fgewgegwe.jpg%3Falt%3Dmedia%26token%3Dd9ec2820-d18a-4c25-901b-8dbfac1991b1&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=97e38cd&#x26;sv=2" alt=""><figcaption></figcaption></figure>

\
After the tool is finished, click **"Finish"**\
\
**Your USB flash drive should look like this:**

<figure><img src="https://alexzeel.gitbook.io/~gitbook/image?url=https%3A%2F%2F2510878693-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F97LB4aFg4eLrczV2s3HQ%252Fuploads%252FV71Ka3UpB4puSd7QNTqx%252Fgebwgewgew.jpg%3Falt%3Dmedia%26token%3Dc872a593-841a-4a4f-aacf-d4887ae428b7&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=9a39ba84&#x26;sv=2" alt=""><figcaption><p>May look slightly different if you used the Windows 11 tool, that's okay.</p></figcaption></figure>

Download [this file](https://mega.nz/file/47BEFIYQ#ayjjlRsHVNCNxKU0_cYxg357LCPhWAnOo1NZjl_jDRQ), then drag it to your USB flash drive along with the other Windows files. Now, your USB should look like this:

<figure><img src="/files/3w1i1z71DWorVEpN2E58" alt=""><figcaption><p>This autounattend file will do a few things automatically. It will debloat your Windows of useless apps, automatically make a local account under the username "admin", disable BitLocker which is automatically enabled on Windows 11 installations, and set your region to the US unless you set it otherwise. Feel free to tweak the configuration of the autounattend to your liking on <a href="https://schneegans.de/windows/unattend-generator/">this site</a>.</p></figcaption></figure>

Lastly, you should:&#x20;

* Go to your motherboard's site
* Click on "Support/Drivers"
* Find your WLAN driver download (if you use WiFI) or LAN driver download (if you use Ethernet), then download and drag it onto your USB flash drive as well.&#x20;

This is because the driver may not automatically install after reinstalling Windows, leaving you without internet (guaranteed to happen with WIFI (WLAN). For LAN users, this happens often for INTEL ethernet cards. Usually, REALTEK Ethernet drivers install automatically, but there are cases in which it does not, so this is recommended in any case).

## Booting/Starting the USB flash drive

While you are holding the SHIFT key, click Restart.

<figure><img src="https://alexzeel.gitbook.io/~gitbook/image?url=https%3A%2F%2F2510878693-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F97LB4aFg4eLrczV2s3HQ%252Fuploads%252FlP1rzfGRPqibDxUo2JNp%252Fimage.webp%3Falt%3Dmedia%26token%3Dbe4c571b-7a27-4fa8-8a5e-8aab8a49c8e5&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=494c8415&#x26;sv=2" alt=""><figcaption></figcaption></figure>

* You will be on a blue screen with options to select. Select "**Use a device**"
* Then, select the USB *(*&#x49;t can be called *"(USB Model Name) Partition 1" or "UEFI Removable Device")*

<figure><img src="https://alexzeel.gitbook.io/~gitbook/image?url=https%3A%2F%2F2510878693-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F97LB4aFg4eLrczV2s3HQ%252Fuploads%252FwVMwPXLHV3j1Orqi9MyX%252Fimage%2520%281%29.webp%3Falt%3Dmedia%26token%3Ddd92d656-0840-4cc4-84af-2469b8367db7&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=1586865d&#x26;sv=2" alt=""><figcaption><p>If this button doesn't show up, please set the USB drive to #1 in boot order/priority in BIOS settings (boot page/tab), then save and exit.</p></figcaption></figure>

* Click **"Install Now"**
* Select your **language**
* Once you arrive at this part of the reinstallation process, please select "Custom: Install Windows only (advanced)". Some may not have this option show up. That's fine, as long as you get to the screen with the partitions (next image shown below this one).

<figure><img src="/files/eSiTQBhYRSwWTurDG0FV" alt=""><figcaption></figcaption></figure>

Once on the screen below, please proceed to click "Delete" on every partition possible, until the screen looks like this:

<figure><img src="/files/xvSqixTDxFaiDUYEe0QH" alt=""><figcaption></figcaption></figure>

Keep in mind that if you have multiple drives, 2 for example, there will be a "Drive 1 Unallocated Space" along with "Drive 0 Unallocated Space", please make sure all drives have the "Unallocated" label in their name. If you have an SSD(s) + HDD(s), make sure you select the SSD's unallocated space before clicking next, or else your PC will be mega-slow.&#x20;

{% hint style="info" %}
Please note, if you are installing Windows 11, your USB partitions will also show up (e.g. "Disk 1 Partition 1: ESD-USB"). This is totally fine, and you can ignore it (do not try to delete it).
{% endhint %}

After you click Next/Install Now, wait for your installation to fully finish. Once you are in Windows, install your NIC drivers that you saved on your USB if needed for your internet to work.

{% hint style="danger" %}
Important Notes:

1. Do not login to Microsoft, OneDrive. Do not install the following apps: SteelSeries, Logitech G Hub, Razer, NVIDIA App, GeForce Experience and any similar apps that interact with your peripherals/hardware. They are all potential flags. A substitute for Logitech G Hub is the [Onboard Memory Manager](https://download01.logi.com/web/ftp/pub/techsupport/gaming/OnboardMemoryManager_2.5.358.exe).
2. Do NOT install the game(s) that you are spoofing for, please follow the rest of the guide and acquire EXPLICIT confirmation from staff before doing so.
   {% endhint %}


---

# Agent Instructions: Querying This Documentation

If you need additional information that is not directly available in this page, you can query the documentation dynamically by asking a question.

Perform an HTTP GET request on the current page URL with the `ask` query parameter:

```
GET https://perm-1.gitbook.io/blitz-perm/preparation/windows-reinstall.md?ask=<question>
```

The question should be specific, self-contained, and written in natural language.
The response will contain a direct answer to the question and relevant excerpts and sources from the documentation.

Use this mechanism when the answer is not explicitly present in the current page, you need clarification or additional context, or you want to retrieve related documentation sections.
