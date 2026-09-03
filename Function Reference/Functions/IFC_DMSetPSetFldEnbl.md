# IFC_DMSetPSetFldEnbl

## Description
Sets specified Field for IfcEntry's PSet Enabled.

```pascal
FUNCTION IFC_DMSetPSetFldEnbl(
				strObjectName : STRING;
				strEntryName  : STRING;
				strPSetName   : STRING;
				strFieldName  : STRING;
				bEnable       : BOOLEAN): BOOLEAN;
```

```python
def vs.IFC_DMSetPSetFldEnbl(strObjectName, strEntryName, strPSetName, strFieldName, bEnable):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|strObjectName|STRING|   |
|strEntryName|STRING|   |
|strPSetName|STRING|   |
|strFieldName|STRING|   |
|bEnable|BOOLEAN|   |

## Examples
```pascal
resultOK := IFC_DMSetPSetFldEnbl('Example', 'Example', 'Example', 'MyRecord', TRUE);
```
```python
import vs

# Sets specified Field for IfcEntry's PSet Enabled.
strObjectName = 'Example'
strEntryName = 'Example'
strPSetName = 'Example'
strFieldName = 'MyField'
bEnable = True

ok = vs.IFC_DMSetPSetFldEnbl(strObjectName, strEntryName, strPSetName, strFieldName, bEnable)
if ok:
    vs.Message('IFC_DMSetPSetFldEnbl succeeded')
else:
    vs.Message('IFC_DMSetPSetFldEnbl failed')
```

## Version
Availability: from Vectorworks 2021

## Category
* [IFC](../Categories/IFC.md)
