```Python
from mosaico import widget, config

# Create title
text = widget.createText()
text.setText(config["name"])
text.setHexColor(config["color"])
text.translate(2,2)
text.setFontHeight(10)

# Create items
items = []
for i in range(0, len(config["items"])):
    items.append(widget.createText())
    items[i].setFontHeight(6)
    items[i].setText(config["items"][i])
    items[i].translate(2, 6+ 7 * (i + 1))

def loop():
    pass 
    
from datetime import date
from mosaico import widget

# Get the current date
today = date.today()
d = today.strftime("%d")
m = today.strftime("%m")
y = today.strftime("%Y")

# Display on matrix
day_month = widget.createText()
day_month.setText(d + "-" + m)
year = widget.createText()
year.setText(y)
year.translateY(8)

# Nothing to do in the loop ;)
def loop():
    pass
    
from mosaico import widget, config

# Create image
img = widget.createImage(widget.configAsset("image"))

def loop():
    pass
```