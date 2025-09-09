# mantaray-pro-wireless
This repo contains the build instructions, firmware, and 3D printable files needed to build, understand and modify the Mantaray Pro Wireless keyboard.


Firmware notes:
 - For defining pins higher than D10, you must use &gpioX Y notation (i.e. P1.07 -> &gpio0 7)
 - ZMK revision is currently pinned at v0.03 to avoid breakages in the build by linking to main
 - to use NFC pins as GPIO, CONFIG_NFCT_PINS_AS_GPIOS=y is set in unified .conf
