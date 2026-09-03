# CreateDataVisPDMenu

## Description
Creates a Layout Manager data visualization pull down menu control.

```pascal
PROCEDURE CreateDataVisPDMenu(
				dialogID               : LONGINT;
				componentID            : LONGINT;
				widthInStdChar         : INTEGER;
				showDefaultStaticItems : BOOLEAN);
```

```python

def vs.CreateDataVisPDMenu(dialogID, componentID, widthInStdChar, showDefaultStaticItems):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT||
|componentID|LONGINT||
|widthInStdChar|INTEGER|The width of the displayed text in standard character count. See GetDlgCtrlWidthStdCh.|
|showDefaultStaticItems|BOOLEAN||

## Examples
```pascal
CreateDataVisPDMenu(1, 2, 3, TRUE);
```
```python
import vs

# Creates a Layout Manager data visualization pull down menu control.
dialogID = 1
componentID = 2
widthInStdChar = 3
showDefaultStaticItems = True

ok = vs.CreateDataVisPDMenu(dialogID, componentID, widthInStdChar, showDefaultStaticItems)
if ok:
    vs.Message('CreateDataVisPDMenu succeeded')
else:
    vs.Message('CreateDataVisPDMenu failed')
```

## Version
Availability: from Vectorworks 2024

## Category
* [Dialogs - Modern](../Categories/Dialogs - Modern.md)
