# HP Spoofing

{% hint style="info" %}
You will need an empty USB Drive formatted in FAT32 for the process on HP Motherboards. You can use the same USB Drive you used to install Windows, but format it beforehand, so it's empty.
{% endhint %}

Firstly, please run the "Backup Serial Checker.bat" inside the spoofer folder

Once done, press: Windows key + Shift + S, and take a **screenshot** of the **FULL** window, example below:

**Send your screenshot in the ticket (Ctrl + V). (THIS IS NOT A RECOMMENDATION, OUR SUPPORT MUST CONFIRM IF IT IS GOOD OR NOT, NOT YOU!).**

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/aLQ6KQmQR4ngdeddWgkR?alt=media" alt=""><figcaption><p>Example</p></figcaption></figure>

Proceed to press the **Windows key + R**, and then type **msinfo32** and press enter, then send a **screenshot** of the **Full** window into the ticket like so:

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/47OQLli0uwVEtNVI0lNG?alt=media" alt=""><figcaption></figcaption></figure>

Wait for staff's **confirmation** before continuing.

* Plug a USB Drive into your computer.
* Right-Click on the USB Drive in File Explorer on the left and select **format**
* Set the File System to **FAT32**, then click **start** and wait for the process to finish.
* Open the loader and you will be asked if you've **unlocked MPM (Manufacturer Mode)**. If you have, input "y" (no quotations), then skip the below process, and head to the notes at the end of this section. If you have not unlocked MPM or have no idea what that means, type "n" (no quotations).

Before proceeding, please understand that the following process is irreversible and we are not responsible for any damages caused to your device (this is just a disclaimer, don't be scared by it).

* In the spoofer, after clicking the spoof button, input your USB Drive letter (can be seen in the "This PC" section of file explorer) that it asks for, and wait for the process to complete.
* After the spoofer window closes automatically, hold the SHIFT key, click Restart, and continue holding SHIFT until the restart begins.

![](https://2510878693-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces/97LB4aFg4eLrczV2s3HQ/uploads/lP1rzfGRPqibDxUo2JNp/image.webp?alt=media&token=be4c571b-7a27-4fa8-8a5e-8aab8a49c8e5\)

* **Select 'Use a device' and select the USB (***AKA "Flash Drive", "(USB Model Name) Partition 1" or "UEFI Removable Device"***)**

![](https://2510878693-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces/97LB4aFg4eLrczV2s3HQ/uploads/wVMwPXLHV3j1Orqi9MyX/image (1).webp?alt=media&token=dd92d656-0840-4cc4-84af-2469b8367db7\)

* **Once it boots, you will see something that looks similar to this picture below:**

![](https://2510878693-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces/97LB4aFg4eLrczV2s3HQ/uploads/LHNCOpCTvIXeoaUBwHBW/image.png?alt=media&token=5ac74511-0863-4d83-bfe9-51886ea96e39\)

* After this process finishes, a popup will appear prompting; "Manufacturer Programming Mode to unlock mode?", with the options `Yes` or `No`
* &#x20;Click `Yes`
* It will boot into Windows again, and the USB Drive can be removed. In the rare case that Windows does not boot, please remove the USB Drive, and wait for a few minutes.
* Notes for before spoofing:

  * If you have a Realtek ethernet card, install the Ethernet driver ("Realtek.exe")
  * G**o ahead and open the spoofer, and click the SPOOF button.** You will be asked if you've unlocked MPM, input "y" with no quotations.

  After the spoofing process has finished ("Spoofing process finished successfully, please restart your PC!" comes up), restart your PC, run the same serial checker above, and send a screenshot of the full window in the ticket, then await confirmation from staff before continuing to the next step of the guide. **(THIS IS NOT A RECOMMENDATION, OUR SUPPORT MUST CONFIRM IF EVERYTHING IS GOOD OR NOT, NOT YOU!)**


---

# Agent Instructions: Querying This Documentation

If you need additional information that is not directly available in this page, you can query the documentation dynamically by asking a question.

Perform an HTTP GET request on the current page URL with the `ask` query parameter:

```
GET https://perm-1.gitbook.io/blitz-perm/spoofing/hp-spoofing.md?ask=<question>
```

The question should be specific, self-contained, and written in natural language.
The response will contain a direct answer to the question and relevant excerpts and sources from the documentation.

Use this mechanism when the answer is not explicitly present in the current page, you need clarification or additional context, or you want to retrieve related documentation sections.
