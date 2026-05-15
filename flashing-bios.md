# Flashing BIOS

{% hint style="warning" %}
**If you have RAID reinstalled, this step will reset your BIOS settings on most motherboards, and give you a BSOD (Blue Screen of Death) when trying to boot Windows (Inaccessible Boot Device error, see the image below). To fix this, after flashing BIOS completes, go immediately to BIOS and switch SATA mode back to RAID + enable NVMe RAID mode if present, then save and exit. You do not need to remake the RAID arrays.**

<p align="center"><img src="/files/hvj45dHMzTVebqPJTvCC" alt=""></p>
{% endhint %}

#### **MAKE SURE TO FLASH TO A DIFFERENT VERSION THAN YOUR CURRENT BIOS VERSION (ONE VERSION UP OR ONE VERSION DOWN IS FINE, MAKE SURE IT IS COMPATIBLE WITH YOUR CPU).** <a href="#make-sure-to-flash-to-one-older-version" id="make-sure-to-flash-to-one-older-version"></a>

> **ASUS:** [**https://youtu.be/Em7SRaG3L\_0?si=pzdHZjNo\_Fu0bAI**](https://youtu.be/Em7SRaG3L_0?si=pzdHZjNo_Fu0bAI2)

> **ASROCK:** [**https://youtu.be/dUCWRqOdLUw?si=1kA5ER1vzcgV3Npg**](https://youtu.be/dUCWRqOdLUw?si=1kA5ER1vzcgV3Npg)

> **GIGABYTE:** [**https://youtu.be/DIIde3s02kM?si=uojxszXk1YHz79sQ**](https://youtu.be/DIIde3s02kM?si=uojxszXk1YHz79sQ)

> **LENOVO:** [**https://youtu.be/AwOax1uWgYc?si=p0GFrReez2Ttk0UV**](https://youtu.be/AwOax1uWgYc?si=p0GFrReez2Ttk0UV)

> **MSI:** [**https://youtu.be/sKMub20CUNI?si=EBQyE2A7o3VdToSG**](https://youtu.be/sKMub20CUNI?si=EBQyE2A7o3VdToSG)

> **HP:** [**https://www.youtube.com/watch?v=C78QX272A44**](https://www.youtube.com/watch?v=C78QX272A44)


---

# Agent Instructions: Querying This Documentation

If you need additional information that is not directly available in this page, you can query the documentation dynamically by asking a question.

Perform an HTTP GET request on the current page URL with the `ask` query parameter:

```
GET https://perm-1.gitbook.io/blitz-perm/preparation/flashing-bios.md?ask=<question>
```

The question should be specific, self-contained, and written in natural language.
The response will contain a direct answer to the question and relevant excerpts and sources from the documentation.

Use this mechanism when the answer is not explicitly present in the current page, you need clarification or additional context, or you want to retrieve related documentation sections.
