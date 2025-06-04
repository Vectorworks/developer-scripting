# IFC_DMGetEntryName

## Description
Gets the name of entry for indicated index from current IFC Data Mapping.

```pascal
FUNCTION IFC_DMGetEntryName(
				index            : INTEGER;
				inStrObjName     : STRING;
				VAR outStrResult : STRING): BOOLEAN;
```

```python
def vs.IFC_DMGetEntryName(index, inStrObjName):
    return (BOOLEAN, outStrResult)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|index|INTEGER|   |
|inStrObjName|STRING|   |
|outStrResult|STRING|   |

## Version
Available from: Vectorworks 2017

## Category
* [IFC](../Categories/IFC.md)
