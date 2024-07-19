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