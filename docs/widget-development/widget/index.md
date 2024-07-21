This object holds all the necessary functions to create drawables and add them to the final widget.

You can import this module with:
```python
from mosaico import widget
```

The main purpose of the module is to provide a simple way to add drawables to the widget, for 
example you can add a text drawable with the following code:

```python
text = widget.createText()
```

For more information on how to create drawables consult the [drawable](/widget-development/widget/drawables/drawable) section.

Some helpers functions are available:

## `remove(drawable)`
Removes the given drawable from the widget.
> Warning: This function will completely remove the drawable from the memory, accessing 
> the drawable after removing it will create a SEGFAULT in C++.

### Example

```python
from mosaico import widget 
text = widget.createText()
widget.remove(text)
text.setText("A beautiful SEGFAULT") # This will create a SEGFAULT lol
```

### Parameters
| Parameter | Type | Description                                |
| --------- | ---- |--------------------------------------------|
| drawable  | Drawable | The drawable to be removed. |

## Returns
None

## `widgetAsset(assetName)`
Returns the path to the asset with the given name inside the widget assets folder.

### Example

```python
from mosaico import widget
image = widget.createImage()
image.setImage(widget.widgetAsset("icon.ppm"))
```

### Parameters
| Parameter | Type | Description                                |
| --------- | ---- |--------------------------------------------|
| assetName | str | The name of the asset (without extension). |

### Returns
str: The path to the asset.


## `configAsset(assetName)`
Returns the path to the asset with the given name inside the config assets folder. 

### Example

```python
from mosaico import widget
image = widget.createImage()
image.setImage(widget.configAsset("icon"))
```

### Parameters
| Parameter | Type | Description                                |
| --------- | ---- |--------------------------------------------|
| assetName | str | The name of the asset (without extension). |

### Returns
str: The path to the asset.