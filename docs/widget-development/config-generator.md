# Configuration generator
Configurable widgets require a way to get data from the user to configure the widget. 
Developers can create a configuration file in .json format that will be parsed by the configuration generator to create a form
that the user can fill in to configure the widget.

This choice was crucial to allow developers to create new widgets without having to worry about the UI, 
and to have consistency in the configuration of widgets from different developers.

## Examples

A simple example of a configuration file to create a configurations to upload an image to the matrix could be:
/// html | div[class='left-side']
```json
{
  "form": {
    "title": "Image",
    "description": "Simply choose an image to display in pixel art on the matrix!",
    "fields": [
      {
        "image": {
          "type": "image",
          "label": "Image",
          "required": true       
          }
      }
    ]
  }
}
```
///

/// html | div[class='right-side']
![Image form](../mobile-app/assets/screenshots/config_generator/image_form.png)
///

/// html | div[style='clear: both;']
///

<div class="pdf-break"></div>


A simple example of a configuration file for a shopping list widget could be:
/// html | div[class='left-side']
```json
{
  "form": {
    "title": "Shopping List",
    "description": "Configure your widget here",
    "fields": [
      {
        "name": {
          "type": "string",
          "label": "Name",
          "required": true,
          "placeholder": "Enter the name of this list"
        },
         "color": {
          "type": "color",
          "label": "Color",
          "required": true,
          "placeholder": "Choose the color of the title"
        },
        "items": {
          "type": "string[]",
          "label": "Shopping items",
          "required": true,
          "placeholder": "Insert your items here"
        }
      }
    ]
  }
}
        
```
///

/// html | div[class='right-side']
![Shopping List](../mobile-app/assets/screenshots/config_generator/shopping_list_form.png)
///

/// html | div[style='clear: both;']
///

<div class="pdf-break"></div>

## Result of the configuration
The data collected from the user is then saved in a .json file, which is then parsed by C++ when a specific widget with that configuration is loaded.
Getting data from the configuration is very easy and can be done in python with the following code:
```python
from mosaico import widget, config # config is the object holding all data from the configuration

text = widget.createText()
text.setText(config["name"]) # Get the name of the list from the configuration
text.setHexColor(config["color"]) # Get the color of the heading from the configuration
text.translate(2,2)
text.setFontHeight(10)

# Create items
items = []
for i in range(0, len(config["items"])): # We can iterate in the array provided by the user
    items.append(widget.createText())
    items[i].setFontHeight(6)
    items[i].setText(config["items"][i])
    items[i].translate(2, 6+ 7 * (i + 1))

def loop():
    pass
```

### What about the assets?
User uploaded assets like images are saved in the .tar.gz archive in the assets folder, 
a helper function is available to retrieve the path of the asset in the archive.

## Field attributes
Regardless of the type of field, all fields have the following attributes in common:

### Name (required)
The unique name of the field. This is used to identify the field in the configuration file.
> DON'T USE THE SAME NAME FOR TWO DIFFERENT FIELDS!

### Type (required)
The type of the field. This can be one of the following:

- `string`: A simple string.
- `string[]`: An array of strings.
- `color`: A color picker.
- `image`: An image upload

### Label 
The label of the field. This is displayed to the user in the configuration form to help them understand what the field is for.

### Required
A boolean value that indicates if the field is mandatory or not.

### Placeholder
A string that is displayed in the field when it is empty to help the user understand what the field is for.


## Field types
### `String`
A simple string field. The user can input any text.

#### Special attributes
None

### `String[]`
An array of strings. The user can input multiple strings.

#### Special attributes
None


### `Color`
A color picker. The user can choose a color from a color picker.

#### Special attributes
None

### `Image`
An image upload field. The user can upload an image.

#### Special attributes
##### Dimensions
The dimensions of the image. This is an object with the following attributes:

- `width`: The width of the image in pixels.
- `height`: The height of the image in pixels.
> MAXIMUM SIZE: 64x64