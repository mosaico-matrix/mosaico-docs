# Mosaico
Mosaico is a unique (Free and open source ❤️) platform that allows **users** and **developers** to create, share, and display custom widgets on a **LED matrix**. This ecosystem is composed of various applications working together to bring vibrant, customizable content to your Raspberry Pi-driven LED matrix.

## Introduction
Mosaico is designed to empower both users and developers by providing an open platform where custom Python widgets can be created and displayed on a LED matrix. Whether you want to show the time, weather, or your latest grocery list, Mosaico makes it easy to develop and deploy your ideas.

## Some examples of widgets:
- Display the current time and date.
```python 
from datetime import date
from mosaico import widget

# Get the current date
today = date.today()
d = today.strftime("%d")
m = today.strftime("%m")
y = today.strftime("%Y")

# Display on matrix
day_month = widget.createText()
day_month.setText(d + "-" + m)
year = widget.createText()
year.setText(y)
year.translateY(8)

# Nothing to do in the loop ;)
def loop():
    pass
```
- Show the weather forecast for your location.
- Create a shopping list widget.
```Python
from mosaico import widget, config

# Create title
text = widget.createText()
text.setText(config["name"])
text.setHexColor(config["color"])
text.translate(2,2)
text.setFontHeight(10)

# Create items
items = []
for i in range(0, len(config["items"])):
    items.append(widget.createText())
    items[i].setFontHeight(6)
    items[i].setText(config["items"][i])
    items[i].translate(2, 6+ 7 * (i + 1))

def loop():
    pass 
```
- Upload a custom image and display it as pixel art.
```Python
from mosaico import widget, config

# Create image
img = widget.createImage(widget.configAsset("image"))

def loop():
    pass
```
- Write custom text messages or quotes.
- Create animations or visual effects.

## Architecture Overview

The Mosaico Ecosystem consists of:

- **Raspberry Pi Software**: Written in C++ and Python, this software drives the LED matrix and manages the execution of widgets.
- **Mobile App**: Connects to the Raspberry Pi via BLE and COAP, allowing users to manage widgets, create slideshows, and configure network settings.
- **App Store**: A platform where developers can submit their widgets for others to use.
- **IDE**: A (dummy) desktop application that allows developers to create and test widgets locally. It is meant to be a lightweight tool to help developers get started with widget development.
- **Simulator**: An X11 window that simulates the LED matrix for development purposes. A web-based simulator is in the works and will allow developers to test their widgets without a physical matrix in the easiest way possible.

### Raspberry Pi Software
The Raspberry Pi software is split into two main parts:
1. **C++ Core**: Drives the LED matrix and runs the Python interpreter for executing widgets. Uses Pybind11 for C++ and Python interoperability.
2. **Python Networking Module**: Manages network communication via GATT and COAP servers, handles persistent data with SQLite, and tunnels commands to the C++ core through a Linux socket.


## Getting Started
To get started with Mosaico:
1. **Set up your Raspberry Pi**: Install the Mosaico software and connect the LED matrix.
2. **Download the Mobile App**: Available on [App Store](#) and [Google Play](#).
3. **Explore the App Store**: Browse and install widgets to display on your matrix.
4. **Create Slideshows**: Customize your display by combining multiple widgets.
5. **Connect to Wi-Fi**: Use the mobile app to configure network settings.

![Getting Started](https://via.placeholder.com/300x200)

## Support
For more information and support, visit our [documentation](#) or contact our [support team](#).

![Support](https://via.placeholder.com/300x200)

Join the Mosaico community and start creating your own vibrant LED matrix displays today!