# CreateImageControl

## Description
Creates a Layout Manager image control.

```pascal
PROCEDURE CreateImageControl(
				dialogID      : LONGINT;
				componentID   : LONGINT;
				iWidthPixels  : INTEGER;
				iHeightPixels : INTEGER;
				hImage        : HANDLE);
```

```python
def vs.CreateImageControl(dialogID, componentID, iWidthPixels, iHeightPixels, hImage):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|   |
|componentID|LONGINT|   |
|iWidthPixels|INTEGER|   |
|iHeightPixels|INTEGER|   |
|hImage|HANDLE|   |

## Examples
```pascal
CreateImageControl(1, 2, 3, 10, hImage);
```
```python
import vs

# Creates a Layout Manager image control.
dialogID = 1
componentID = 2
iWidthPixels = 3
iHeightPixels = 10
hImage = vs.FSActLayer()  # handle to the first selected object on the active layer

vs.CreateImageControl(dialogID, componentID, iWidthPixels, iHeightPixels, hImage)
newObj = vs.LNewObj()  # handle to the newly created object
```

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
