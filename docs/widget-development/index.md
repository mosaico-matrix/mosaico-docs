# Introduction
Widgets can be dynamically installed on the matrix without needing software re-compilation.
This is done by integrating a Python interpreter in the C++ software running on the Pi.

In order to start developing widgets, you need to have a basic understanding of Python and the Matrix software architecture.

We can define 3 types of widgets:

- **Static**: Widgets that don't require any configurations
    - A clock
    - An inspirational quote
    - News headlines
    - Stock prices
- **Configurable**: Widgets that require some input from the user before being displayed
    - Weather forecast
    - Todo list
    - Image to pixel art
- **Interactive**: Widgets that require live interaction with the user (coming soon)
    - Games
    - Painter

These objects will be provided for you to use in your widgets: `widget`, `config`, `canvas` and `colors`.