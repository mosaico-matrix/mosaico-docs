A text is a drawable that can be used to display text on the matrix.
If the text overflows the canvas, it will start scrolling.

## `setText(text)`
Sets the text to be displayed.

### Example

```python
from mosaico import widget
text = widget.createText()
text.setText("Hello, World!")
```

### Parameters
| Parameter | Type | Description |
| --------- | ---- | ----------- |
| text | str | The text to be displayed. |

### Returns
None

## `setFont(font)`
Sets the font to be used to display the text.


### Example

```python
from mosaico import widget
text = widget.createText()
text.setFont("8x13B")
```

### Parameters
| Parameter | Type | Description |
| --------- | ---- | ----------- |
| font | str | The font to be used. |

### Returns
None

### Available Fonts
```Python
"4x6","5x7","5x8","6x9","6x10","6x12","6x13","7x13","7x14","8x13","9x15","9x18","10x20","clR6x12","7x14B","9x15B","texgyre-27","8x13O","7x13B","9x18B","6x13O","tom-thumb","helvR12","6x13B","7x13O","8x13B"
```