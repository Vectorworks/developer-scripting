# IFC_DMGetObjNameAt

## Description
Returns the Object Name for specified index in IFC Data Mapping.

```pascal
FUNCTION IFC_DMGetObjNameAt(
				index                : INTEGER;
				VAR outStrObjectName : STRING): BOOLEAN;
```

```python
def vs.IFC_DMGetObjNameAt(index):
    return (BOOLEAN, outStrObjectName)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|index|INTEGER|   |
|outStrObjectName|STRING|   |

## Examples
```pascal
resultOK := IFC_DMGetObjNameAt(1, 'Example');
```
```python
import vs

# Returns the Object Name for specified index in IFC Data Mapping.
index = 1

ok, outStrObjectName = vs.IFC_DMGetObjNameAt(index)
vs.Message('IFC_DMGetObjNameAt returned: ' + str((ok, outStrObjectName)))
```

## Version
Availability: from Vectorworks 2021

## Category
* [IFC](../Categories/IFC.md)
