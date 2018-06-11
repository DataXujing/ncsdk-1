# Intel® Movidius™ Neural Compute SDK
This Intel® Movidius™ Neural Compute software developer kit (NCSDK) is provided for users of the [Intel® Movidius™ Neural Compute Stick](https://developer.movidius.com/) (Intel® Movidius™ NCS). It includes software tools, an API, and examples, so developers can create software that takes advantage of the accelerated neural network capability provided by the Intel Movidius NCS hardware.

 
# Installation
The provided Makefile helps with installation. Clone this repository and then run the following command to install the NCSDK:

```
make install
```

# Examples
The Neural Compute SDK also includes examples. After cloning and running 'make install,' run the following command to install the examples:
```
make examples
```

## NCAPPZOO Examples
For additional examples, please see the Neural Compute App Zoo available at [http://www.github.com/movidius/ncappzoo](http://www.github.com/movidius/ncappzoo). The ncappzoo is a valuable resource for NCS users and includes community developed applications and neural networks for the NCS.

# Documentation
The complete Intel Movidius Neural Compute SDK documentation can be viewed at [https://movidius.github.io/ncsdk/](https://movidius.github.io/ncsdk/)

# Getting Started Video
For installation and general instructions to get started with the NCSDK, take a look at this [video](https://www.youtube.com/watch?v=fESFVNcQVVA)

# Troubleshooting and Tech Support
Be sure to check the [NCS Troubleshooting Guide](https://ncsforum.movidius.com/discussion/370/intel-ncs-troubleshooting-help-and-guidelines#latest) if you run into any issues with the NCS or NCSDK.

Also for general tech support issues the [NCS User Forum](https://developer.movidius.com/forums) is recommended and contains community discussions on many issues and resolutions.

# WINDOWS SUPPORT
The api/winsrc is a WINDOWS support project. You can compile it on VS2017. Tested on Windows 10.
To use it, you need:
1. Visual Studio 2017 with C++ and you must also have intalled C++ "Windows 10 SDK (10.0.15063.0)" and "Visual Studio Platform Toolset v141)
2. Compile project located in folder api\winsrc\ on VS2017 (I have compiled it in 32bit/x86, and it can be compiled as "Debug" or "Release")
3. You need also Python3, e.g. python 3.6.5, you can download it from: https://www.python.org/downloads/release/python-365/   (32bit version, if you have compiled library in 32bit/x86)
4. Download https://zadig.akeo.ie/downloads/zadig-2.3.exe
5. In python run directory you must copy following files:
	- libmvnc.dll (from folder: api\winsrc\Release\ or api\winsrc\Debug\)
	- libusb-1.0.dll (from folder: api\winsrc\libusb\lib\MS32\dll\ if you have compiled library in 32bit)
	- all "pthread" dlls (from folder: api\winsrc\pthread\dll\x86\ if you have compiled library in 32bit)
	- folder "mvnc" (from folder: api\winsrc\src\)
	- hello_ncs.py (from folder: "examples\apps\hello_ncs_py\"
6. Copy folder "mvnc" located in "python" to your PYTHON_LIBRARY path, e.g. "C:\Python3\Lib\"
7. Run "hello" script by using cmd: python.exe hello_ncs.py
	(if some python library will be missing then you must install it, e.g. "numpy", you can install "numpy" by using cmd: python.exe -m pip install numpy
	 of oourse if any other python libraries will be missing you must also install them by using pip).
8. During first run you must install the WINUSB driver by using zadig-2.3.exe, when your first call OpenDevice over. Because there a new device will be found. This driver must be installed for device: "VSC Loopback Device"!

ENJOY it!