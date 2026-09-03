# IFC_DMIsPSetFldEmpty

## Description
Checks if specified Field for IfcEntry's PSet is Empty.

```pascal
FUNCTION IFC_DMIsPSetFldEmpty(
				strObjectName : STRING;
				strEntryName  : STRING;
				strPSetName   : STRING;
				strFieldName  : STRING): BOOLEAN;
```

```python
def vs.IFC_DMIsPSetFldEmpty(strObjectName, strEntryName, strPSetName, strFieldName):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|strObjectName|STRING|   |
|strEntryName|STRING|   |
|strPSetName|STRING|   |
|strFieldName|STRING|   |

## Examples
```pascal
resultOK := IFC_DMIsPSetFldEmpty('Example', 'Example', 'Example', 'MyRecord');
```
```python
import vs

# Checks if specified Field for IfcEntry's PSet is Empty.
strObjectName = 'Example'
strEntryName = 'Example'
strPSetName = 'Example'
strFieldName = 'MyField'

ok = vs.IFC_DMIsPSetFldEmpty(strObjectName, strEntryName, strPSetName, strFieldName)
if ok:
    vs.Message('IFC_DMIsPSetFldEmpty succeeded')
else:
    vs.Message('IFC_DMIsPSetFldEmpty failed')
```

## Version
Availability: from Vectorworks 2021

## Category
* [IFC](../Categories/IFC.md)
