# IFC_DMEnablePSet

## Description
Enables/Disables indicated Entry's PSet from current IFC Data Mapping.

```pascal
FUNCTION IFC_DMEnablePSet(
				strObjectName : STRING;
				strEntryName  : STRING;
				strPSetName   : STRING;
				bEnable       : BOOLEAN): BOOLEAN;
```

```python
def vs.IFC_DMEnablePSet(strObjectName, strEntryName, strPSetName, bEnable):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|strObjectName|STRING|   |
|strEntryName|STRING|   |
|strPSetName|STRING|   |
|bEnable|BOOLEAN|   |

## Version
Availability: from Vectorworks 2021

## Category
* [IFC](../Categories/IFC.md)
