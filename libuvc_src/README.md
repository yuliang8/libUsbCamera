`libuvc` is a cross-platform library for USB video devices, built atop `libusb`.
It enables fine-grained control over USB video devices exporting the standard USB Video Class
(UVC) interface, enabling developers to write drivers for previously unsupported devices,
or just access UVC devices in a generic fashion.

## Getting and Building libuvc

Prerequisites: You will need `libusb` and [CMake](http://www.cmake.org/) installed.

To build, you can just run these shell commands:

    git clone https://github.com/ktossell/libuvc
    cd libuvc
    mkdir build
    cd build
    cmake ..
    make && sudo make install

and you're set! If you want to change the build configuration, you can edit `CMakeCache.txt`
in the build directory, or use a CMake GUI to make the desired changes.

There is also `BUILD_EXAMPLE` and `BUILD_TEST` options to enable the compilation of `example` and `uvc_test` programs. To use them, replace the `cmake ..` command above with `cmake .. -DBUILD_TEST=ON -DBUILD_EXAMPLE=ON`.
Then you can start them with `./example` and `./uvc_test` respectively. Note that you need OpenCV to build the later (for displaying image).

## Developing with libuvc

The documentation for `libuvc` can currently be found at https://int80k.com/libuvc/doc/.

Happy hacking!


## 2019-09-19  
##  yuliang
## version:  0.0.2
## changeList:
## File:  stream.c
## Function:  uvc_get_still_ctrl_format_size(),
## Notes:     在成功执行之后，添加 ctrl->pStillCtrl = Still_ctrl;




