# SetSymDefSubType

## Description
Sets the sub type for a symbol definition that is used to define a plug-in style.

```pascal
PROCEDURE SetSymDefSubType(
				hSymDef : HANDLE;
				subType : INTEGER);
```

```python
def vs.SetSymDefSubType(hSymDef, subType):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hSymDef|HANDLE|Handle to symbol definition that is being used to define a plug-in style.|
|subType|INTEGER|Sub type identifier to set for the symbol definition.|

## Examples
```pascal
SetSymDefSubType(hSymDef, 1);
```
```python
import vs

# Sets the sub type for a symbol definition that is used to define a plug-in
# style.
hSymDef = vs.GetObject('MySymbol')  # handle to a symbol definition
subType = 0

vs.SetSymDefSubType(hSymDef, subType)
```

## Version
Availability: from Vectorworks 2017

## Category
* [Objects - Symbols](../Categories/Objects%20-%20Symbols.md)
