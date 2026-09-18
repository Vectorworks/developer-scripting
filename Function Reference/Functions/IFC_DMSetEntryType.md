# IFC_DMSetEntryType

## Description
Sets specified IfcEntry type - Primary/Secondary.

```pascal
FUNCTION IFC_DMSetEntryType(
				strObjectName : STRING;
				strEntryName  : STRING;
				type          : INTEGER): BOOLEAN;
```

```python
def vs.IFC_DMSetEntryType(strObjectName, strEntryName, type):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|strObjectName|STRING|   |
|strEntryName|STRING|   |
|type|INTEGER|   |

## Examples
```pascal
resultOK := IFC_DMSetEntryType('Example', 'Example', 1);
```
```python
import vs

# Sets specified IfcEntry type - Primary/Secondary.
strObjectName = 'Example'
strEntryName = 'Example'
type = 0

ok = vs.IFC_DMSetEntryType(strObjectName, strEntryName, type)
if ok:
    vs.Message('IFC_DMSetEntryType succeeded')
else:
    vs.Message('IFC_DMSetEntryType failed')
```

## Version
Availability: from Vectorworks 2021

## Category
* [IFC](../Categories/IFC.md)
