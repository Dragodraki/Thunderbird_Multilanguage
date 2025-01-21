# <p align="center"> <i> Don't use! A major update will be released soon! </i>
<br>
<p align="center" <i> Planned: legacy version will be even more secure than current TB </i>
<p align="center" <i> NG anti phishing modules, corruption detector, ultrafast spell checkings and tidier UI</i>
<br>
-------------------------------
<br>
<br>
<br>
<br>

# Thunderbird_Multilanguage
This special Mozilla Thunderbird version 52.9.1 comes with some unique properties. <br/>
(Release Date: 22.07.2024, Publisher: Dragodraki alias Dreamland, Notice: fork of Mozilla Thunderbird) 
<br/>

[<img src="https://user-images.githubusercontent.com/76787321/197257488-1b7aa8e9-9b6f-4600-949e-8ff477cb4bf4.png" width="23%"></img>](https://github.com/Dragodraki/Thunderbird_Multilanguage/releases/latest/download/Thunderbird.52.9.1.32-Bit.multilingual.Spezialversion.exe)
<br>

-------------------------------
EXPLANATION
-------------------------------
Mozilla dropped support for older Windows like XP and 7 for a while now. Version 52.9.1 was an old version runs fine on all Windows versions since Windows XP. Yeah, its outdated and lacks of many security patches since then. But compared to Firefox, in Thunderbird by default the user will not interact with internet directly and the mail account is piped through the domain it belongs too. So the security risk is much less than in an actual browser.
So, everyone has to decide for themself, whether want to sacrifice a minor bit of security for an extreme stable and performant mail program like TB 52.9.1. Here are the main benefits of using it in general and of my special version in detail:

Thunderbird 52.9.1 - general benefits (over todays Thunderbird/Outlook):
+ It's soooooo less ressource consuming in CPU/RAM (e.g. 4GB RAM is enough)
+ XUL-based (native/legacy) addon support - you can even modify existing xpi files by extracting and re-packing them or create your own without any peermission from AMO or signature. Though it leaves room for security holes too, I admit, so please don't install Thunderbird to any other install location than "%ProgramFiles%" or "%ProgramFiles(x86)%"!
+ 52.9.1 is extremely crash-safe. Never found another version that is that like unimpressed by the amount of mails. Poeple often complain about Mozilla crashed due too a large amount of stored mails, no matter whether in inbox or any other (online or local) folder.
+ The dashboard contains relevant GUI elements only. In other words: It's not half as overcrowded as TB 115 or Microsoft Outlook (how the hell daily users should get comfy with todays Outlook, they're overwhelmed by register cards and menu butttons - not speaking of Outlook bugs). Even completely beginners can navigate through the legacy GUI of Thunderbird.

