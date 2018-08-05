# TouchID-Settings-For-non-TouchID-devices

This hack will enable Touch ID settings for a non-Touch ID devices running iOS 7.0.x up to iOS 8, also works on iOS 9 and iOS 10, just with a slightly different way. I tested mine on iOS 9.3.5 on an iPod 5, but if you're on iOS 7 or iOS 8, you'll have a slightly different method (via Preferences.app, whereas iOS 9 and 10's is through the PreferencesUI.framework).

This enables the Touch ID settings menu in the Settings app on all ARM32-bit devices, and a few ARM64-bit devices. It was initially discovered on November 5, 2014, around 7:50-8:00 PM EST time. ;)



Before you begin, hear me out:

> So it'll be a Preferences.app (or PreferencesUI.framework if the device is on iOS 9 or iOS 10) plist edit via iFile (you can use SSH or AFC2, but this was done via iFile. So iFile is the recommended one.
> I cannot upload the Settings.plist because of copyright reasons, and because it could mess up your Settings layout even if I did upload it, so you have to do this manually, but it's *very* simple.

Disclaimer: I'm not responsible if you mess up. And please back up the Settings.plist in the Preferences.app or PreferencesUI.framework before attempting this, as well as your device in iTunes if you mess anything up. That's highly recommended.

You need iFile or AFC2 or OpenSSH before you attempt this! Install it in Cydia (iFile comes with a trial but it's worth it!)

• 1: Go in to /Applications/Preferences.app (iOS 9/10 users must navigate to /System/Library/PrivateFrameworks/PreferencesUI.framework),
• 2: Find Settings.plist, then tap on the Settings.plist, hit Property List Viewer.
• 3: In the plist file, navigate to the array—>scroll down to 17—>fill out like so: detail: PasscodeLockController to NO, so replace it with PSTouchIDPasscodeController, not Passcode. (for the record: The PSTouchIDPasscodeController gives access to the 5S's Touch ID section, not Passcode, obviously; only giving you access to Passcode's section).
• 4: Replace the iconCache with TouchID (no space) instead of Passcode.
 
That should help you get the Settings app (with no functionality at all and is just for looks and for play) to display Touch ID settings on a non-Touch ID device via this plist hack.
