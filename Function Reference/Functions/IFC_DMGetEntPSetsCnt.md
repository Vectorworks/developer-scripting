# IFC_DMGetEntPSetsCnt

## Description
Returns the Property Sets count for IfcEntity in Object's IFC Data Mapping.

```pascal
FUNCTION IFC_DMGetEntPSetsCnt(
				strObjectName : STRING;
				strEntryName  : STRING;
				VAR outType   : INTEGER): BOOLEAN;
```

```python
def vs.IFC_DMGetEntPSetsCnt(strObjectName, strEntryName):
    return (BOOLEAN, outType)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|strObjectName|STRING|   |
|strEntryName|STRING|   |
|outType|INTEGER|   |

## Examples
```pascal
resultOK := IFC_DMGetEntPSetsCnt('Example', 'Example', 1);
```
```python
import vs

# Returns the Property Sets count for IfcEntity in Object's IFC Data Mapping.
strObjectName = 'Example'
strEntryName = 'Example'

ok, outType = vs.IFC_DMGetEntPSetsCnt(strObjectName, strEntryName)
vs.Message('IFC_DMGetEntPSetsCnt returned: ' + str((ok, outType)))
```

## Version
Availability: from Vectorworks 2021

## Category
* [IFC](../Categories/IFC.md)