Thunderbird 52.9.1 - my special version benefits (over default 52.9.1):
+ Multilanguage support: Both, the mail client and the integrated addon "Lightning" contain 58 different preinstalled locales. By installing, the language will adapt to your system locale already but of course you are still able to switch to another one easily (Menu -> Add-ons -> Languages -> Change...) and offline without ethernet access.
+ Absolutely no telemetry to anyones server! THis version respects your privacy like no other version before. All consent/report settings are disabled by default (yes, also the invisible options you cannot access via GUI).
+ Filetype association were hevaily change in windows 10. Normally, the default setup is not able to set TB as default when installing on it and later Windows. This version is. By using SetUserFTA it uses Microsofts own algorithm to generate the unique hash value that is needed to make the set default program is actually used. Of course the native registry flags are also onboard to make filetype association working for windows XP and 7 too.
+ When setting up a nwe mail adress, TB by default shows a nagging screen offering Gandi (and some other) services you first have to decline to open the actual form. This version verboses the third party provider window.
+ A very very special tweak allows the addons to be repaired at every second start of Thunderbird. Normally your addons will be disabled if your TB version does not longer supports them and even if reopened by the old version they stay grayed out and all you are permitted to do is uninstalling them. I cannot avoid them to being disabled by using another Thunderbird version than mine. But: As soon you re-open your profile with my installed version, they will recover from their dispended state in the start after next. That means: If for whatever reason you use two different versions of Thunderbird on one system and using the same profile, with my version your grayed out addons will cure so you don't have to reinstall them. Ha, you can even have from both versions addons installed (addons and extensions) and the addons will work again once you open 52.9.1. All you have to do is lanching TB one time, immediately close it and relaunch now normal.
The reason for why it works has nothing to do with a feature but purely with a bug: In your installation folder in subfolder \defaults\pref\ the file "channel-prefs.js" contains the string "pref("extensions.databaseSchema", "ThisRepairsAllAddonsEachStart");". The type of extensions.databaseSchema should actually set to integer and tells Mozilla something about how addons are arranged. Cause I define this one as string, Mozilla is confused every time you open your mail client. Look at it like a visitor come to your street and search for your house number - instead of a house number I provide a nice metal plate with the word "Welcome". The visitor will be confused not finding the number to verify he's stands in front of the right house. What He'll do - he will watch his surroundings and count out the other houses with existing numbers on it. He re-creates the missing part by interact with his can be called "neighbours". Mozilla does the same here: It re-creates all addons state because of being confused by an integer value of addons architecture shows an unspoorted data type instead. And because of channel-prefs.js is loaded every call, addons will be repaired on every termination too. What next start of TB shows them again living and being enabled.
+ Calendar files (ics) import by double-click is not possible even with this special version, but at least send ics via mail will now get displayed correctly as attachment and can be imporrted in Lightning over the GUI. You have to download them first and then open the select menu on Lightning. Therefore the addon "Show F*cking Outlook Appointments" is preinstalled.
+ Ever had problems with winmail.dat and not knowing how to open that crap? Actually that file doesn't exist and is a result of attachments being not correctly coded by either the recipient (you) or the sender. Thanks to addon "LookOut".
+ Addon "FolderFlags" allows you to override the default folder type (trash/spam/inbox/outbox/etc.) to design your own custom folders.
+ Addon "Manually Sort Folder" allows you to change folder or mail address order. Native Thunderbird never implemented a feature to do so.
+ Addon "ConfirmBeforeDelete" adds a delete dialog to make sure you don't delete one or more mails by hitting ENTF unintentional.
+ The advantages of Addon "Simple Locale Switcher" are named above already but in detail this addon adds the "Switch" button in the addons languages page and the "Language" button in the custom toolbar. Only this way you are able to actually switch between the locale in GUI.
+ Two additional preinstalled themes are available which making it a total of three preinstalled. You can choose between the normal UI, a dark mode and the original colors from Thunderbird 3 which is only available in this special installer (not in the addon store).
+ Addon "Quartz Minerals" makes your mail client shows  transparent color in main windows menu bar. Since Windows 10 removed alpha-channel from window frames, the opacity works on Windows Vista/7/(8) only, but even in newer versions the mild turquoise color (what would be transparency in Windows Aero instead) is more eye-friendly than the default color.
+ Some other settings are also set. E.g. the Spam assistent is enabled by deault now, mails are allowed to be quarantined by your local installed Antivirus (which seems very important to me due to security measures) and some minor changes.

<br>

-------------------------------
LICENSE (FREEWARE)
-------------------------------
Permissions:
+ Private and Commcercial usage is allowed as long you don't demand money for it ;)
+ Forks are allowed, but they have to kept free of charge ;)
+ Free Distribution to friends or strangers is allowed, even wanted ;)

Limitations:
- Use the app at your own risk!
- Don't sell it as product or pretend to be its developer!
- Don't abuse it for malicious purposes!
<br>

-------------------------------
USAGE
-------------------------------
Just download the EXE file and install Thunderbird, you can install it over any existing version - it shouldn't create any conflict.
<br>
If you are a developer and want to inspect the source files, just extract the EXE file with a tool like WinRAR. Its a packed archive with Inno-Setup. Inside the extracted content navigate to {tmp}\Mozilla Thunderbird\.
<br><br>

-------------------------------
WINDOWS SUPPORT
-------------------------------
The support is the same as the default Thunderbird 52.9.1 and tested on the following Windows versions:

- Windows XP
- Windows Vista
- Windows 7
- Windows 8/8.1
- Windows 10
- Windows 11
<br>
<br>
