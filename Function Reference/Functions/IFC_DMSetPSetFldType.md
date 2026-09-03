# IFC_DMSetPSetFldType

## Description
Sets the type of specified Field for IfcEntry's PSet.

```pascal
FUNCTION IFC_DMSetPSetFldType(
				strObjectName : STRING;
				strEntryName  : STRING;
				strPSetName   : STRING;
				strFieldName  : STRING;
				type          : INTEGER): BOOLEAN;
```

```python
def vs.IFC_DMSetPSetFldType(strObjectName, strEntryName, strPSetName, strFieldName, type):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|strObjectName|STRING|   |
|strEntryName|STRING|   |
|strPSetName|STRING|   |
|strFieldName|STRING|   |
|type|INTEGER|   |

## Examples
```pascal
resultOK := IFC_DMSetPSetFldType('Example', 'Example', 'Example', 'MyRecord', 1);
```
```python
import vs

# Sets the type of specified Field for IfcEntry's PSet.
strObjectName = 'Example'
strEntryName = 'Example'
strPSetName = 'Example'
strFieldName = 'MyField'
type = 0

ok = vs.IFC_DMSetPSetFldType(strObjectName, strEntryName, strPSetName, strFieldName, type)
if ok:
    vs.Message('IFC_DMSetPSetFldType succeeded')
else:
    vs.Message('IFC_DMSetPSetFldType failed')
```

## Version
Availability: from Vectorworks 2021

## Category
* [IFC](../Categories/IFC.md)
