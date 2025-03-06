+++
date = '2025-03-06T20:18:27+05:30'
draft = false
title = 'Enable Bluetooth in Arch Based Distros'
+++

If Bluetooth is not working properly after installing an Arch-based Linux distribution like Arch Linux, EndeavourOS, or Manjaro, it may be due to the Bluetooth service not being enabled.

## Step 1: Verify the Bluetooth Package
Before enabling the Bluetooth service, ensure that the required Bluetooth protocol package (`bluez`) is installed. You can check for its presence using the following command:

```sh
pacman -Q bluez
```

If the package is not found, install it with:

```sh
sudo pacman -S bluez
```

## Step 2: Enable and Start the Bluetooth Service
Once `bluez` is installed, enable the Bluetooth service so that it starts automatically at boot:

```sh
sudo systemctl enable bluetooth.service
```

To start the Bluetooth service immediately without rebooting, run:

```sh
sudo systemctl start bluetooth.service
```

## Step 3: Install Additional Tools (Optional)
For better device management, you may also want to install `bluez-utils`, which provides essential utilities like `bluetoothctl`:

```sh
sudo pacman -S bluez-utils
```

## Step 4: Check Bluetooth Status
To confirm that Bluetooth is running correctly, use:

```sh
systemctl status bluetooth.service
```

If Bluetooth is still not working, consider checking whether your system has the appropriate firmware and drivers for your Bluetooth adapter.

By following these steps, you should be able to enable and use Bluetooth on your Arch-based Linux system without issues.


