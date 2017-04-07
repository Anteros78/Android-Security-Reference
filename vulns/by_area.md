Its worth keeping in mind the nature of the below flaws, as they generally fall into camps such as:

- Needs physical (or adb) access
- Needs malicious app installed on the device 
- Needs access over digital cellular network
- MITM of comms of existing app on device

This doc is for tacking vulns found with the Android platform

- Accessability Layer
  - [How Android Accessibility Services Can Be Used To Hack Your Phone](http://www.makeuseof.com/tag/android-accessibility-services-can-used-hack-phone/) _17th May 2016_
     - Up to M-6-23 only as takes advantage of gaps in system overlays
  - [On Malware Leveraging the Android
Accessibility Framework](http://www.cs.uml.edu/~xinwenfu/paper/Accessibility.pdf) _~2013_
     - Uses Accessibility Framework to detect launcher icon presses and will show fake application instead. 
- Ashmem
  - [BitUnmap: Attacking Android Ashmem](https://googleprojectzero.blogspot.co.uk/2016/12/bitunmap-attacking-android-ashmem.html) _1st Dec 16_
    - Fixed in the Nov security update
- Binder
  - [racy getpidcon usage permits binder service replacement](https://bugs.chromium.org/p/project-zero/issues/detail?id=851) _15th June 2016_ 
- Chipsets
  - [QuadRooter: New Android Vulnerabilities in Over 900 Million Devices](http://blog.checkpoint.com/2016/08/07/quadrooter/) _7th August 16_
    - [Full details](https://www.checkpoint.com/downloads/resources/quadRooter-vulnerability-research-report.pdf)
    - 3 of 4 of these are IOCTL based, and patched in August security patches
- Dev
  - [Unofficial Copies of Android Support Libraries Being Distributed on JCenter](http://tools.android.com/unofficial-copies-of-android-support-libraries-being-distributed-on-jcenter) _20 Sept 16_
  - [Reminder: Check Your Projects Before Importing Them](https://commonsware.com/blog/2016/09/19/reminder-check-projects-before-importing.html) _19 Sept 16_ 
- Drag & Drop
  - [Be Careful of Drag-and-Drop on Android N](https://commonsware.com/blog/2016/06/01/be-careful-drag-drop-android-n.html) _1st June 2016_
- Filesystem
  - [How My Rogue Android App Could Monitor & Brute-force Your App’s Sensitive Metadata](https://www.arneswinnen.net/2016/09/how-my-rogue-android-app-could-monitor-brute-force-your-apps-sensitive-metadata/) _8th Sept 16_
- FLAG_SECURE
  - [PSA: FLAG_SECURE Window Leaks](https://commonsware.com/blog/2016/06/06/psa-flag-secure-window-leaks.html)  _6 June 16_
- Intents
  - [Surreptitious Sharing on Android](https://www.ibr.cs.tu-bs.de/news/ibr/surreptitious-sharing-2016-04-04.xml) _4th April 2016_
    - Accessing app private data via intents
- Kernel 
  - [Dirty COW explained: Get a moooo-ve on and patch Linux root hole](http://www.theregister.co.uk/2016/10/21/linux_privilege_escalation_hole/) _21 Oct 16_
    - [What is the Dirty COW vulnerability and how does it impact mobile security?](https://www.nowsecure.com/blog/2016/10/21/dirty-cow-vulnerability-mobile-impact/)
    - [PoCs](https://github.com/dirtycow/dirtycow.github.io/wiki/PoCs)
- MediaServer
  - [Return to libstagefright: exploiting libutils on Android](https://googleprojectzero.blogspot.co.uk/2016/09/return-to-libstagefright-exploiting.html) _7th Sept 2016_
  - [EXIF Parsing](http://www.forbes.com/sites/thomasbrewster/2016/09/06/google-android-one-photo-hack/#3db069111555) _7th Sept 16_ ([fix](https://twitter.com/timstrazz/status/773275505235591168))
  - StageFright
    - [Hardening the media stack](http://android-developers.blogspot.co.uk/2016/05/hardening-media-stack.html) _5th May 16_
    - [StageFrightened](http://googleprojectzero.blogspot.co.uk/2015/09/stagefrightened.html) _16th Sept 15_
- Mem Dumps
  - [Undocumented Patched Vulnerability in Nexus 5X Allowed for Memory Dumping Via USB](https://securityintelligence.com/undocumented-patched-vulnerability-in-nexus-5x-allowed-for-memory-dumping-via-usb/) _1st Sept 2016_  
  - [Forensics tool nabs data from Signal, Telegram, WhatsApp ](http://www.theregister.co.uk/2016/08/15/retroscope/?mt=1471266388161) _15h Aug 2016_
- OpenSSL
  - [Heartbleed](https://en.wikipedia.org/wiki/Heartbleed)
    - Android 4.1.1 only as mentioned in link
- TapJacking
  - SYSTEM_ALERT_WINDOW
    - System alert windows can only either consume or pass-on motion events based upon its `Window` bounds
      - A single overlay can have multiple `Windows`
    - [Android's Hover feature is a data HOOVER](http://www.theregister.co.uk/2016/11/08/androids_hover_/) _8th Nov 2016_
    - [How Tapjacking Made a Return with Android Marshmallow — and Nobody Noticed](https://www.xda-developers.com/how-tapjacking-made-a-return-with-android-marshmallow-and-nobody-noticed/)
- TCP
  - [Linux flaw that allows anyone to hijack Internet traffic also affects 80% of Android devices](https://blog.lookout.com/blog/2016/08/15/linux-vulnerability-android/) _15th Aug 16_
- TrustZone
  - [Extracting Qualcomm's KeyMaster Keys - Breaking Android Full Disk Encryption](https://bits-please.blogspot.co.uk/2016/06/extracting-qualcomms-keymaster-keys.html?m=1) _30th June 16_
- Uninstallation
  - [Life after App Uninstallation: Are the Data Still
Alive? Data Residue Attacks on Android](http://www.cis.syr.edu/~wedu/Research/paper/data_residue_ndss2016.pdf)
- Zygote
  - [Attack on Zygote: a new twist in the evolution of mobile threats](https://securelist.com/analysis/publications/74032/attack-on-zygote-a-new-twist-in-the-evolution-of-mobile-threats/) _3rd March 2016_
    - One of the best articles I have seen deconstructing malware 
