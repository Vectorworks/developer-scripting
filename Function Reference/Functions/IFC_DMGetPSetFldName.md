# IFC_DMGetPSetFldName

## Description
Gets Field Name for specified index in IfcEntry's PSet.

```pascal
FUNCTION IFC_DMGetPSetFldName(
				strObjectName       : STRING;
				strEntryName        : STRING;
				strPSetName         : STRING;
				index               : INTEGER;
				VAR outStrFieldName : STRING): BOOLEAN;
```

```python
def vs.IFC_DMGetPSetFldName(strObjectName, strEntryName, strPSetName, index):
    return (BOOLEAN, outStrFieldName)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|strObjectName|STRING|   |
|strEntryName|STRING|   |
|strPSetName|STRING|   |
|index|INTEGER|   |
|outStrFieldName|STRING|   |

## Examples
```pascal
resultOK := IFC_DMGetPSetFldName('Example', 'Example', 'Example', 1, 'MyRecord');
```
```python
import vs

# Gets Field Name for specified index in IfcEntry's PSet.
strObjectName = 'Example'
strEntryName = 'Example'
strPSetName = 'Example'
index = 1

ok, outStrFieldName = vs.IFC_DMGetPSetFldName(strObjectName, strEntryName, strPSetName, index)
vs.Message('IFC_DMGetPSetFldName returned: ' + str((ok, outStrFieldName)))
```

## Version
Availability: from Vectorworks 2021

## Category
* [IFC](../Categories/IFC.md)
