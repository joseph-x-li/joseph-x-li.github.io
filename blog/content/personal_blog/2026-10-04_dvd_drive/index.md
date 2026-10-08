+++
title = "How Claude Fixed My DVD Drive"
+++

*A troubleshooting session with Claude Code, lightly edited for the blog.*

---

**Me:** hi

**Claude:** Hi! What can I help you with today?

---

**Me:** I currently have plugged into this MacBook an Asus N Drive DVD drive, but it's not opening the DVD player. When I first plugged it in, it asked me permission to connect the drive, and I hit Allow, but since then, it has not been working. Can you figure out what's wrong?

*Claude checked the USB device list, the optical drive status (`drutil`), the external disks (`diskutil`), and the I/O Registry.*

**Claude:** I found the problem: **Google Chrome has taken control of the drive, so macOS can't use it.**

The Mac sees the drive fine (ASUS External Drive, USB ID 0b05:1a28), and it presents itself as a normal mass-storage device. But the system driver that would let macOS read discs never attached to it. Instead, Chrome has opened the drive directly:

```
ASUS External Drive
  ├─ IOUSBHostInterface@0   (mass storage, no system driver attached)
  └─ Google Chrome          (has the device open)
```

That's why `drutil` and Disk Utility don't see the drive at all. The permission prompt you clicked **Allow** on was most likely Chrome asking whether a website could connect to a USB device, not macOS asking. Once you allowed it, Chrome took the drive for that site and blocked macOS from using it.

**To fix it:**
1. In Chrome, go to `chrome://settings/content/usbDevices` and remove the ASUS drive from any site listed there.
2. Quit Chrome completely with ⌘Q.
3. Unplug the DVD drive and plug it back in.
4. Insert a disc.

---

**Me:** Can I use Google Chrome to actually view the DVD and its movie contents

**Claude:** No, Chrome isn't a good way to watch a DVD movie, for two reasons:

- **The video format:** DVD movies are stored as MPEG-2 video in `.VOB` files. Chrome can't play MPEG-2, so even if it could read the files you'd get no picture.
- **Copy protection:** Most store-bought DVDs are encrypted with CSS, and Chrome has no way to decrypt them.

**What to use instead:**
1. **Apple's DVD Player app.** It's built into macOS, hidden at `/System/Library/CoreServices/Applications/DVD Player.app`.
2. **VLC** (free, videolan.org). It plays almost any DVD and is the best backup option.

One thing to watch for: the first time you play a disc, the drive may ask you to set a region code. The number of times you can change it is limited, so pick the region that matches your discs.

---

**Me:** Okay, I quit Chrome completely, but it's still broken.

*Claude confirmed Chrome had fully let go of the drive, then dug into the kernel logs. Along the way it discovered its earlier log searches had silently returned nothing, because in zsh, `log` is a built-in command (it reports who has logged in). It has to be called as `/usr/bin/log`. 🙃*

**Claude:** Chrome wasn't the real problem. With Chrome closed I could read the system logs properly, and they show what's actually going wrong.

macOS detects the drive and loads the correct DVD driver. But every time the driver tries to talk to the drive, the transfer fails with a `transaction error`. macOS resets the drive and tries again, five times within about 4 seconds, then gives up:

```
endpoint 0x81: status 0xe00002ed (transaction error): 0 bytes transferred
USB device 0B051A28 - will be reset!
... fConsecutiveResetCount > MaxConsecutiveResets (5)
IOUSBMassStorageDriver: stop
```

So this is a problem with the physical connection. The drive drops out the moment real data starts moving, which happens when the motor spins up and draws the most power. The usual causes, from most to least likely:

1. **Not enough power.** These ASUS drives need more power than a single USB port gives during spin-up. Connect the second USB plug or power input if there is one, or use a powered USB hub.
2. **A bad cable or adapter.** Try a different adapter or a USB-C port directly on the Mac.
3. **The drive is stuck.** Unplug everything for about 30 seconds, then plug it back in.
4. **A failing drive.** Test it on another computer.

---
*plugs CD reader into USB hub with external power*  
**Me:**  not enough power was the issue. THANKS CLAUDE

**Claude:** Glad it's working! Enjoy the movie 🎬

---

### The takeaways

- Claude's pretty smart, yo