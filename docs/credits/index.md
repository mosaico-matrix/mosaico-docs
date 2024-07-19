# Credits

## Developers
This project was developed by the following people:

- [murkrow](https://github.com/Murkrow02/): Project lead, developer

## Open source community ❤
This project wouldn't have been possible without the awesome open source community, here are some of the libraries and resources used in this project:

- [hzeller](https://github.com/hzeller/rpi-rgb-led-matrix): Huge shoutout to Henner Zeller for the awesome C++ library to control the LED matrix
- [Adafruit](https://learn.adafruit.com/adafruit-rgb-matrix-bonnet-for-raspberry-pi/overview): LED matrix bonnet and guide to set up the pi
- [Nlohmann JSON](https://github.com/nlohmann/json): Modern JSON library for C++
- [pybind11](https://github.com/pybind/pybind11): Amazing seamless operability between C++ and Python
- [aiocoap](https://github.com/chrysn/aiocoap): Python library to create COAP server
- [bless](https://github.com/kevincar/bless): Python library used to set up a simple GATT server with BLE
- [GitPython](https://github.com/gitpython-developers/GitPython): Python library to interact with git repositories
- [PixelArtIcons](https://github.com/halfmage/pixelarticons): Used in the app store with some widgets
- [Laravel](https://laravel.com/): PHP framework used to create the App Store API
- [Flutter](https://flutter.dev/): Framework used to create the mobile app

## Tools
- [Raspberry Pi](https://www.raspberrypi.org/): Used to control the LED matrix
- [Raspberry Pi cross-compiler](https://github.com/tttapa/docker-arm-cross-toolchain/): Used to compile the C++ code for the Raspberry Pi without needing to wait for hours
- [Android Studio](https://developer.android.com/studio): Used to develop the Android app
- [PHPStorm](https://www.jetbrains.com/phpstorm/): Used to develop the App Store API
- [CLion](https://www.jetbrains.com/clion/): Used to develop the LED matrix controller
- [PyCharm](https://www.jetbrains.com/pycharm/): Used to develop the networking module
- [Docker](https://www.docker.com/): Simplified the development and deployment process by containerizing the app store API
- [ChatGPT](https://chat.openai.com/): Helped me a lot to learn flutter and python
- [SQLite](https://www.sqlite.org/index.html): Used to store the data in the networking module

## Why Flutter?
This is the first time I've used Flutter, and I must say I'm impressed.
The development process is smooth, hot-reload is a game-changer, the pub.dev ecosystem is rich, and the community is very active.
I've always been able to find a package that does what I need, and when I couldn't, I was able to write my own without too much hassle.

I found it really easy to create a beautiful and responsive UI, the only steep learning curve was the state management, at first I used
the standard `setState` of the `StatefulWidget` but then I switched to `Provider` and `ChangeNotifier` to keep the UI code totally separated from the business logic.
Using the `Provider` package also allowed me to move the providers I needed in both the mobile app and the IDE to the shared library, so I could reuse them in both projects without duplicating code.


