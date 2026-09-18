# SetImageControlHandle

## Description
Sets the image definition node handle for the specified Layout Manager image control.

```pascal
PROCEDURE SetImageControlHandle(
				dialogID    : LONGINT;
				componentID : LONGINT;
				hImage      : HANDLE);
```

```python
def vs.SetImageControlHandle(dialogID, componentID, hImage):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|   |
|componentID|LONGINT|   |
|hImage|HANDLE|   |

## Examples
```pascal
SetImageControlHandle(1, 2, hImage);
```
```python
import vs

# Sets the image definition node handle for the specified Layout Manager
# image control.
dialogID = 1
componentID = 2
hImage = vs.FSActLayer()  # handle to the first selected object on the active layer

vs.SetImageControlHandle(dialogID, componentID, hImage)
```

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
