# Spoofing Errors

## Spoofing Errors

### EFUSE FULL

If you get the "EFUSE full" error when the spoofer is spoofing your MAC address, this means:

* You have permanently spoofed your Realtek ethernet card too many times, so the EFUSE (the storage of writing capacity) has filled up. The cable does not have any correlation to this, it is the actual card connected to the motherboard that has this issue.
* You will not be able to permanently spoof your ethernet MAC address anymore.

Here are the solutions for this issue:

* USB to Ethernet adapter (WE RECOMMEND BUYING A REALTEK ONE SO IT IS SPOOFABLE):
* Get a WiFi USB and use that instead (Once it gets banned, it cannot be spoofed again):
* Get a PCIe Ethernet NIC that you will put into your PCIe slot on your motherboard which will let you use Ethernet as normal, with a different Ethernet card than your onboard one (WE RECOMMEND BUYING A [REALTEK](https://www.amazon.com/Realtek-Chipset-Ethernet-Interface-Software/dp/B007MWYCG2) ONE SO IT IS SPOOFABLE):
* USB tethering with your phone as the "router" and a charging cable as the "Ethernet cable" ( [ARP](blitz-perm/arp-tables-fn-tourneys-faceit-vgk/arp.md) has a detailed guide for this!). This solution requires no extra hardware.

For all solutions above, you must disable the onboard LAN controller in BIOS

Keep in mind that you can try simply changing the MAC address on a registry level, and you may get lucky with it working. To try this, go to the "Extra" tab in the spoofer, click "WiFi MAC" then wait for it to finish. It will change your MAC address, even if EFUSE is full, but only on a registry level. You will know if it worked if you do not get delay banned.

### CHECKSUM ERROR

This error means:

* You have an Intel Ethernet card (most likely the I219 or I216 model)
* Support will provide a possible fix for this by using a different tool in your ticket, and if that does not work you must either try one of the solutions listed above in the EFUSE FULL section above (e.g. PCIe NIC), or the registry MAC spoof, which is less likely to work (WiFi MAC option in the "Extra" tab of the spoofer). It will change your MAC address, even if EFUSE is full, but only on a registry level. You will know if it worked if you do not get delay banned.

Got a different error and think it should be documented here? Suggest it in the support ticket!
