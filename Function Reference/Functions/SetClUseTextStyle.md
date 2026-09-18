# SetClUseTextStyle

## Description
Controls whether the text style of the specified class is used at object creation.

```pascal
PROCEDURE SetClUseTextStyle(
				className : STRING;
				use       : BOOLEAN);
```

```python
def vs.SetClUseTextStyle(className, use):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|className|STRING|Name of class|
|use|BOOLEAN|Use text style on-off setting.|

## Examples
```pascal
SetClUseTextStyle('Wall', TRUE);
```
```python
import vs

# Controls whether the text style of the specified class is used at object
# creation.
className = 'None'
use = True

vs.SetClUseTextStyle(className, use)
```

## See Also
VS Functions:
[GetClUseTextStyle](GetClUseTextStyle.md) 
| [SetClTextStyleRef](SetClTextStyleRef.md) 
| [GetClTextStyleRef](GetClTextStyleRef.md)

## Version
Availability: from Vectorworks 2015

## Category
* [Classes](../Categories/Classes.md)
