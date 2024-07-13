# Shared library

Since this project is composed of multiple applications, I preferred to create a shared library to store common code that can be used across different projects. 

This library is written in Dart and mostly contains classes and functions that are crucial for the communication with the matrix or common UI components to share between the IDE and the mobile app.
I tried to follow CLEAN architecture principles, so the library is divided into the following folders:

- **core**: 
    - **configurations**:
    - **exceptions**:
    - **models**:
    - **networking**:
    - **utils**:
- **common**:
- **features**:
    - **config_generator**:
    - **matrix_control**:
    - **mosaico_loading**:
    - **mosaico_slideshows**:
    - **mosaico_widgets**:
