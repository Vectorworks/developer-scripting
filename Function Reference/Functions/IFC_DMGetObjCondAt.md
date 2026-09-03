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

## Examples
```pascal
resultOK := IFC_DMGetObjCondAt(1, 'Example');
```
```python
import vs

# Returns the Object's Condition for specified index in IFC Data Mapping.
index = 1

ok, outStrObjectCondition = vs.IFC_DMGetObjCondAt(index)
vs.Message('IFC_DMGetObjCondAt returned: ' + str((ok, outStrObjectCondition)))
```

## Version
Availability: from Vectorworks 2021

## Category
* [IFC](../Categories/IFC.md)
