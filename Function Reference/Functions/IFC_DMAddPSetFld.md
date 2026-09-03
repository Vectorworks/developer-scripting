# IFC_DMAddPSetFld

## Description
Adds Field to specified IfcEntry's PSet.

```pascal
FUNCTION IFC_DMAddPSetFld(
				strObjectName : STRING;
				strEntryName  : STRING;
				strPSetName   : STRING;
				strFieldName  : STRING;
				type          : INTEGER;
				bOptional     : BOOLEAN;
				bEnable       : BOOLEAN;
				bEmpty        : BOOLEAN): BOOLEAN;
```

```python
def vs.IFC_DMAddPSetFld(strObjectName, strEntryName, strPSetName, strFieldName, type, bOptional, bEnable, bEmpty):
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
|bOptional|BOOLEAN|   |
|bEnable|BOOLEAN|   |
|bEmpty|BOOLEAN|   |

## Examples
```pascal
resultOK := IFC_DMAddPSetFld('Example', 'Example', 'Example', 'MyRecord', 1, TRUE, FALSE, TRUE);
```
```python
import vs

# Adds Field to specified IfcEntry's PSet.
strObjectName = 'Example'
strEntryName = 'Example'
strPSetName = 'Example'
strFieldName = 'MyField'
type = 0
bOptional = True
bEnable = True
bEmpty = True

ok = vs.IFC_DMAddPSetFld(strObjectName, strEntryName, strPSetName, strFieldName, type, bOptional, bEnable, bEmpty)
if ok:
    vs.Message('IFC_DMAddPSetFld succeeded')
else:
    vs.Message('IFC_DMAddPSetFld failed')
```

## Version
Availability: from Vectorworks 2021

## Category
* [IFC](../Categories/IFC.md)
