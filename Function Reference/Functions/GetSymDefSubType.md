# GetSymDefSubType

## Description
Returns the sub type defined for a symbol definiiton. This is used when creating and using plug-in styles.

```pascal
FUNCTION GetSymDefSubType(hSymDef : HANDLE): INTEGER;
```

```python
def vs.GetSymDefSubType(hSymDef):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hSymDef|HANDLE|Handle to a symbol definition contaiing a plug-in style.|

## Examples
```pascal
resultN := GetSymDefSubType(hSymDef);
```
```python
import vs

# Returns the sub type defined for a symbol definiiton.
hSymDef = vs.GetObject('MySymbol')  # handle to a symbol definition

resultN = vs.GetSymDefSubType(hSymDef)
vs.Message('GetSymDefSubType returned: ' + str(resultN))
```

## Version
Availability: from Vectorworks 2017

## Category
* [Objects - Symbols](../Categories/Objects%20-%20Symbols.md)
