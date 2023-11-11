---
layout: post
title: "Graphene OS -Hardened security Handbook"
author: tchncs.de
---
GrapheneOS itself is the Hardened system for Android. Recommended by Edward Snowden: I use Graphene OS every day!

The system itself has been enhanced with kernel enhancements, browser enhancements, sandboxed profiles, randomized MAC locations, removal of Google, camera, microphone permissions management, and support for the secure hardware chip HSM technology on newer Pixel phones (Titan M2). But there is still a lot left to tweak to maximize security/privacy.

I'll show you the method I used here. And how I use the habits of Qubes OS/Tails/Whonix, combined with the system Grapheneos, which is expected and considered to be privacy and anonymity.

# Hardened // Security Step 1: Use a different profile for the main system
Immediately after installing the system, a profile must be created for switching.
The reason for this is that the main profile is Admin, which is the main directory.
The less attacked Admin is, the better. Please use 100% of the other profiles for daily use.

# Hardened // Security Step 2: Setup, disable all unneeded features to increase security.
Everything will be done according to the Graphene OS manual.

First we need to turn off the 2G/3G/5G network and use only LTE mode.
By default turn off the option to allow sensors.
Turn off all USB by default.
Turn off Bluetooth, Printing, NFC.
Keep Airplane Mode on.
Use power saving mode.
Screen set password/fingerprint and turn on password randomization.
Turn off developer functions
Disable OEM mode
Turn off positioning, camera, microphone (or cultivate good permissions control, which means you can't allow permissions on the fly.)

If you've done what I said above, you've basically got it all set up, and the next Hardened // Security Steps 3 ~ 4 are all about personal taste adjustments, or extreme security.


# Hardened // Security Step 3 : Disposable Container Protection Measures
The concept is like a disposable virtual machine, with greater control over permissions / protection against forensics.
How to use: In the configuration file, turn on Guest Mode and check the box to remove guest activity. After following the steps above, the disposable container will be completely destroyed whenever you close the guest mode. With GrapheneOS's perfect Sandbox isolation, this is basically a no-brainer!

# Hardened // Security Step 4 : Setting up an environment like Tails / Whonix to connect to the tor network 100% of the time.
Here we use inviZible Pro software to cover the whole network with Tor and exclude the Tor browser from the software. This way the two software will not interfere with each other.

However, it is also important to realize that the security of Tor on Android is very weak anyway. Remember, it is highly recommended to use it with Hardened // Security Step 3!

# Hardened // Security Step 5 : Daily Browsing/Anonymous
I'm going to use Whonix's distinction between pseudonymity and anonymity here. In any case, you should use a profile to separate the two and not merge them together.

For example, for day-to-day browsing, you can only use a VPN on it, or not use a VPN tool. Because this identity means that you (the pseudonym) can know who you are. But not who you really are.

Anonymity. That means you can only use TOR on it, and you can't use your pseudonym identity, including your account, on Anonymous. (No one knows who you are), which also corresponds to the phrase: what person nothing

Whonix is a compound of two words: who ("what person/s") and nix (a German word that means "nothing")


# Misperception/actualization clarification:
Everyone on this system thinks that you have to use Tor Browser/Tor related software to maximize the security/anonymity of the system. According to the official GrapheneOS statement, the lack of sandboxing in Tor/Firefox for Android creates an attack surface, including the fact that Firefox's sandboxing is weak, as described by the developers of the Whonix system.

Also, even using orbot/inviZible Pro to cover the entire system with Tor network is not a good idea, because of the following reasons: Fingerprint / DRM identification, the system mostly relies on profiles for solid security, isolation.


# Glossary:
Fingerprint: A fingerprint is the equivalent of a unique identification mechanism for the device. Once a threat/enemy has a fingerprint, they know 100% who that person is and what they are looking for. The theory applies in detail to cell phone software. Browsers. The way to avoid 100% fingerprint recognition in Graphene OS is to use the Tor browser, and all software should run on the Tor browser.

If you do install other software on your system, make sure it is 100% internet free. If it's a game, or any other software that requires internet access, there is a high chance that your fingerprints will be recognized by the other party.
