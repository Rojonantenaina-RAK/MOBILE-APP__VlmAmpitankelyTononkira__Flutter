## 1 - Pre-Requis
```bash
sudo apt-get update -y && sudo apt-get upgrade -y;
sudo apt-get install -y curl git unzip xz-utils zip libglu1-mesa

sudo apt-get install libc6:amd64 libstdc++6:amd64 lib32z1 libbz2-1.0:amd64
```

- Install [Android Studio](https://developer.android.com/studio/install#linux) and [VS Code](https://code.visualstudio.com/docs/setup/linux)

## 2 - Activate KVM Acceleration
- (for a better performance of our Emulator)

```bash
sudo apt-get install cpu-checker
egrep -c '(vmx|svm)' /proc/cpuinfo
```

```bash
sudo kvm-ok
```

```
INFO: /dev/kvm exists
KVM acceleration can be used
---
Otherwise,
INFO: Your CPU does not support KVM extensions
KVM acceleration can NOT be used
```

## 3 - Download Flutter SDK bundle [here](https://storage.googleapis.com/flutter_infra_release/releases/stable/linux/flutter_linux_3.29.3-stable.tar.xz)
- Extract it and Add .flutter/bin to PATH

## 4 - Install Flutter extension on AndroidStudio and then 'Create Flutter Project'

## 5 - Fix

```bash
flutter config --android-sdk ~/Downloads/Android
```
```bash
# To be added on .bashrc
export ANDROID_SDK_ROOT=~/Downloads/Android
export PATH=$PATH:$ANDROID_SDK_ROOT/platform-tools
export PATH=$PATH:$ANDROID_SDK_ROOT/emulator
export PATH=$PATH:$ANDROID_SDK_ROOT/tools
export PATH=$PATH:$ANDROID_SDK_ROOT/tools/bin

```

```bash
# Accept licenses
flutter doctor --android-licenses

# See if everything is ok
flutter doctor
```
