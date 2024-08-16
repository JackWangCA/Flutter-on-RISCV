# Welcome to Flutter on RISCV!

This project aims to migrate the Flutter SDK to RISC-V Architecture. Below is a preliminary tutorial on how to do it on your local machine. Please do let me know if there any issues by creating issues on Github. I will try my best to fix any issues that may arise. 

# What is needed

 - A RISC-V Machine (Virtual Machine also works)
 - A stable internet connection
 - About 20GB of storage



# Steps to get Flutter running on your machine

Please follow the steps below in order for Flutter SDK to run correctly.

## 1. Download the Flutter SDK

Currently, I have only tested this with Flutter SDK version 3.24.0. It is recommended that you use this version. But feel free to test this method on other versions as well.

    wget https://storage.googleapis.com/flutter_infra_release/releases/stable/linux/flutter_linux_3.24.0-stable.tar.xz
    tar -xvJf flutter_linux_3.24.0-stable.tar.xz
BTW, if any dependencies are missing, go ahead and get them installed and then run the commands again.

## 2. Download the Dart SDK

This is a precompiled Dart SDK for RISC-V. You can also try to make your own. I'll post some tutorials on that pretty soon.

    git clone https://github.com/JackWangCA/Flutter-on-RISCV.git
