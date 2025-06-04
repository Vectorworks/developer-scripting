# IFC_DMAddPSetInEntry

## Description
Adds a Pset to indicated object's entry from current Data Mapping.

```pascal
FUNCTION IFC_DMAddPSetInEntry(
				inStrObjName       : STRING;
				inStrEntryName     : STRING;
				inStrPsetName      : STRING;
				bEnable            : BOOLEAN;
				inStrPsetCondition : STRING): BOOLEAN;
```

```python
def vs.IFC_DMAddPSetInEntry(inStrObjName, inStrEntryName, inStrPsetName, bEnable, inStrPsetCondition):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inStrObjName|STRING|   |
|inStrEntryName|STRING|   |
|inStrPsetName|STRING|   |
|bEnable|BOOLEAN|   |
|inStrPsetCondition|STRING|   |

## Version
Availability: from Vectorworks 2021

## Category
* [IFC](../Categories/IFC.md)
