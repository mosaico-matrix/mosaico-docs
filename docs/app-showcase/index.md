# Mobile App
The mobile app interfaces with the Raspberry Pi to:

- Configure and manage installed widgets.
- Browse and install widgets from the App Store.
- Create and manage slideshows.
- Check device status
- Control device
- Send Wi-Fi credentials via BLE.


<div style="display: flex;">
    <img class="screenshot" src="assets/screenshots/home/widgets_empty.png" alt="Image 1">
        <img class="screenshot" src="assets/screenshots/home/store.png" alt="Image 1">
            <img class="screenshot" src="assets/screenshots/home/slideshows.png" alt="Image 2">
    <img class="screenshot" src="assets/screenshots/home/device_control.png" alt="Image 2">
</div>
<!-- <figure markdown>
![Mobile App Interface](assets/screenshots/home/widgets_empty.png) {: style="height:83px"}
![Mobile App Interface](assets/screenshots/home/device_control.png) {: style="height:83px"}
  <figcaption>Partners</figcaption>
</figure> -->

## Features
- **Custom Widgets**: Develop and display custom Python widgets on a LED matrix.
- **Widget Store**: Submit and download widgets from the online store.
- **Slideshows**: Create slideshows to display multiple widgets in sequence.
- **Network Configuration**: Easily configure network settings via BLE or COAP.
- **Local IP Retrieval**: Use BLE to get the local IP address of the Raspberry Pi for COAP connections.

## Developing Widgets
Developers can create widgets using Python and submit them to the App Store. Each widget can be either static or configurable. For example:
- **Static Widget**: Displays fixed information such as the current time.
- **Configurable Widget**: Requires user input, such as a grocery list widget.

![Widget Example](https://via.placeholder.com/300x200)

## Mobile App Functionality
The mobile app offers various features to enhance your Mosaico experience:
- **App Store Access**: Browse and install widgets from the store.
- **Widget Management**: Add, remove, and configure widgets.
- **Slideshow Creation**: Combine multiple widgets into a slideshow with specified durations.

![App Store Interface](https://via.placeholder.com/300x600)

## Creating Slideshows
Slideshows allow you to display a sequence of widgets on your LED matrix. Each slideshow is composed of multiple slideshow items, defined as:
- **widget_id**: The identifier of the widget.
- **config_id** (if any): The identifier of the widget configuration.
- **durationSeconds**: The duration for which the widget is displayed.

![Slideshow Example](https://via.placeholder.com/300x200)

## Connecting to Wi-Fi
The mobile app can send Wi-Fi credentials to the Raspberry Pi via BLE, enabling easy network configuration. When the matrix is connected to the internet, BLE can also be used to retrieve the local IP address for COAP communication.

![Wi-Fi Setup](https://via.placeholder.com/300x600)