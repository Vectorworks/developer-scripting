# IFC_DMGetObjCondAt

## Description
Returns the Object's Condition for specified index in IFC Data Mapping.

```pascal
FUNCTION IFC_DMGetObjCondAt(
				index                     : INTEGER;
				VAR outStrObjectCondition : STRING): BOOLEAN;
```

```python
def vs.IFC_DMGetObjCondAt(index):
    return (BOOLEAN, outStrObjectCondition)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|index|INTEGER|   |
|outStrObjectCondition|STRING|   |

## Version
Availability: from Vectorworks 2021

## Category
* [IFC](../Categories/IFC.md)
