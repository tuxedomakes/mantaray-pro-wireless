# mantaray-pro-wireless
This repo contains the build instructions, firmware, and 3D printable files needed to build, understand and modify the Mantaray Pro Wireless keyboard.


Firmware notes:
 - For defining pins higher than D10, you must use &gpioX Y notation (i.e. P1.07 -> &gpio0 7)
 - ZMK revision is currently pinned at v0.03 to avoid breakages in the build by linking to main
 - to use NFC pins as GPIO, CONFIG_NFCT_PINS_AS_GPIOS=y is set in unified .conf


BEGIN DOCUMENTATION

# Mantaray Pro Wireless

*Ergonomic. Compact. Portable. Hackable. Damn.*

TODO: Add KB image here

## Introduction

If you've found your way here: congratulations! Your desk is about to get a serious upgrade.

The Mantaray Pro Wireless is a unbody, split-ergonomic keyboard designed for a comfortable, flexible typing experience. Inspired by feedback on my open-source unibody wired Mantaray keyboard, the Mantaray Wireless Pro version is enhanced with split wireless freedom, dual displays, and a focus on hackable modularity and future upgrade paths (more on that later).

This board comes in two versions: fully assembled, and a DIY Edition (kit).
- The assembled version is exactly what it sounds like - the keyboard is fully assembled and ready to use (note: if you opted to not add switches and keycaps with your purchase, you will need to "install" these. Don't worry, the keyboard is hot-swappable, making installation a breeze!)
- The DIY Edition kit is perfect for hobbyists and first-time builders alike. Our comprehensive build guide makes the assembly process as simple as possible. Please read through the build guide before ordering to ensure you're comfortable with the build process.

## Key Features

* **Wireless Freedom:** Powered by ZMK firmware, wireless flexibility is included out of the box.
* **Insane Battery Life:** Go for weeks, even months, on a single charge. Expect up to **20 days** on the main left half and **3 months** on the right half with the included 200mAh batteries. Battery life will vary depending on usage.
* **Dual `nice!view` Displays:** Two crisp, power-sipping MIP displays give you critical info at a glance: current layer, connectivity status, battery levels, and more.
* **Hackable & Modular:** Exposed I2C headers on the PCB let you add new functionality like a scroll wheel, trackball, or macro pad to your board. The platform is open for you to design and build your own creations. We have some exciting features planned for the future that will utilize this functionality, so be sure to sign up for our newsletter (no spam, no BS, just awesome updates when we have something new to share).
* **Travel Ready:** A built-in battery cutoff switch ensures the keyboard won't wake up and start typing from inside your backpack.
* **Limitless Mounting Options:** Four threaded inserts on the base allow you to mount the keyboard to anything you can imagine - tripods, MagSafe-compatible stands, or custom tenting legs.
* **Low-Profile Ergonomics:** A column-staggered layout promotes natural hand and wrist posture, all housed in a sleek case designed for low profile Kailh Choc V1 switches and keycaps.
* **Hot-Swappable:** No soldering required for switch swaps! Easily install and experiment with different Kailh Choc V1 switches to find your perfect feel.
* **Customization Without Code:** ZMK Studio support allows you to remap keys and create macros through a powerful web-based UI, with no coding required. If you want more control, dive into the ZMK firmware docs to customize your keeb.

# DIY Edition
<details>
 <summary>
  DIY Edition
 </summary>
 ## What's in the Box?

* 1 x Mantaray Pro Wireless PCB Set
* 1 x 3D Printed Case + Plate Set
* 52 x Kailh Choc Hot-Swap Sockets
* 2 x `XIAO nRF52840 Plus` Wireless Controllers
* 2 x `nice!view` MIP Displays
* 2 x Rechargeable LiPo Batteries (200mah, 402030)
* All necessary diodes, screws, and standoffs for assembly
* 4 x Non-slip Silicone Rubber Feet
* Note: The diodes, battery connector, and power slider are already soldered for you.

## What You'll Need to Complete Your Build

This is a DIY kit. You will need to source the following components:

* **52 x Kailh Choc V1 Switches:** Choose your preferred type (e.g., Red, Brown, White).
* **52 x Kailh Choc V1 Keycaps.** Be sure to get caps that utilize choc spacing (18mm x 17mm). MX spaced caps (19mm x 19mm) are not compatible.
* **Soldering Iron & Solder:** Required for soldering controllers, displays, and sockets.
* **Basic Tools:** A small screwdriver, flush cutters, and (optionally) tweezers.

## Build Guide

TODO: Add link to video guide on YouTube

**Step 1: Solder Controllers**

NOTE: Before you install your microcontroller, it would be wise to test that it works. While we do test the microcontrollers before shipping them to you, once they're soldered to the board they are time consuming to remove if something goes wrong (if using a hotplate and low-temperature solder, this process is easier).

TODO: add assembly step images

**Step 2: Solder Hotswap Sockets**

Place the hotswap sockets on the front of the PCB and solder them from the back. This step is straightforward but requires patience.

TODO: add assembly step images

**Step 3: Solder the Displays**

**Be sure to solder the displays as straight as possible**, the tolerances on the top case are very tight, and your display needs to be positioned precicely. Seriously, take your time on this step.

Solder the headers for your two `nice!view` displays. To maintain a low profile and protect your battery from punctures, solder the bottom of the headers flush to the bottom of the PCB. Using some tape to hold things in place is helpful here. Once you have soldered all 5 header pins in place, remove the black plastic piece that held the headers together (if you fail to do so, the display will not sit flush on the PCB. This step is required).

With the plastic spacer removed, place your display onto the header pins and solder them from the top. You ensured proper alignment, right? Just checking. With the display soldered, use some flush cutters to cut those headers as flush as possible.

TODO: add assembly step images

**Step 4: Test that everything works**

Your hotswap sockets, display, and microcontroller are in place. Now is a good time to pop in some switches and ensure that the keyboard is working. Connect your PCB to a computer using a USB cable (it's recommended to avoid using the battery just yet), and verify that your display works, and that keypresses are being recognized (you may need to pair your keyboard via bluetooth. See bluetooth pairing section for instructions on completing this process). Once you've confirmed everything is working, remove all your switches, then proceed to the next step.

TODO: add assembly step images
TODO: add bluetooth pairing section reference

**Step 5: Assemble the Case**

Install the head set inserts into the bottom plate now. Thee are 5 located on the inside of the bottom case that are used to mount the PCB, and 4 on the bottom that are used to attach mounting and tenting accessories. You can use a soldering iron with a small tip for this. I've found a temperature of ~420 degrees fahrenheit works well.

Screw the fully assembled PCB into the case using the provided M2 screws. Place the top case over the PCB, ensuring the displays align with their cutouts. The top case uses a snap fit to secure it in place, so take your time and firmly (but gently) press on all sides of the top case to snap it to the bottom case.

**Step 6: Install Switches and Keycaps**

Carefully press your Kailh Choc V1 switches into the hotswap sockets. Watch for bent pins. Once all switches are installed, add your keycaps.

TODO: add assembly step images

**Step 7: Connect Batteries & Flash Firmware**
WARNING: Take this seriously. Wrong battery polarity can, at best, brick your PCB or microcontroller. At worst, it can cause a fire or explosion. Be absolutely sure the polarity of your battery is correct before inserting it. Refer to the image below for the expected polarity of the battery.

Connect the LiPo batteries to the battery connector on the PCB.

TODO: add assembly step images
TODO: add more safety information and warning callouts

## Firmware

The Mantaray Pro Wireless runs on the powerful open-source ZMK firmware.

**How to Flash:**
1.  Download the pre-compiled `.uf2` firmware file from this repository.
2.  Connect one half of the keyboard to your computer via USB-C.
3.  Enter the bootloader by double-tapping the "Reset" button on the `nice!nano` controller.
4.  A removable drive named "NICENANO" should appear on your computer.
5.  Drag and drop the firmware file onto the removable drive.
6.  The keyboard will reboot with the new firmware. Repeat for the other half.

**Customization:**
For easy keymap customization without any coding, visit [ZMK Studio](https://studio.zmk.dev/). For advanced configuration, you can fork the ZMK firmware on GitHub and build it yourself.

## A Playground for Hackers

We designed this keyboard to be a platform for creativity.

* **Magnetic I2C Port:** The magnetic connector allows you to easily attach and detach I2C-compatible modules. We will be releasing official modules like trackballs and scroll wheels, but we encourage you to design and share your own!
* **Toggleable Pull-up Resistors:** A DIP switch on the bottom of the board enables or disables the I2C pull-up resistors. This ensures maximum compatibility with any module you might use—whether it's your own DIY creation or an official one.
* **Mounting Points:** The six threaded inserts on the base are your canvas. Design and 3D print your own tenting legs, mount the keyboard on a tripod, or attach it to a VESA mount.
</details>




## ❤️ Support ❤️

TODO: add support links to ko-fi, tindie, and website

## Disclaimer

This is a DIY electronics kit that requires soldering and assembly. While we provide a comprehensive build guide, purchasers should be comfortable with or willing to learn basic soldering. This project includes working with LiPo batteries. Know about the risk of improper battery usage before you begin. Due to the DIY nature of this product, returns cannot be accepted once assembly has begun.
