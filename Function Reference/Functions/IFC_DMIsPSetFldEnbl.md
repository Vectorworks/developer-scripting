# IFC_DMIsPSetFldEnbl

## Description
Checks if specified Field for IfcEntry's PSet is Enabled.

```pascal
FUNCTION IFC_DMIsPSetFldEnbl(
				strObjectName : STRING;
				strEntryName  : STRING;
				strPSetName   : STRING;
				strFieldName  : STRING): BOOLEAN;
```

```python
def vs.IFC_DMIsPSetFldEnbl(strObjectName, strEntryName, strPSetName, strFieldName):
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
resultOK := IFC_DMIsPSetFldEnbl('Example', 'Example', 'Example', 'MyRecord');
```
```python
import vs

# Checks if specified Field for IfcEntry's PSet is Enabled.
strObjectName = 'Example'
strEntryName = 'Example'
strPSetName = 'Example'
strFieldName = 'MyField'

ok = vs.IFC_DMIsPSetFldEnbl(strObjectName, strEntryName, strPSetName, strFieldName)
if ok:
    vs.Message('IFC_DMIsPSetFldEnbl succeeded')
else:
    vs.Message('IFC_DMIsPSetFldEnbl failed')
```

## Version
Availability: from Vectorworks 2021

## Category
* [IFC](../Categories/IFC.md)
