### USB device experiments with the RPi Zero W 2
Much of this was taken from: https://www.collabora.com/news-and-blog/blog/2019/02/18/modern-usb-gadget-on-linux-and-how-to-integrate-it-with-systemd-part-1/

#### Install dependencies on pi zero
    sudo apt install git build-essential autoconf libtool libconfig-dev cmake

#### Install helpers to make configfs on boot easier
    git clone https://github.com/linux-usb-gadgets/libusbgx.git
    cd libusbgx
    autoreconf -i
    ./configure
    make
    make doxygen-doc [optional]
    sudo make install

    git clone https://github.com/linux-usb-gadgets/gt.git
    # Patch gt to remove dependency to create man page.
    # In gt/source/CMakeLists.txt comment out 
    # ADD_SUBDIRECTORY(manpages)
    mkdir -p gt/build
    cd gt build
    cmake ../
    make
    sudo make install
   
#### Add overlay for USB device in boot.txt

#### Load modules in cmdline.txt

#### Mount configfs using fstab on boot

#### Create service to start gadget when UDC is available

#### Create scheme for each composite device supported
