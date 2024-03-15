# ADS-B Aircraft Tracking with PiAware on Debian Linux

## Introduction
Track aircraft using an ADS-B antenna and PiAware software on a Raspberry Pi running Debian Linux.

## Equipment and Software Needed

- **Raspberry Pi** (Raspberry Pi 3 or later recommended)
- **MicroSD card** (minimum 8 GB)
- **ADS-B USB dongle** (e.g., FlightAware Pro Stick, RTL-SDR compatible device)
- **ADS-B antenna**
- **Debian Linux** (Raspbian or Raspberry Pi OS recommended)
- **PiAware software**

## Installation Steps

### 1. Prepare the Raspberry Pi
- Download and install the Raspberry Pi Imager from the [Raspberry Pi website](https://www.raspberrypi.org/downloads/).
- Use the Imager to write Raspberry Pi OS to the MicroSD card.
- Insert the MicroSD card into the Raspberry Pi, connect to monitor, keyboard, mouse, and power it up.

### 2. Install Dependencies
- Update the package lists and upgrade the packages by running the following commands in the shell:
  ```shell
  sudo apt-get update
  sudo apt-get upgrade

### 3. Install PiAware
- Download and install PiAware:
    ```shell
    wget https://flightaware.com/adsb/piaware/files/packages/piaware-repository_7.0_all.deb
    sudo dpkg -i piaware-repository_7.0_all.deb
    sudo apt-get update
    sudo apt-get install piaware
    ```

### 4. Install Dump1090
- Install Dump1090 for ADS-B data decoding:
    ```shell
    sudo apt-get install dump1090-fa
    ```

### 5. Configure Your Antenna and Receiver
- Connect the ADS-B antenna to the USB dongle and plug it into the Raspberry Pi.
- PiAware will automatically detect the dongle and start receiving data.

### 6. Verify the Installation
- Check PiAware status:
    ```shell
    sudo systemctl status piaware
    ```

### 7. Register Your Device with FlightAware (Optional)
- Claim your PiAware device on FlightAware to contribute data and track flights online.

## Post-Setup

- **Optimize Antenna Placement:** Ensure the antenna has a clear view of the sky.
- **Secure Your Raspberry Pi:** Change the default password and apply security measures.
- **Regular Updates:** Keep the system and PiAware updated.

With this setup, you can track aircraft in real-time using your Raspberry Pi and PiAware software, with the option to view data locally or on FlightAware's platform.
