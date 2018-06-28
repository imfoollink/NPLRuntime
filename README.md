### Install Guide

#### Environment Setup
- Install Visual Studio 2017
- Install CMake 3.11: ftp://10.0.1.201//home/ftp_default_user/NPL_SDK/DEVKIT/Mobile2/cmake-3.11.3-win64-x64.msi
- Install Android NDK r9d: ftp://10.0.1.201//home/ftp_default_user/NPL_SDK/DEVKIT/Mobile2/android-ndk-r9d-windows-x86_64.zip
- Install Android SDK: ftp://10.0.1.201//home/ftp_default_user/NPL_SDK/DEVKIT/Mobile2/android-studio-bundle-145.3330264-windows.exe
- Install Apache Ant: ftp://10.0.1.201//home/ftp_default_user/NPL_SDK/DEVKIT/Mobile/apache-ant-1.9.7-bin.zip
- Install JDK: ftp://10.0.1.201//home/ftp_default_user/NPL_SDK/DEVKIT/Mobile/jdk-8u102-windows-x64.exe
- Run Andoid SDK manager, make sure you have "Andorid SDK build tools"-"19.x" and "Android 4.4.2 (API 19)" installed.
- Extract boost to your local drive: ftp://10.0.1.201//home/ftp_default_user/NPL_SDK/DEVKIT/Mobile2/boost_1_65_1.rar
- Set environment variable: BOOST_ROOT to your boost root directory.
- Install nVidia Nsight for Tegra: ftp://10.0.1.201//home/ftp_default_user/NPL_SDK/DEVKIT/Mobile2/NVIDIA_Nsight_Tegra_Release_3.5.18065.5230.exe
- Open Vistual Studio, Nsight->Options..., Fill out NDK, SDK, etc. fields respectively.

#### Build
- Clone the project from: http://10.0.1.201/FrontEnd/NPLRuntime_truck_star
- Checkout truck_star_CP branch
- Run Cmake GUI
- "Where is the source code:" put your source code (NPLRuntime_truck_star project) path here
- "Where to build the binaries:" choose a SEPERATE(important!) path for binary outputs
- "Configure", "Specify the generator for this project", choose "Visual Studio 15 2017", check "Specify options for cross-compiling", "Next"
- Put "Android" in the "Operating System" field (which should be the first field), and leave the other fields empty or to their defaults.
- "Finish"
- Amongst cmake option list, Look for "NPLRUNTIME_LUAJIT21" and uncheck it (We will be using LuaJIT20 solely).
- After "Configure" finished, click "Generate" to generate a vistual studio solution for android.
- Open the generated solution with Visual Studio 2017, switch to "Debug" configuration and build.
- Make sure your android device have all developer options turned on and plug it to your pc, it should appear in visual stuidio "Device" UI automatically.
- Run "Nsight Tegra Debugger", the project should be fully debuggable now.
