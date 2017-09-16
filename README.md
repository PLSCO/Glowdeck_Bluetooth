# Glowdeck_Bluetooth
Tools for working with the Bluetooth module on the Glowdeck board


NOTES

•    You should already have uploaded the firmware and website bins to the Wifi module (see the README.txt file in the Wifi directory in this package) before starting this instruction set.

•    Updating the Bluetooth firmware (even via micro-USB) will take approximately 5-6 minutes to complete. Interrupting this process before it successfully completes could render your Bluetooth module permanently unusable. 
•    You do not need to follow the instructions in the Glowdeck directory if you successfully complete the steps outlined in both this and the Wifi folders (you can however refer to that folder in the future to perform a standalone update of the Glowdeck firmware).

INSTRUCTIONS

1.    If you have not done so already, install any/all files located in the “Prerequisites” sub-directory within this folder. If you are not sure whether you have already installed a prerequisite package, there is no harm in reinstalling it (and some packages will inform you that you already have the pertinent installation on your system). Following installation(s), if you are prompted to restart your computer, do so. 
2.    Unplug all cables from your board except the cable connecting the LCD (also be sure to leave your Wifi module attached). 
3.    While pressing and holding down the front button, connect power to the DC barrel jack in the back of your PCB (using the provided 12V power adapter) to startup in DFU/bootloader mode. 
4.    The LEDs will all turn on (in either red or blue), and you can depress the front button.

5.    Connect a micro-USB cable from the board’s micro-USB port (directly adjacent to the DC power jack in the back of your PCB) to a USB port on your Windows computer.

6.    Open an Explorer window (i.e. where you are able to see all of your computer’s hard drives and attached volumes), and you should see a new volume - either GLOWDECK_V1 or GLOWDECK_V2 - appear in the list. It will have the same appearance as if you just connected a USB thumb drive.

7.    In the same manner in which you would copy a file from your computer to a USB thumb drive, drag and drop the Glowdeck_V1.cpp.hex.bin file from this folder on to the GLOWDECK_VX drive. 
8.    Wait a few moments for the copy to complete, and then Glowdeck should exit DFU/bootloader mode and start running the new firmware.

9.    The LCD will prompt you to update the BC127 (the Bluetooth module) firmware. When you see this prompt (and not sooner), open the Bluetooth updater application by double clicking the “Melody DFU.exe” file (contained in this directory).


10.    Ensure the baud rate is set to 9600, and that the COM port matches the port Glowdeck is connected to on your computer. Then click Connect, and you should see version information for your Bluetooth module appear in the box on the left. If you get an error, your configuration is likely wrong (i.e. the incorrect COM port is selected) - try again.

11.    Click Choose File, and select the file “Melody_5_7_RC14.dfu” (contained in this directory). The right box should now display version information for this firmware file.

12.    Click Download, and Glowdeck’s LCD should indicate that you are now updating the Bluetooth module. Wait patienbtly until the Melody DFU application indicates Update Complete. Then press the right button on the PCB.

13.    You will now see a prompt to restart your board. Disconnect the micro-USB cable, then disconnect power. Reconnect power and the board will perform some initialization routines on its own. Once complete, power cycle your board one last time. You have successfully updated all of the modules on your board to their current state of development.

*The files in this package are not intended for public distribution. The firmware update procedure described herein should be followed exactly as-written, and only by persons with some degree of familiarity with embedded development.

**To apply an over-the-air update using Streams, open the app and connect to your board by selecting it under the “Devices” tab. Once connected, select “About” from the navigation pane, and then click the “Update Glowdeck Firmware” button. This process can take between 30 seconds and 6 minutes to complete. Do not interrupt the process - neither on your phone or on Glowdeck - until Glowdeck restarts on its own (even if your phone indicates the process is complete). If you have auto-lock enabled on your phone after a certain timeout, be sure to disable this, or keep your phone from auto-locking by occassionally tapping the screen to prevent it from idling during the update.

***To upload firmware to your board from a Windows 8 computer, you must first follow the one-time procedure described here:

Do not allow locations on removable drives to be added to libraries: http://j.mp/windows8fix

Please note that uploading firmware from a Mac computer - or trying to upload from a Mac     running Windows as a virtual machine (e.g. using VMWare) - is not supported at this time.

DISCLAIMER:
By proceeding to update or modify the firmware on the Glowdeck PCB (and/or on one of its constituent components/modules), you assume full responsibility for any resultant outcome. You acknowledge that one such outcome of a firmware modification/update can be the rendering of one or more modules of the Glowdeck PCB dysfunctional (whether temporary or permanent). Contact support@streams.io before proceeding and wait for a response if you have any questions.
