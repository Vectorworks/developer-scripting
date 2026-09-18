# IFC_DMDelPSetFromEnt

## Description
Deletes Property Set from specified Object IfcEntry's group in IFC Data Mapping.

```pascal
FUNCTION IFC_DMDelPSetFromEnt(
				strObjectName : STRING;
				strEntryName  : STRING;
				strPSetName   : STRING): BOOLEAN;
```

```python
def vs.IFC_DMDelPSetFromEnt(strObjectName, strEntryName, strPSetName):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|strObjectName|STRING|   |
|strEntryName|STRING|   |
|strPSetName|STRING|   |

## Examples
```pascal
resultOK := IFC_DMDelPSetFromEnt('Example', 'Example', 'Example');
```
```python
import vs

# Deletes Property Set from specified Object IfcEntry's group in IFC Data
# Mapping.
strObjectName = 'Example'
strEntryName = 'Example'
strPSetName = 'Example'

ok = vs.IFC_DMDelPSetFromEnt(strObjectName, strEntryName, strPSetName)
if ok:
    vs.Message('IFC_DMDelPSetFromEnt succeeded')
else:
    vs.Message('IFC_DMDelPSetFromEnt failed')
```

## Version
Availability: from Vectorworks 2021

## Category
* [IFC](../Categories/IFC.md)
