# TouchID-Settings-For-non-TouchID-devices

This hack will enable Touch ID settings for non-Touch ID devices running iOS 7.1.x up to iOS 8, and it also works on iOS 9 and iOS 10. I tested mine on iOS 9.3.5 on an iPod 5, but if you're on iOS 7 or iOS 8, you'll have a slightly different method to enable it (via Preferences.app, whereas iOS 9 and 10's is through the PreferencesUI.framework). This doesn't work on iOS 7.0-7.0.6 *yet* because the Touch ID/Passcode settings are located in Settings->General instead of right in Settings apps' root menu like on iOS 7.1.x, and there'll be a method for it to work on iOS 7.0-7.0.6 and below soon, just this is only working for iOS 7.1.x currently.

Again, this enables the Touch ID settings menu in the Settings app, and it'll work on all ARM32-bit and ARM64-bit devices like the iPhone 4, iPhone 4S, iPhone 5, iPhone 5C, iPad 2, iPad 3, iPad 4, iPad mini 1G, iPad mini 2G, iPad Air 1G, and iPod 5, and iPod 6 as long as they run iOS 7.1.x and above.

It was initially discovered on November 5, 2014, around 7:50-8:00 PM EST time, and edited on August 5, 2018 at 11:39:05 AM EST time. ;)



Before you begin, hear me out:

> So it'll be a Preferences.app (or PreferencesUI.framework if the device is on iOS 9 or iOS 10) plist edit via iFile (you can use SSH or AFC2, but this was done via iFile. So iFile is the recommended one.
> I cannot upload the Settings.plist because of copyright reasons, and because it could mess up your Settings layout even if I did upload it, so you have to do this manually, but it's *very* simple.

Disclaimer: I'm not responsible if you mess up. And please back up the Settings.plist in the Preferences.app or PreferencesUI.framework before attempting this, as well as your device in iTunes if you mess anything up. That's highly recommended.

You need iFile or AFC2 or OpenSSH before you attempt this! Install it in Cydia (iFile comes with a trial but it's worth it!)

**I HONESTLY ONLY CONDONE AND RECOMMEND THAT USERS TO ONLY USE IFILE - AND NOT SSH OR AFC2 - FOR NOW, AND JUST FOR THE RECORD!**

• Go in to /Applications/Preferences.app (iOS 9/10 users must navigate to /System/Library/PrivateFrameworks/PreferencesUI.framework),

• Find Settings.plist, then tap on the Settings.plist, hit Property List Viewer,

• In the plist file, navigate to the array—>go down to line 17 or line 18—>fill out the code like so: replace the detail that has PasscodeLockController with PSTouchIDPasscodeController, and replace the id with TOUCHID_PASSCODE instead of PASSCODE (for the record: The PSTouchIDPasscodeController gives access to the 5S/SE/6/6S/7/8's Touch ID section, not Passcode),

• Replace the iconCache with TouchID (no space) instead of Passcode.

• Save it, then close out of iFile, and then if the Settings app is opened, close and kill the Settings app, and re-launch the Settings app and in order for changes to take affect and be applied. You should then see the Touch ID & Passcode settings be displayed accordingly.
 
So that should help you get the Settings app (with no functionality at all and is just for looks and for play) to display Touch ID settings on a non-Touch ID device via this plist hack.

Demo: https://twitter.com/p0sin2018/status/1026122161226956802
