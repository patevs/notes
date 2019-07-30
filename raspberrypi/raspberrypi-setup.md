
# Raspberry Pi Setup

> The `Raspberry Pi` is a low cost, credit-card sized computer that plugs into a computer monitor or TV, and uses a standard keyboard and mouse. [What is Raspberry Pi](https://www.raspberrypi.org/help/what-%20is-a-raspberry-pi/)

- [Raspberry Pi Website](https://www.raspberrypi.org/)

---

## Links & Resources

Downloads:

- [Raspberry Pi Downloads](https://www.raspberrypi.org/downloads/)
  - [NOOBS Download](https://www.raspberrypi.org/downloads/noobs/)
  - [Raspbian Download](https://www.raspberrypi.org/downloads/raspbian/)

Documentation:

- [NOOBS Documentation](https://github.com/raspberrypi/noobs/blob/master/README.md)
- [Raspbian Documenation](http://raspbian.org/)

Tools:

- [SD Memory Card Formatter](https://chocolatey.org/packages/sdformatter)
- [balenaEtcher](https://chocolatey.org/packages/etcher)

---

## Installation

- [Installing OS Images](https://www.raspberrypi.org/documentation/installation/installing-images/README.md)
  - [NOOBS Install](https://www.raspberrypi.org/documentation/installation/noobs.md)
  - [Ubuntu Server Install](https://ubuntu.com/download/iot/raspberry-pi-2-3)
- [Installing with Windows](https://www.raspberrypi.org/documentation/installation/installing-images/windows.md)

### How to Automatically Install an OS

Even if you are using your Pi without a display, you can still use NOOBS to easily install an OS of your choice. To set up NOOBS to automatically and silently (i.e. without requiring any user input) install a specific OS, follow these steps:

1. Copy the OS folder for the OS you want to install into the `/os` dir (or alternatively delete all other OSes contained in the `/os` dir so that only your chosen OS remains.

2. If the OS you want to automatically install has multiple flavours available, edit the `flavours.json` file so that it only contains the flavour entry that you want to install.

3. Edit the `recovery.cmdline` file in the root NOOBS directory and append `silentinstall` to the arguments list.

When you now boot your Pi using an SD card containing the modified version of NOOBS that you just created, it will automatically install the OS you chose and boot into it after the installation has finished.

---

## Configuration

- [Raspberry Pi Configuration](https://www.raspberrypi.org/documentation/configuration/)

---

## Remote Access

- [Raspberry Pi Remote Access](https://www.raspberrypi.org/documentation/remote-access/)

---
