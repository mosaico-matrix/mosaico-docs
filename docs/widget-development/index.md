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

## File management
Your widget will be stored in the `widgets` directory of the storage. The directory structure should look like this:

```
widgets/
├── author_name/
│   ├── widget_name/
│   │   ├── widget.py
configs/
├── author_name/
│   ├── widget_name/
│   │   ├── config.json
```

If you create files inside your widget script (for example, to save persistent data),
your path is automatically set to the widget's directory (if the widget is static) 
or the configuration's directory (if the widget is configurable).