# N2KNMEA0183Wifi BMS Firmware UI

This is a UI for https://github.com/ieb/N2KNMEA0183Wifi which is uploaded to the device Firmware to give quick access on http://bloatsystems.local to monitor the BMS that the device is connected to. It was forked from https://github.com/ieb/N2KLifePo4 which is an install-able PWA App and which may evolve beyond what cna reasonably be accommodated in Flash. This version has a service worker as is required by a PWA, however due so size limitations the PWA manifest is lacking some images that cause Chrome to refuse to install.


Most of the code is shared with the lifepo4 PWA, however D3JS has been optimized and the ui is reactive so it works on Android and can be installed on a home screen for quickaccess.


# Install into Flash

Where possible the files are gzipped, as the Azyng web server code supports serving from flash gzipped without decompression.

     ./initialiseFlash.sh

This will rebuild the disk image for flash and upload it over serial using pio.

    ./redeployUI.sh

This will process and upload the UI files over http without resetting the flash.


<div>
<img alt="UI" src="screenshots/Screenshot 2024-12-23 at 18.08.49.png" />
</div>

