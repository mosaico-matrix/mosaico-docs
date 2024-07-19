In case you want to develop a configurable widget, you'll need to use the `config` object
This object is automatically filled with all the data entered from the user in the configuration page.

You can import this object with:
```python
from mosaico import config
```

This is simply an array, so you can access the data like this:
```python
text = widget.createText()
text.setText(config['name']) # Where name is the name of the configuration field
```