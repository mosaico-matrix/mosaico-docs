An image is a drawable that can be used to display a PPM image on the matrix.
The image can have variable width and height but is mandatory to be less than or equal to the matrix width and height.

## `setImage(imagePath)`
Sets the image to be displayed. The path should never be entered directly but
should be obtained from utilities mentioned in the [widget index](/widget-development/widget/) section.

### Example

```python
from mosaico import widget
image = widget.createImage()
image.setImage(widget.widgetAsset("icon.ppm"))
image.setImage(widget.configAsset("icon"))
```

### Parameters
| Parameter | Type | Description |
| --------- | ---- | ----------- |
| imagePath | str | The path to the image file. |

### Returns
None