# IFC_DMGetEntryType

## Description
Returns the IfcEntity type for specified Object in IFC Data Mapping.

```pascal
FUNCTION IFC_DMGetEntryType(
				strObjectName : STRING;
				index         : INTEGER;
				VAR outType   : INTEGER): BOOLEAN;
```

```python
def vs.IFC_DMGetEntryType(strObjectName, index):
    return (BOOLEAN, outType)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|strObjectName|STRING|   |
|index|INTEGER|   |
|outType|INTEGER|   |

## Version
Availability: from Vectorworks 2021

## Category
* [IFC](../Categories/IFC.md)
