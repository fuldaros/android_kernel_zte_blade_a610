## ZTE Blade A610 3.18.19         
![ZTE Blade A610](http://s.4pda.to/kDjK89wYl0tNbeimUz0XyHvrxtNN0DwfXRh8p.jpg)

Codename - a610

Basic   | Spec Sheet
-------:|:-------------------------
CPU     | 1.3GHz Quad-Core MT6735
GPU     | ARM64
GPU     | Mali T720
Memory  | 2GB RAM
Android Version | 6.0.x/7.x.x
Storage | 16GB
Battery | 4000 mAh
Display | 5" 1280 x 720 px
Camera  | 13/5 MPx

## How make it?
 
# Create the necessary directories
    mkdir kernel/
    cd kernel/
# First you need to download the repository
    sudo apt install git
    git clone https://github.com/fuldaros/android_kernel_zte_blade_a610.git
# Set defconfig
    make O=out A610_defconfig
# Install and configure toolchain
    git clone https://android.googlesource.com/platform/prebuilts/gcc/linux-x86/aarch64/aarch64-linux-android-4.9
    export CROSS_COMPILE=~/kernel/aarch64-linux-android-4.9/bin/aarch64-linux-android-
# Configure compilation
    export ARCH=arm64
# Compile
    make -jX O=out Image.gz-dtb
("X"-number of threads)
## Proffit!
