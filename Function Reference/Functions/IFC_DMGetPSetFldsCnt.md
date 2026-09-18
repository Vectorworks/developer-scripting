# IFC_DMGetPSetFldsCnt

## Description
Gets Fields Count for specified IfcEntry's PSet.

```pascal
FUNCTION IFC_DMGetPSetFldsCnt(
				strObjectName      : STRING;
				strEntryName       : STRING;
				strPSetName        : STRING;
				VAR outFieldsCount : INTEGER): BOOLEAN;
```

```python
def vs.IFC_DMGetPSetFldsCnt(strObjectName, strEntryName, strPSetName):
    return (BOOLEAN, outFieldsCount)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|strObjectName|STRING|   |
|strEntryName|STRING|   |
|strPSetName|STRING|   |
|outFieldsCount|INTEGER|   |

## Examples
```pascal
resultOK := IFC_DMGetPSetFldsCnt('Example', 'Example', 'Example', 1);
```
```python
import vs

# Gets Fields Count for specified IfcEntry's PSet.
strObjectName = 'Example'
strEntryName = 'Example'
strPSetName = 'Example'

ok, outFieldsCount = vs.IFC_DMGetPSetFldsCnt(strObjectName, strEntryName, strPSetName)
vs.Message('IFC_DMGetPSetFldsCnt returned: ' + str((ok, outFieldsCount)))
```

## Version
Availability: from Vectorworks 2021

## Category
* [IFC](../Categories/IFC.md)
