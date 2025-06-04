# IFC_DMAddField

## Description
Adds a field to current IFC Data Mapping.

```pascal
FUNCTION IFC_DMAddField(
				inStrObjName   : STRING;
				inStrEntryName : STRING;
				inStrFieldName : STRING;
				type           : INTEGER;
				bOptional      : BOOLEAN;
				bEnable        : BOOLEAN;
				bEmpty         : BOOLEAN): BOOLEAN;
```

```python
def vs.IFC_DMAddField(inStrObjName, inStrEntryName, inStrFieldName, type, bOptional, bEnable, bEmpty):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inStrObjName|STRING|   |
|inStrEntryName|STRING|   |
|inStrFieldName|STRING|   |
|type|INTEGER|   |
|bOptional|BOOLEAN|   |
|bEnable|BOOLEAN|   |
|bEmpty|BOOLEAN|   |

## Version
Available from: Vectorworks 2017

## Category
* [IFC](../Categories/IFC.md)
