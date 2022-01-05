# rpi_zero_2w
USB device experiments with the RPi Zero W 2

# Install dependencies on pi zero
$ sudo apt install git build-essential autoconf libtool libconfig-dev

# Install helpers to make configfs on boot easier
$ git clone https://github.com/linux-usb-gadgets/libusbgx.git
$ cd libusbgx
$ autoreconf -i
$ ./configure
$ make
$ make doxygen-doc [optional]
$ sudo make install

git clone https://github.com/linux-usb-gadgets/gt.git
