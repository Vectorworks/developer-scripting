# IFC_DMGetPSetName

## Description
Returns the Name for Mapped IfcEntity's Property Set IFC Data Mapping.

```pascal
FUNCTION IFC_DMGetPSetName(
				strObjectName      : STRING;
				strEntryName       : STRING;
				psetIndex          : INTEGER;
				VAR outStrPSetName : STRING): BOOLEAN;
```

```python
def vs.IFC_DMGetPSetName(strObjectName, strEntryName, psetIndex):
    return (BOOLEAN, outStrPSetName)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|strObjectName|STRING|   |
|strEntryName|STRING|   |
|psetIndex|INTEGER|   |
|outStrPSetName|STRING|   |

## Examples
```pascal
resultOK := IFC_DMGetPSetName('Example', 'Example', 1, 'Example');
```
```python
import vs

# Returns the Name for Mapped IfcEntity's Property Set IFC Data Mapping.
strObjectName = 'Example'
strEntryName = 'Example'
psetIndex = 1

ok, outStrPSetName = vs.IFC_DMGetPSetName(strObjectName, strEntryName, psetIndex)
vs.Message('IFC_DMGetPSetName returned: ' + str((ok, outStrPSetName)))
```

## Version
Availability: from Vectorworks 2021

## Category
* [IFC](../Categories/IFC.md)
