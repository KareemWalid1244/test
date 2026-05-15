# TPM

## TPM

VALORANT/LOL, Ricochet (COD/BO7) and Fortnite (specifically in tournaments) bans/flags TPM, and requires it enabled.

There are ways to solve this without getting delay banned:

1. In some cases, specifically with:

* GIGABYTE, MSI, and ASRock motherboards on an INTEL CPU
* AM4 motherboards with one of the newest BIOS patch that fixes some TPM security issues:

The TPM serial will change after flashing BIOS, if you have this security patch OR if you are GIGABYTE, MSI, and ASRock motherboards on an INTEL CPU. To check if this applies to you, enable TPM, download [this TPM checker](https://mega.nz/file/AmI2mbCL#u3CUEgrg592OyiuIwGuSwWkx28fzfriTWhOnSvYViIw), run it as admin, then send a screenshot of the output in your ticket, like so:

Then, follow the video in [Flashing BIOS](blitz-perm/preparation/flashing-bios.md) . Please note for Intel; If available, please use your motherboard's BIOS flashback button (a physical button usually near your USB ports or on your motherboard directly) for a guaranteed chance of this working. Please make sure the version you flash to is compatible with your CPU. If the SHA256 value (refer to the above image) changes after flashing BIOS, your TPM has been spoofed.

If the above method does not work, you can try our confirmed working method below. Please note:

* This method will NOT work on Fortnite IF YOU ARE AMD SPECIFICALLY (It is working for all other games and for Intel it will work on Fortnite!), so if you are AMD and want to play tournaments which require TPM enabled in Fortnite (e.g. Cash Cups), you must acquire a TPM chip and use that instead (ask in a ticket for support on which one to buy for your motherboard and from where).
* This method will not work for Intel CPUs that are BELOW the 11th gen.
* Please save your current TPM serials [using the same TPM checker](https://mega.nz/file/AmI2mbCL#u3CUEgrg592OyiuIwGuSwWkx28fzfriTWhOnSvYViIw) before continuing, and send the screenshot in the ticket.

1. Prepare the USB\
   Plug in a USB drive.\
   Download Rufus from:\
   [https://github.com/pbatard/rufus/releases/download/v4.11/rufus-4.11p.exe](https://github.com/pbatard/rufus/releases/download/v4.11/rufus-4.11p.exe)\
   Download Linux Mint from:\
   [https://pub.linuxmint.io/stable/22.2/linuxmint-22.2-cinnamon-64bit.iso](https://pub.linuxmint.io/stable/22.2/linuxmint-22.2-cinnamon-64bit.iso)
2. Create the bootable USB\
   Open Rufus.\
   Select the Linux Mint ISO.\
   Select your USB drive.\
   Change Partition Scheme from MBR to GPT.

Below is an image of how it should look:

\
If it matches, start the process and wait for it to finish.

3. Boot into Linux Mint\
   Restart your PC, get into BIOS/Boot Manager\
   Boot from the USB.\
   Select the first option at the top of the menu.
4. Once in Linux Mint, open Terminal.\
   Run:\
   `sudo su`
5. Add the mint user to sudo\
   Run:\
   `usermod -aG sudo mint`\
   Restart the PC.
6. Clear TPM in BIOS\
   Enter BIOS.\
   Go into Trusted Computing (usually located in the Advanced tab for most motherboards).\
   Set "Pending Operation" to "TPM Clear".\
   Save and exit with the USB drive as #1 in your boot priority/order.

Important note:\
You must boot directly into Linux Mint after clearing TPM.\
If Windows boots first, you must repeat the TPM clear step.

7. Open Terminal.\
   Run:\
   `sudo su`

Then copy all 7 commands below, and paste the entire thing into the terminal, then press enter:

`sudo apt update`\
`sudo apt install -y tpm2-tools openssl`\
`sudo tpm2_clear`\
`RAND=$(openssl rand -hex 32)`\
`sudo tpm2_createprimary -C o -g sha256 -G rsa -q $RAND -c primary.ctx`\
`sudo tpm2_readpublic -c primary.ctx -f pem -o key.pem`\
`sudo tpm2_evictcontrol -C o -c primary.ctx 0x81010001`

8. Confirm there are no errors (it should say "Persisted" as the last line).\
   Shut down the PC.\
   Unplug the USB.\
   Power on and boot into Windows.\
   Plug the USB back in, format it, then unplug it again.
9. Check if your TPM serials has changed (SEND THE SCREENSHOT OF NEW TPM SERIAL IN YOUR TICKET AS WELL), and check if your TPM status is "ready for use" in tpm.msc

If all is correct, then your TPM is spoofed.
