# IFC_DMGetFieldsCount

## Description
Gets fields count for indicated entry from current IFC Data Mapping.

```pascal
FUNCTION IFC_DMGetFieldsCount(
				inStrObjName   : STRING;
				inStrEntryName : STRING;
				VAR outCount   : INTEGER): BOOLEAN;
```

```python
def vs.IFC_DMGetFieldsCount(inStrObjName, inStrEntryName):
    return (BOOLEAN, outCount)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inStrObjName|STRING|   |
|inStrEntryName|STRING|   |
|outCount|INTEGER|   |

## Version
Available from: Vectorworks 2017

## Category
* [IFC](../Categories/IFC.md)
