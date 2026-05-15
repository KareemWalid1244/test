# VHD

As Intel users are strongly advised to not RAID0 due to the flags caused by the array "leaking" serials, meaning your real disk serials are easily visible to the anticheat. We recommend a different solution, called a VHD (Virtual Hard Drive). Think of this as creating a sort of blanket over your disk serials. It may work, or it may not work. Either way, it is a good safety precaution to take.

{% embed url="<https://www.youtube.com/watch?v=rp_n-yrCD6Y>" %}
Credits to Intel (the guy, not the brand) for providing so many useful video tutorials!
{% endembed %}

Notes:

* Do not install 1.1.1.1 like the video says
* Slow down the video to 0.5x if you are not able to follow the steps at a faster speed
* Once you have installed a game launcher onto your C drive (do NOT install the game launcher on the VHD), make sure you go into task manager and set it to disabled:

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/K1DvCzzkffjiKCPB8Gtp?alt=media" alt=""><figcaption></figcaption></figure>

* EVERY TIME you login to Windows, you must go to the location of the VHD (WIN + r, shell:startup), right click it, and then click "Mount". You must do this BEFORE opening the game launcher.


---

# Agent Instructions: Querying This Documentation

If you need additional information that is not directly available in this page, you can query the documentation dynamically by asking a question.

Perform an HTTP GET request on the current page URL with the `ask` query parameter:

```
GET https://perm-1.gitbook.io/blitz-perm/intel-disk-alternative/vhd.md?ask=<question>
```

The question should be specific, self-contained, and written in natural language.
The response will contain a direct answer to the question and relevant excerpts and sources from the documentation.

Use this mechanism when the answer is not explicitly present in the current page, you need clarification or additional context, or you want to retrieve related documentation sections.
