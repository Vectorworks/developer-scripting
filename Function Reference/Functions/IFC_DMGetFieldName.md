# IFC_DMGetFieldName

## Description
Gets indicated field name from current IFC Data Mapping.

```pascal
FUNCTION IFC_DMGetFieldName(
				inStrObjName        : STRING;
				inStrEntryName      : STRING;
				index               : INTEGER;
				VAR outStrFieldName : STRING): BOOLEAN;
```

```python
def vs.IFC_DMGetFieldName(inStrObjName, inStrEntryName, index):
    return (BOOLEAN, outStrFieldName)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inStrObjName|STRING|   |
|inStrEntryName|STRING|   |
|index|INTEGER|   |
|outStrFieldName|STRING|   |

## Version
Available from: Vectorworks 2017

## Category
* [IFC](../Categories/IFC.md)
