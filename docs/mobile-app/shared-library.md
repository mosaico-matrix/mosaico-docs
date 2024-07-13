# Shared library

## Introduction
Since this project is composed of multiple applications, I preferred to create a shared library to store common code that can be used across different projects. 

This library is written in Dart and mostly contains classes and functions that are crucial for the communication with the matrix or common UI components to share between the IDE and the mobile app.
I tried to follow CLEAN architecture principles, so the library is divided into the following folders:

## Project structure
### Core 
- **configurations**:
    - `app_color_scheme.dart`: Contains the color scheme used in the app. This is shared so that both the IDE and the mobile app can use the same colors.
    - `coap_config.dart`: Contains the configuration for the CoAP client.
    - `configs.dart`: Contains the configuration for the app.
- **exceptions**: Contains custom exceptions that can be thrown by the app and caught by the global error handler in order to dispatch the error to the UI.
- **models**: Shared models needed throughout the app.
- **networking**: 
    - `ble_service.dart`: Contains the BLE client that is used to communicate with the matrix.
    - `coap_service.dart`: Contains the CoAP client that is used to communicate with the matrix.
    - `rest_service.dart`: Contains the REST client that is used to communicate with the matrix.
### Utils
- **common**: shared dart widgets used in IDE and APP
      - matrices
          - `led_matrix.dart`: The main matrix widget. This can be extended with multiple animations and effects.
          - `loading_matrix.dart`: Random pixels turned off and on to simulate loading.
             - ![loading matrix](assets/gifs/matrices/loading_matrix.gif)
          - `no_data_matrix.dart`: A widget that displays animated sad face with a message when there is no data to display.
             - ![no data matrix](assets/gifs/matrices/no_data_matrix.gif)
### Features
- **config_generator**: the module responsible for generating the configuration file for a widget with the `dynamic_form`
- **matrix_control**: the module responsible for controlling the matrix and checking the connection status
- **mosaico_loading**: wrapper around pages to handle loading states
- **mosaico_slideshows**: the module responsible for programming slideshows
- **mosaico_widgets**: the module responsible for installing and managing widgets
