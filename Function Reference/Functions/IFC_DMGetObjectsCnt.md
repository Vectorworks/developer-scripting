# IFC_DMGetObjectsCnt

## Description
Returns the IFC Data Mapping Objects count.

```pascal
FUNCTION IFC_DMGetObjectsCnt(VAR outCount : INTEGER): BOOLEAN;
```

```python
def vs.IFC_DMGetObjectsCnt():
    return (BOOLEAN, outCount)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|outCount|INTEGER|   |

## Examples
```pascal
resultOK := IFC_DMGetObjectsCnt(1);
```
```python
import vs

# Returns the IFC Data Mapping Objects count.
ok, outCount = vs.IFC_DMGetObjectsCnt()
vs.Message('IFC_DMGetObjectsCnt returned: ' + str((ok, outCount)))
```

## Version
Availability: from Vectorworks 2021

## Category
* [IFC](../Categories/IFC.md)
