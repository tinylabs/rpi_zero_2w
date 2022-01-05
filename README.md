### USB device experiments with the RPi Zero W 2

#### Install dependencies on pi zero
    sudo apt install git build-essential autoconf libtool libconfig-dev cmake asciidoc

#### Install helpers to make configfs on boot easier
    git clone https://github.com/linux-usb-gadgets/libusbgx.git
    cd libusbgx
    autoreconf -i
    ./configure
    make
    make doxygen-doc [optional]
    sudo make install

    git clone https://github.com/linux-usb-gadgets/gt.git
    mkdir -p gt/build
    cd gt build
    cmake ../
    make
    
