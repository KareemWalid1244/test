# ASUS Spoofing

Firstly, please run the "Backup Serial Checker.bat" inside the spoofer folder

Once done, press: Windows key + Shift + S, and take a **screenshot** of the **FULL** window, example below:

**Send your screenshot in the ticket (Ctrl + V). (THIS IS NOT A RECOMMENDATION, OUR SUPPORT MUST CONFIRM IF EVERYTHING IS GOOD OR NOT, NOT YOU!)**

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/qnfHPooTg0kKKPPWKN1l?alt=media" alt=""><figcaption><p>Example</p></figcaption></figure>

Proceed to press the **Windows key + R**, and then type **msinfo32** and press enter, then send a **screenshot** of the **Full** window into the ticket like so:

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/47OQLli0uwVEtNVI0lNG?alt=media" alt=""><figcaption></figcaption></figure>

Wait for staff's **confirmation** before continuing.

Now, download [this .bat file](https://mega.nz/file/VmRDgRZQ#9JRFGkMpknrN7Wo6VKKBY7SH-5sW4oEb_TfGJ-OOQIU) and run it as admin. After the CMD window closes, your "This PC" section of file explorer should look something like this, with a separate partition named "EEEEEEE".

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/sL7udHVffvCItuXMiHLo?alt=media" alt=""><figcaption></figcaption></figure>

If your file explorer matches, **continue with the steps below.**

Notes for before spoofing:

* If you have a Realtek ethernet card, install the Ethernet driver ("Realtek.exe")
* If your MSINFO32 is messed up, an example being your baseboard manufacturer is "JN3N4N34J1S9EJWN" (random numbers/letters), or displaying, for example, "MSI" when your actual motherboard is ASUS, please use the "SMBIOS Fixer" feature in the "Extra" tab of the spoofer. **This also applies to the following: "Manufacturer found: \[random gibberish value]".**
* &#x20;**If you do not know your real motherboard brand and model, you can check out this information in your BIOS (usually in the starting page), or physically on your motherboard inside your PC case.**
* Wait for staff's **confirmation** before continuing. If they approve, please **continue with the next steps below.**
* Run the spoofer, input your key, and click "Spoof". When it asks for your USB letter, input your newly made partition's letter. Make sure you only input the LETTER (1 character by itself, eg. "D" without quotations).
* Wait for the spoofing process to complete ("Spoofing process finished successfully, please restart your PC!" comes up).
* Once done, continue with the tutorial:

Now, boot into BIOS by doing the following:

* **Hold the shift key as you click "Restart", like this image indicates**

<figure><img src="https://2510878693-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces/97LB4aFg4eLrczV2s3HQ/uploads/lP1rzfGRPqibDxUo2JNp/image.webp?alt=media&token=be4c571b-7a27-4fa8-8a5e-8aab8a49c8e5" alt=""><figcaption></figcaption></figure>

* **Select 'Troubleshoot' then select "UEFI Firmware Settings", and click "Restart".**

<figure><img src="https://2510878693-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces/97LB4aFg4eLrczV2s3HQ/uploads/attUAVcnbEMYi8A7orcT/troubleshoot.webp?alt=media&token=aa0df94e-d9a6-4ce4-8706-c38d24b04775" alt=""><figcaption></figcaption></figure>

<figure><img src="https://2510878693-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces/97LB4aFg4eLrczV2s3HQ/uploads/k7wbshIubj6JYYmyiFCR/Rzd3vwjVqwfZoZBVBBWSw.jpg?alt=media&token=58792a9a-9e3e-42bd-848c-a92ad5be6720" alt=""><figcaption><p>Click UEFI Firmware Settings, then click "Restart"</p></figcaption></figure>

* **After it's completed the restart, your PC will boot into BIOS. Please switch from EZ Mode to Advanced Mode, then navigate to the "Boot" tab. Go into the "Secure Boot" section, then follow these 3 incredibly important drop-downs:**

<details>

<summary>Step 1: Configuring Secure Boot Settings</summary>

Go to Boot > Secure Boot > OS Type **\[Windows UEFI]** & Secure Boot Mode **\[Custom].** \
\
**Note:** If there is no '**Secure Boot Mode**', that's fine, just ignore that part.

</details>

<details>

<summary>Step 2: Preparing Keys in Key Management</summary>

Go into the "Key Management" section, and click "Clear Secure Boot Keys" at the top. Then, click "Install Default Secure Boot Keys". It should NOT look like this image below. Make sure they all say "Default/Factory" and NOT "0 | No Keys".  If it does look like this, click "Install Default Secure Boot Keys".

<div align="center"><figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/LOtM9ZFxbi0sTYP0DxcO?alt=media" alt=""><figcaption><p><span data-gb-custom-inline data-tag="emoji" data-code="274c">❌</span></p></figcaption></figure></div>

</details>

<details>

<summary>Step 3: Appending the Certificate (KEK Management + DB Management)</summary>

* Now open **KEK Management (Called "Key Exchange Keys" on ASUS laptops)**
* Choose the **Append Key** option
* Then, choose **No** (to load the EFI from a file on an external media)
* Choose the **3rd** option (usually - can be something different, go through trial and error until you find this file below)
* Choose the "**remember.der"** file
* Select **Public Key Certificate.**&#x20;
* If a window asking for a GUID comes up, just press enter.&#x20;
* Select **Yes** to append KEK with content from the "remember.der" file.

**A 'SUCCESS' MESSAGE SHOULD APPEAR IF YOU HAVE DONE THE STEPS CORRECTLY.**&#x20;

Now, please perform the exact same steps (from "Choose the Append Key option" and below), this time with **DB Management (Called "Authorized Signatures" on ASUS laptops).**

**If this returns with success as well, please continue with the guide.**

</details>

* **Go back to the starting page of the "Boot" tab, and change "Boot Option #1" to the boot option starting with "UEFI OS", and make sure "Boot Option #2" is set to "Windows Boot Manager".**

<figure><img src="https://2510878693-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces/97LB4aFg4eLrczV2s3HQ/uploads/1OEM3eMw0TFeUgqBIYaD/image.jfif?alt=media&token=c583dfa7-55ee-4927-bd18-bc3ec753b80f" alt=""><figcaption></figcaption></figure>

* **Save and exit BIOS, and make sure you see the yellow and white text flashing on your screen before Windows boots. This is the spoofing being done, it will ALWAYS show up.**
* After the spoofing process has finished, run the same serial checker above, and send a screenshot of the full window in the ticket, along with a screenshot of your system information (msinfo32). Then, await confirmation from staff before continuing with the guide. **(THIS IS NOT A RECOMMENDATION, OUR SUPPORT MUST CONFIRM IF EVERYTHING IS GOOD OR NOT, NOT YOU!)**

{% hint style="danger" %}
Make sure that you do not ever delete the EFI partition that was made, in Windows disk management, or set the UEFI OS to below your Windows Boot Manager in boot option priorities. If you do any of these, your serials will revert, and you will be banned. As well, an important note: If you are reinstalling Windows with a USB drive after you have spoofed and you have an ASUS motherboard, be sure to AVOID deleting the EFI partition that the "autopartition.bat" made. This way, the spoof will stay even after reinstalling Windows (Just make sure UEFI OS stays #1 in the boot order!)
{% endhint %}


---

# Agent Instructions: Querying This Documentation

If you need additional information that is not directly available in this page, you can query the documentation dynamically by asking a question.

Perform an HTTP GET request on the current page URL with the `ask` query parameter:

```
GET https://perm-1.gitbook.io/blitz-perm/spoofing/asus-spoofing.md?ask=<question>
```

The question should be specific, self-contained, and written in natural language.
The response will contain a direct answer to the question and relevant excerpts and sources from the documentation.

Use this mechanism when the answer is not explicitly present in the current page, you need clarification or additional context, or you want to retrieve related documentation sections.
