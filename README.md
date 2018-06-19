### Install Guide

#### Environment Setup
- Install CMake 3.11: ftp://10.0.1.201//home/ftp_default_user/NPL_SDK/DEVKIT/Mobile2/cmake-3.11.3-win64-x64.msi
- Install Android NDK r9d: ftp://10.0.1.201//home/ftp_default_user/NPL_SDK/DEVKIT/Mobile2/android-ndk-r9d-windows-x86_64.zip
- Install Android SDK: ftp://10.0.1.201//home/ftp_default_user/NPL_SDK/DEVKIT/Mobile2/android-studio-bundle-145.3330264-windows.exe
- Extract boost to your local drive: ftp://10.0.1.201//home/ftp_default_user/NPL_SDK/DEVKIT/Mobile2/boost_1_65_1.rar
- Set environment variable: BOOST_ROOT to your boost root directory.
- Install nVidia Nsight for Tegra: ftp://10.0.1.201//home/ftp_default_user/NPL_SDK/DEVKIT/Mobile2/NVIDIA_Nsight_Tegra_Release_3.5.18065.5230.exe
- Open Vistual Studio, Nsight->Options..., Fill out NDK, SDK, etc. fields respectively.

#### Build
- Clone the project from: http://10.0.1.201/FrontEnd/NPLRuntime_truck_star
- Checkout truck_star_CP branch
- Cmake, generate a vistual studio solution for android.
- Open the solution in visual studio and build Debug version.
