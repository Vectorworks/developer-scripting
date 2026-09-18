# SetImageControlPath

## Description
Sets the image control path for the specified layout manager image control.  Use with CreateImageControl.

```pascal
FUNCTION SetImageControlPath(
				nDialogID    : LONGINT;
				nComponentID : LONGINT;
				strPath      : STRING): BOOLEAN;
```

```python
def vs.SetImageControlPath(nDialogID, nComponentID, strPath):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|nDialogID|LONGINT|   |
|nComponentID|LONGINT|   |
|strPath|STRING|   |

## Examples
```pascal
resultOK := SetImageControlPath(1, 2, 'file.txt');
```
```python
import vs

# Sets the image control path for the specified layout manager image control.
nDialogID = 1
nComponentID = 2
strPath = 'C:/Temp'

ok = vs.SetImageControlPath(nDialogID, nComponentID, strPath)
if ok:
    vs.Message('SetImageControlPath succeeded')
else:
    vs.Message('SetImageControlPath failed')
```

## Version
Availability: from VectorWorks13.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
