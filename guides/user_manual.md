## 1\. Welcome to the Mantaray Pro Wireless

Congratulations on your new Mantaray Pro Wireless\! This manual will guide you through the setup, features, and customization of your new keyboard to help you unlock its full potential.

Note: This manual is not an assembly guide for the Mantaray Pro Wireless DIY Edition. You can find the build guide [here](https://tuxedodevices.com/blogs/guides/mantaray-pro-wireless-diy-edition-build-guide).

* USB C Port  
* Power & Connection Status  
* Selected Bluetooth Profile  
* Active Layer  
* Nice\!View Display  
* Power Switch  
* LED (disabled by default to extend battery life)

## 2\. What's in the Box?

* Mantaray Pro Wireless (Pre-Assembled)  
  * Assembled Mantaray Pro Wireless Keyboard  
    * **If located outside the United States**, batteries will not be included with your order  
* Mantaray Pro Wireless DIY Edition  
  * Left & Right 3D printed case  
  * Left & Right PCBs  
  * 2 x XIAO nRF52840 Plus Microcontrollers  
  * 2 x 200mah LiPo Batteries   
    * **If located outside the United States**, batteries will not be included with your order  
  * 52 x Kailh Choc Hotswap Sockets  
  * 8 x Non-slip Rubber Feet  
  * 2 x nice\!view Displays \+ Headers  
  * 10 x M2 Screws  
  * 18 x M2 Heat Set Inserts  
  * (If Selected) 1 Set of Choc v1 Keycaps  
  * (If Selected) 52 x Kailh Choc v1 Switches

## 3\. Getting Started: First Use

**Note:** If you have the Mantaray Pro Wireless DIY Edition please follow the [build guide](https://tuxedodevices.com/blogs/guides/mantaray-pro-wireless-diy-edition-build-guide) before proceeding.

* Charging the Keyboard:  
  * Connect the included USB-C cable to the port on the back of the keyboard and plug the other end into a USB power source.  
  * A full charge takes approximately 2-3 hours and provides up to 21 days of battery life on the left board, and 3 months of battery on the right\*\*. These are estimates, and actual battery life is dependent on usage.  
* Powering On/Off:  
  * On Position: Up, toward the USB-C port  
  * Off Position: Down, toward the display  
  * Locate the power switch on the edges of the keyboard, near the display.  
  * Slide the switches to the "ON" position to turn on the boards.  
* Connecting to Your Device:  
  * Bluetooth   
    * Ensure Bluetooth is enabled on the device you wish to connect to.  
    * On your device, select "Mantaray Pro W" from the list of available Bluetooth devices. Follow any on-screen prompts to complete the pairing.  
    * **Pro Tip:** You can pair up to five different devices at a time. To switch between paired devices, simply press the corresponding L2 \+ Number key (e.g. L2 \+ 2).  
  * Wired (USB-C)  
    * Connect the left board to your computer using a USB-C cable.  
      * The keyboard will automatically switch to wired mode and begin charging.  
        * **WARNING:** Keeping a wireless keyboard plugged in constantly keeps its internal lithium battery at 100% – leading to accelerated degradation and increased fire risk. To stay safe, follow proper battery care practices, switch off, disconnect, or remove the battery when not using wireless mode.  
        * **Note:** The Mantaray Pro Wireless uses ZMK to facilitate communication between the board halves. The left half sends key presses directly to your computer via Bluetooth or USB, depending on how it’s currently connected. The right half sends keypresses to the left half, which then forwards them to the computer. Communication will always happen through the left side of the board. Because of this, **the left half may be used independently, and wired, while the right half relies on the presence of the left** half to facilitate communication. This is currently a limitation of ZMK.

## 4\. Bluetooth Profiles

You can use up to 5 Bluetooth profiles at a time, and switch between them to use your keyboard on different devices.

* Switching Profiles  
  * Press L2 \+ 1-5 to select a profile

## 4\. Keyboard Layout and Function Keys

**Base Layer**

**Symbol Layer**

**Media Layer**

* Indicator Light:  
  * An indicator LED is present near the USB-C port. It is disabled by default to maximize battery life; however, it can be enabled by customizing your device firmware via ZMK.

## 5\. Advanced Features and Customization

You can use the ZMK Studio web app to easily remap your keys, add new layers, and more.

* Key Remapping:  
  * Plug the left board into your computer  
  * In your browser, open [ZMK Studio](https://zmk.studio/)  
  * Click “USB”  
  * Select “Mantaray Pro W” from the list of available devices  
  * Remap your keys and add layers  
    * For more detailed information on using ZMK Studio, refer to the [official documentation](https://zmk.dev/docs/features/studio).

## 7\. Troubleshooting

Common Issues and Solutions:

### Keyboard Won't Connect

* Check that the keyboard is powered on.  
* Ensure the battery is charged.  
* Confirm the correct connection method is selected (Bluetooth or Wired).  
* Your Bluetooth pairing keys may be out of sync. You can **reset the Bluetooth pairing keys for all profiles by holding Q \+ P** for a few seconds.  
* Ensure no other devices are trying to connect to the keyboard.  
* Move the keyboard closer to your device.  
* Avoid placing large metal objects between the keyboard and your device.  
* Check for other wireless devices that may interfere with the signal. Wireless dongles and other Bluetooth devices may be the culprit.

### ZMK Studio Won't Connect

If ZMK Studio fails to connect to your keyboard, make sure:

- **The left half is powered off** via the power switch on the side of the unit
- **The left half is plugged into your computer** via USB-C
- **The keyboard is not connected to your computer via Bluetooth** — disconnect or forget "Mantaray Pro W" in your Bluetooth settings, or temporarily turn off Bluetooth on your computer
- **You are using Chrome or Edge** — Firefox and Safari do not support the WebSerial API required by ZMK Studio

## 8\. Safety and Maintenance

* General Safety Precautions:  
  * This product contains lithium batteries. Do not expose to extreme temperatures or liquids.  
* Cleaning Instructions:  
  * Clean with a soft, dry cloth. For stubborn dirt, use a small brush and a small amount of isopropyl alcohol. Always remove your battery before deep cleaning.  
* Battery Safety:  
  * Recharging your battery should only be done at 50ma, with an absolute maximum of 100ma. More than this may cause damage to your keyboard and/or battery.

## 9\. Contact and Support

* Contact Information:  
  * Customer Support Email: tuxedomakes@gmail.com  
  * [Contact Us Form](https://tuxedodevices.com/pages/contact)  
  * [Tuxedo Devices Discord](https://discord.gg/HABg37gjrd)
