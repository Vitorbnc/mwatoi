# About

**mwatoi** is a python based project which can automatically extract whatsapp chats from android devices and copies it to iphone backup.

*Note:* It can't copy media files.

This project was tested only in Windows.

# Prerequisites

1. python3
2. JRE
3. iTunes
4. USB Debugging enabled on Android Phone
5. Open WhatsApp on Android and create a local and a Google Drive backup of all chats prior to starting this process
6. Install WhatsApp on iPhone and enter the same phone number used in Android, skip iCloud restoration and open the app

# How to run

1. Install dependencies:

    `> pip install -r requirements.txt`
2. Connect Android Phone to Windows PC through USB and run `WhatsAppKeyDBExtract.bat` (by [p4r4d0x86](https://github.com/p4r4d0x86/WhatsApp-Key-DB-Extractor)).
    
    Follow these steps provided by [FabiML](https://forum.xda-developers.com/t/tool-whatsapp-key-db-extractor-crypt6-12-non-root-updated-october-2016.2770982/page-29#post-81902381):

    * Launch `WhatsAppKeyDBExtract.bat` found in the `WhatsApp-Key-DB-Extractor-4.7-E1.0` folder
    * Input Y to reboot the device
    * Once rebooted, unlock it (you should not find your WhatsApp app anymore) and press any key in `cmd`
    * Wait until the streamed install is done
    * Unlock again your phone
    * Prompted "WhatsApp has been updated" should be prompted in your phone, press continue
    * Search for WhatsApp in your phone and open it
    (A new prompt in your phone will say it's an outdated version of WhatsApp press ok, if it doesnt appear don't worry)
    * Press the adjust date and you will be sent to a Date & Time page, keep it open
    * Press any key in `cmd`
    * Select the option you prefer at the command window
    * Select full backup in your phone (without entering any password)
    * Restore WhatsApp and press any key
3. Copy the entire `extracted` folder and all its contents from `WhatsApp-Key-DB-Extractor-4.7-E1.0` to the root folder of this repository.

4. Start transfer process and follow on-screen instructions:

    `> python main.py`

# References

1. https://github.com/residentsummer/watoi
2. https://github.com/EliteAndroidApps/WhatsApp-Key-DB-Extractor
3. https://github.com/andreas-mausch/whatsapp-viewer
4. https://github.com/p4r4d0x86/WhatsApp-Key-DB-Extractor


# Notes
- Fully tested with Xperia XZ Premium (Android 9.0), Windows 10 x64, Python 3.10.2, JRE 8u331, iTunes 12.12.3.5 (from Microsoft Store)
- Change `iphone_backup_root_locs` in `main.py` to match your iTunes location if required
- If a specific WhatsApp chat crashes the app when opening, try swiping over it and marking messages as 'read'.
- Please make sure to take complete Google Drive backup before connecting your android device.
