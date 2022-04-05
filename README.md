# ExtPassword! v1.00

Copyright (c) 2019 - 2022 Nir Sofer

Web site: https://www.nirsoft.net/utils/external_drive_password_recovery.html

Description
===========

ExtPassword! is tool for Windows that allows you to recover passwords
stored on external drive plugged to your computer.
ExtPassword! can decrypt and extract multiple types of passwords and
essential information, including passwords of common Web browsers,
passwords of common email software, dialup/VPN passwords, wireless
network keys, Windows network credentials, Windows product key, Windows
security questions.

This tool might be useful if you have a disk with Windows operating
system that cannot boot anymore, but most files on this hard drive are
still accessible and you need to extract your passwords from it.

System Requirements And Limitations
===================================

* This tool works with any version of Windows, starting from Windows XP
  and up to Windows 11. Both 32-bit and 64-bit systems are supported.
  This is true for the running system and for the external disk.
* This tool is just a small standalone .exe file that you can run on
  any system without installing anything.
* Currently, this tool is designed to work with full disk only, and
  there is no option to choose specific folders to read.
* You must provide read access to important system files on the
  external drive that are needed to extract and decrypt the passwords,
  especially the user profiles folder (e.g: X:\Users ) and the Registry
  hives folder (e.g: X:\Windows\System32\Config )
  You may need to run ExtPassword! as Administrator (Ctrl+F11) in order
  to allow it to read the files.

Supported Software And Features
===============================

* Web Browsers: Chrome, Chrome Canary, Chromium, Microsoft Edge, Opera,
  Vivaldi, Yandex, Brave, Firefox, Sea Monkey, Pale Moon, Waterfox,
  Internet Explorer 11/10 (On Windows 10 only).
* Email Clients: Microsoft Outlook (2007 - 2019), Thunderbird, Windows
  Mail App of Windows 10 and Windows 11 (Only POP3/IMAP/SMTP/Exchange
  accounts).
* Dialup/VPN passwords of Windows operating system.
* Wireless network keys of Windows operating system.
* Windows Credential files ( %AppData%\Microsoft\Credentials ), which
  store passwords of remote computers on your network.
* Security questions of Windows 10 and Windows 11.
* If Microsoft account was used to login the external system, the
  ExtPassword! tool automatically tries to read and decrypt the Microsoft
  account cache file (located under
  C:\Windows\System32\config\systemprofile\AppData\Local\Microsoft\Windows\
  CloudAPCache\MicrosoftAccount ) and then use it to decrypt the
  DPAPI-encrypted passwords.
* On Windows 10 - ExtPassword! can decrypt DPAPI passwords without
  typing the login password if the TBAL Primary key entry is stored as
  LSA secret (The entry name is
  M$_MSV1_0_TBAL_PRIMARY_{22BE8E5B-58B3-4A87-BA71-41B0ECF3A9EA} ).
  Windows 10 creates this entry for the last user that turned off the
  computer.

How to use ExtPassword!
=======================

ExtPassword! doesn't require any installation process or additional dll
files. In order to start using it, simply run the executable file -
ExtPassword.exe
In order to ensure that ExtPassword! have read permission to all files
needed to decrypt the passwords on the external drive, it's recommended
to run ExtPassword! as Administrator. You can do it simply from Help menu
-> Run As Administrator. The is also 'Run As Administrator' button in the
Options window.

After running ExtPassword!, the Options window is displayed. You have to
choose the external drive that you want to scan. Optionally, type the
login passwords you used on this system (every password on separate
line). The login passwords are needed to decrypt some of the
DAPI-encrypted passwords. You can also type the SHA1 hash of the password
instead of the actual password.
If you used a master password to decrypt the passwords of Firefox or
other Mozilla products, you have to type your password in the master
password text-box.

After you fill the external drive information, press the OK button. After
you press the OK button, ExtPassword! scans the external drive and
displays the log on the main window. After the scanning process is
finished, ExtPassword! switches to passwords list mode to show you all
passwords and other information found on the external drive.

If you cannot find the password you need, you can try to switch to the
log screen by pressing F7, and try to figure out what is wrong.

In the passwords list mode, you can select one or more passwords (or
simply press Ctrl+A to select all of them) and then use the 'Save
Selected Items' option (Ctrl+S) to export them to
comma-delimited/tab-delimited/HTML/XML/JSON file. You can also copy the
selected passwords to the clipboard (Ctrl+C) and then paste them into
Excel or other spreadsheet application.

Translating ExtPassword! to other languages
===========================================

In order to translate ExtPassword! to other language, follow the
instructions below:
1. Run ExtPassword! with /savelangfile parameter:
   ExtPassword!.exe /savelangfile
   A file named ExtPassword_lng.ini will be created in the folder of
   ExtPassword! utility.
2. Open the created language file in Notepad or in any other text
   editor.
3. Translate all string entries to the desired language. Optionally,
   you can also add your name and/or a link to your Web site.
   (TranslatorName and TranslatorURL values) If you add this information,
   it'll be used in the 'About' window.
4. After you finish the translation, Run ExtPassword!, and all
   translated strings will be loaded from the language file.
   If you want to run ExtPassword! without the translation, simply rename
   the language file, or move it to another folder.

License
=======

This utility is released as freeware. You are allowed to freely
distribute this utility via CD-ROM, DVD, Internet, or in any other way,
as long as you don't charge anything for this and you don't sell it or
distribute it as a part of commercial product. If you distribute this
utility, you must include all files in the distribution package, without
any modification !

Disclaimer
==========

The software is provided "AS IS" without any warranty, either expressed
or implied, including, but not limited to, the implied warranties of
merchantability and fitness for a particular purpose. The author will not
be liable for any special, incidental, consequential or indirect damages
due to loss of data or any other reason.

Feedback
========

If you have any problem, suggestion, comment, or you found a bug in my
utility, you can send a message to support@nirsoft.net
