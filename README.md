# RPCS3-on-Linux-in-Termux-with-Box64-and-Ubuntu
RPCS3 on Linux in Termux with Box64 and Ubuntu is a project that enables PlayStation 3 emulation on Android devices by utilizing Termux and Box64. This repository offers a detailed guide for setting up the RPCS3 emulator within an Ubuntu environment, allowing users to play their favorite PS3 games on the go.

## Overview 

1) Termux: A powerful terminal emulator for Android.

2) Box64: A dynamic translator to run x86_64 binaries on ARM64 systems.

3) RPCS3: A PlayStation 3 emulator.

This setup allows you to run RPCS3 on Android via Termux by creating an Ubuntu environment and using Box64 for x86_64 emulation.

## Prerequisites

1) An ARM64 Android device

2) Termux installed on your device (download it from F-Droid or the Termux GitHub page)

## Installation

1. Install Termux

Download and install the Termux app from F-Droid or its GitHub releases.

2.Install Proot-Distro: If you haven't installed it yet, run the following command in Termux:

bash:pkg install proot-distro

3.Install Ubuntu: Set up Ubuntu using proot-distro:

bash: proot-distro install ubuntu
proot-distro login ubuntu

4.Update and Upgrade Ubuntu: Inside the Ubuntu shell, update and upgrade your packages:

bash: apt update && apt upgrade -y

5.Install Box64: You need to install Box64, which allows you to run 64-bit applications on ARM. You can clone the Box64 repository and build it from source:

bash: git clone https://github.com/ptitSeb/box64.git
cd box64
mkdir build && cd build
cmake .. -DARM64=ON
make
sudo make install

6.Download RPCS3: Now, download the RPCS3 emulator from the official website:

bash: wget https://github.com/RPCS3/rpcs3-binaries/releases/latest/download/rpcs3-linux-x86_64.AppImage
chmod +x rpcs3-linux-x86_64.AppImage

7.Run RPCS3: You can run RPCS3 using Box64. Ensure you have the correct permissions to execute the AppImage file:

bash: ./rpcs3-linux-x86_64.AppImage

## Additional Notes

1.Ensure your Android device has enough storage and performance capabilities to run RPCS3, as it is a demanding emulator.

2.You might encounter additional dependencies or issues depending on your specific device and Android version. Be prepared to troubleshoot as needed.

3.RPCS3 requires BIOS files from the PlayStation 3, which you download from other platforms.

## Required packages

 1. build-essential - Basic development tools.
cmake - Build system generator

2. libgl1-mesa-dev - OpenGL library.
libglu1-mesa-dev - OpenGL Utility Library.
libgtk-3-dev - GTK+ 3 for GUI applications.
libglib2.0-dev - GLib for low-level core library.

3. libsdl2-dev - SDL2 for handling audio, keyboard, mouse, and graphics.
libavcodec-dev - Audio/Video codec library.
libavformat-dev - Library for audio/video file format handling.
libavutil-dev - Utility functions for audio/video processing.

## Conclusion

This repository contains the setup and instructions for running the RPCS3 emulator on Linux using Box64 within an Ubuntu environment on Android. By leveraging the power of Box64, users can enjoy PlayStation 3 gaming experiences on their mobile devices.

### Key Features

- **Cross-Platform Compatibility**: Run RPCS3 on ARM devices with ease.
- **Performance Optimization**: Utilize Box64 to achieve improved performance on supported hardware.
- **User-Friendly Instructions**: Detailed steps to guide users through the installation process.

### Getting Started

To get started, follow the installation instructions provided in the repository. Ensure that all dependencies are installed and that your system meets the necessary requirements for optimal performance.

### Future Plans

- **Enhancements**: We plan to continuously improve the emulator performance and compatibility with more PS3 games.
- **Community Contributions**: Contributions from the community are welcomed to enhance this project further.
- **Documentation**: Ongoing efforts to improve the documentation and provide more examples and usage scenarios.

### Acknowledgments

Thank you to the RPCS3 team for their continuous development and support, as well as to the Box64 developers for providing the framework that makes this project possible. Your hard work and dedication to emulation technology inspire us all.
For any issues, suggestions, or contributions, please feel free to open an issue or submit a pull request.
Happy gaming!
