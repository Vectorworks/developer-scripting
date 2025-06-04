# IFC_DMSetPSetFldOpt

## Description
Sets specified Field for IfcEntry's PSet Optional.

```pascal
FUNCTION IFC_DMSetPSetFldOpt(
				strObjectName : STRING;
				strEntryName  : STRING;
				strPSetName   : STRING;
				strFieldName  : STRING;
				bOptional     : BOOLEAN): BOOLEAN;
```

```python
def vs.IFC_DMSetPSetFldOpt(strObjectName, strEntryName, strPSetName, strFieldName, bOptional):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|strObjectName|STRING|   |
|strEntryName|STRING|   |
|strPSetName|STRING|   |
|strFieldName|STRING|   |
|bOptional|BOOLEAN|   |

## Version
Availability: from Vectorworks 2021

## Category
* [IFC](../Categories/IFC.md)
