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

## Version
Availability: from Vectorworks 2021

## Category
* [IFC](../Categories/IFC.md)
