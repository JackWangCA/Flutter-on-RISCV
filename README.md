# Welcome to Flutter on RISCV!

This project aims to migrate the Flutter SDK to RISC-V Architecture. Below is a preliminary tutorial on how to do it on your local machine. Please do let me know if there any issues by creating issues on Github. I will try my best to fix any issues that may arise. 

# What is needed

 - A RISC-V Machine (Virtual Machine also works)
 - A stable internet connection
 - At least 20GB of storage

# What works and what doesn't

Right now, this is just a preliminary build and not everything works. Certain commands are tested and are working correctly while some are not. Commands that are not listed here and currently not tested. If you run into any issues, please do let me know. :) Thanks!

## Working

 - `flutter help`
 - `flutter doctor`
 - `flutter channel`
 - `flutter clean`
 - `flutter create`
 - `flutter pub`

Tested and works

## Not working

 - `flutter run`

flutter run would run into an error due to an unmatched version of Dart SDK and Flutter SDK. I will post an updated version of the precompiled Dart SDK when I resolve this issue. Please repeat step 2 and step 5 in the tutorial below and run this command again when I post the update.
 


# Steps to get Flutter running on your machine

Please follow the steps below in order for Flutter SDK to run correctly.

## 1. Download the Flutter SDK

Currently, I have only tested this with Flutter SDK version 3.24.0. It is recommended that you use this version. But feel free to test this method on other versions as well.

    wget https://storage.googleapis.com/flutter_infra_release/releases/stable/linux/flutter_linux_3.24.2-stable.tar.xz
    tar -xvJf flutter_linux_3.24.2-stable.tar.xz
BTW, if any dependencies are missing, go ahead and get them installed and then run the commands again.

## 2. Download the Dart SDK

This is a precompiled Dart SDK for RISC-V. You can also try to make your own. I'll post some tutorials on that pretty soon.

    git clone https://github.com/JackWangCA/Flutter-on-RISCV.git

## 3. Set $PATH for Flutter SDK

Go into your path and add flutter/bin, this makes sure that Flutter commands are recognized. It would also be a good idea to add dart-sdk/bin to your path as well.

## 4. Run some Flutter command

Run any flutter command so it downloads the Dart SDK files that it needs. Ex. `flutter doctor`

## 5. Replace the Dart SDK with the precompiled one 
Now go ahead and replace the Dart SDK in the Flutter SDK with the one that you have just downloaded by running these commands

    cp -r /root/dart-sdk/bin/* /root/flutter/bin/cache/dart-sdk/bin/
    cp -r /root/dart-sdk/dart /root/flutter/bin/
If the paths to the SDKs are different on your machine, please make the respective changes to the commands above.

## 6. Done!
Now you should be able to run Flutter commands. There may still be dependencies that you may need ton install but not listed here. Please go ahead and install them and run the commands that failed again.


# Thanks

 
