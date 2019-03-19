# Nvidia drivers on Ubuntu

### Series and versioning
Nvidia releases graphics drivers in a particular way: There are several driver _series_, which focus on supporting certain hardware generations, and providing certain feature sets for these. Higher series numbers indicate support for newer hardware and newer features.

These driver series are _versioned_. Newer versions provide bug fixes and improved support with specific applications.

A typical driver release combines series and version number, separated by a dot, e.g. _418.43_.

### How to choose the right driver for my hardware?

To determine which driver is suitable for a particular graphics card model, two web searches are available:
 
* [Recommended driver](https://www.nvidia.com/Download/index.aspx?lang=en-us)
* [List of compatible drivers](https://www.geforce.com/drivers) - limited to GeForce hardware, may be incomplete

The latest driver series and versions Nvidia provides for Linux are listed at https://www.nvidia.com/object/unix.html

### How to install drivers?

Drivers should not be downloaded from Nvidia and used directly on Ubuntu. Instead, Ubuntu provides repackaged (and patched?) variants of these drivers. Some of these drivers are available in the fully supported _restricted_ section of the Ubuntu archive repository (enabled by default), newer ones are available in the unsupported [graphics-drivers PPA](https://launchpad.net/~graphics-drivers/+archive/ubuntu/ppa). In current Ubuntu releases (18.04 LTS and newer) Nvidia drivers are packaged as _nvidia-driver-SERIES_, e.g. _nvidia-driver-390_. 

The `ubuntu-drivers` utility can be used to automatically select a matching driver - with recent hardware, configure the graphics-drivers PPA beforehand.
