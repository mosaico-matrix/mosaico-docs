A drawable is basically a list of pixels that can be drawn on the widget canvas.
The drawable class is abstract and cannot be instantiated but all the drawables inherit from it.

## `moveTo(x, y)`
Directly moves the drawable to the specified position, without animating it.

### Example

```python
from mosaico import widget
text = widget.createText()
text.moveTo(10, 10)
```

### Parameters
| Parameter | Type | Description |
| --------- | ---- | ----------- |
| x | int | The x coordinate of the new position. |
| y | int | The y coordinate of the new position. |


### Returns
None

## `translateBy(dx, dy)`

Moves the drawable by the specified amount of pixels.

### Example

```python
from mosaico import widget
text = widget.createText()
text.translateBy(10, 10)
```

### Parameters
| Parameter | Type | Description |
| --------- | ---- | ----------- |
| dx | int | The amount of pixels to move the drawable in the x axis. |
| dy | int | The amount of pixels to move the drawable in the y axis. |

### Returns
None

## `translateByX(dx)`

Moves the drawable by the specified amount of pixels in the x axis.

### Example

```python
from mosaico import widget
text = widget.createText()
text.translateByX(10)
```

### Parameters
| Parameter | Type | Description |
| --------- | ---- | ----------- |
| dx | int | The amount of pixels to move the drawable in the x axis. |

### Returns
None

## `translateByY(dy)`

Moves the drawable by the specified amount of pixels in the y axis.

### Example

```python
from mosaico import widget
text = widget.createText()
text.translateByY(10)
```

### Parameters
| Parameter | Type | Description                                              |
|-----------| ---- |----------------------------------------------------------|
| dy        | int | The amount of pixels to move the drawable in the y axis. |

### Returns
None

## `setFrameDuration(frameDurationMs)`

Sets the duration of each frame in milliseconds. This is used for animations to determine the speed.

### Example

```python
from mosaico import widget
text = widget.createText()
text.setFrameDuration(100)
```

### Parameters
| Parameter | Type | Description                          |
|-----------|------|--------------------------------------|
| frameDurationMs | unsigned int | Duration of each frame in milliseconds |

### Returns
None

## `setColor(color)`

Sets the color of the drawable using a `Color` object.

### Example

```python
from mosaico import widget
from mosaico.color import Color
text = widget.createText()
text.setColor(Color(255, 0, 0))  # Sets color to red
```

### Parameters
| Parameter | Type | Description |
|-----------|------|-------------|
| color     | Color | The color to set |

### Returns
None

## `setHexColor(hexColor)`

Sets the color of the drawable using a hex string.

### Example

```python
from mosaico import widget
text = widget.createText()
text.setHexColor("#FF0000")  # Sets color to red
```

### Parameters
| Parameter | Type   | Description |
|-----------|--------|-------------|
| hexColor  | string | The hex string representing the color |

### Returns
None

## `animateTo(x, y, animationDurationMs)`

Animates the drawable to move to the specified position over the given duration.

### Example

```python
from mosaico import widget
text = widget.createText()
text.animateTo(50, 50, 2000)  # Move to (50, 50) over 2000 milliseconds
```

### Parameters
| Parameter             | Type           | Description |
|-----------------------|----------------|-------------|
| x                     | int            | The x coordinate of the target position |
| y                     | int            | The y coordinate of the target position |
| animationDurationMs   | unsigned int   | Duration of the animation in milliseconds |

### Returns
None

## `hide()`

Hides the drawable.

### Example

```python
from mosaico import widget
text = widget.createText()
text.hide()
```

### Returns
None

## `show()`

Shows the drawable if it is hidden.

### Example

```python
from mosaico import widget
text = widget.createText()
text.show()
```

### Returns
None

## `isVisible()`

Checks if the drawable is currently visible.

### Example

```python
from mosaico import widget
text = widget.createText()
print(text.isVisible())  # Outputs: True or False
```

### Returns
| Type    | Description             |
|---------|-------------------------|
| bool    | True if visible, False otherwise |

## `isAnimating()`

Checks if the drawable is currently animating.

### Example

```python
from mosaico import widget
text = widget.createText()
print(text.isAnimating())  # Outputs: True or False
```

### Returns
| Type    | Description             |
|---------|-------------------------|
| bool    | True if animating, False otherwise |

## `getX()`

Gets the current x coordinate of the drawable.

### Example

```python
from mosaico import widget
text = widget.createText()
print(text.getX())  # Outputs: current x position
```

### Returns
| Type | Description      |
|------|------------------|
| int  | The x coordinate |

## `getY()`

Gets the current y coordinate of the drawable.

### Example

```python
from mosaico import widget
text = widget.createText()
print(text.getY())  # Outputs: current y position
```

### Returns
| Type | Description      |
|------|------------------|
| int  | The y coordinate |
