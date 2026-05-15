# ARP

If your ARP is flagged in, for example, Fortnite, one or two things will occur:

* You could get 24hr banned on a few reports (Can also be caused from not RAIDing correctly)
* You could be VPN kicked out of tournaments (FOR THIS ISSUE, IT IS MORE LIKELY TO BE TPM OR DISK, NOT ARP. IF TPM AND DISK HAVE BEEN CHANGED/SPOOFED, THEN IT IS LIKELY TO BE ARP)

To fix this issue and change your ARP, read below.

1. Think of ARP tables as your router's MAC address. They cannot be spoofed permanently unless you have a specific firmware on your router, and most routers are incompatible with this firmware.

* Check if your router model is compatible [here](https://openwrt.org/toh/start).
* A recommendation for a cheap OpenWRT router that comes preflashed with this firmware (thus allowing you to change ARP tables whenever you'd like) is the [GL.iNet GL-SFT1200 (Opal)](https://www.gl-inet.com/products/gl-sft1200/), a cheap travel router that has below-average speeds. [Here is a video](https://www.youtube.com/watch?v=geEyNVH6NJE) for spoofing this router's ARP, courtesy of Intel (a guy, not the brand!)
* For a higher quality router, we recommend the [GL.iNet GL-MT6000 (Flint 2)](https://www.gl-inet.com/products/gl-mt6000/), which also comes preflashed with the firmware. [Here is a video](https://www.youtube.com/watch?v=B_71zvEJDVQ) for spoofing this router's ARP, once again Intel's video.

2. This next method involves essentially using your phone as a mini-router, and may result in slightly slower speeds (depends on the phone, and your router/data plan). However, on the plus side, this method doesn't need to you to spend any money!

* Disable onboard LAN controller, WiFi, Bluetooth in BIOS
* Grab a normal charging cable (cannot be a short-length one) that can connect your phone to your computer (USB-C to USB-A in most cases), and plug your phone in to your PC using the cable.&#x20;
  * Then, for Android phones, select USB tethering in the notification option (device connection), and it should connect automatically. (This will use the Android phone's WiFi connection, not your data). The connection will show up as an Ethernet type connection in your "Network Connections" (WIN + r, NCPA.CPL) window if done correctly
  * For iPhones, it's slightly more complicated. You need to install the iTunes desktop app, then turn on your hotspot on your phone, plug it into your PC, and a prompt will come up in the iTunes app. Confirm it, then it should connect (it will unfortunately use your phone data on iPhones). The connection will show up as an Ethernet type connection in your "Network Connections" (WIN + r, NCPA.CPL) window if done correctly


---

# Agent Instructions: Querying This Documentation

If you need additional information that is not directly available in this page, you can query the documentation dynamically by asking a question.

Perform an HTTP GET request on the current page URL with the `ask` query parameter:

```
GET https://perm-1.gitbook.io/blitz-perm/arp-tables-fn-tourneys-faceit-vgk/arp.md?ask=<question>
```

The question should be specific, self-contained, and written in natural language.
The response will contain a direct answer to the question and relevant excerpts and sources from the documentation.

Use this mechanism when the answer is not explicitly present in the current page, you need clarification or additional context, or you want to retrieve related documentation sections.
