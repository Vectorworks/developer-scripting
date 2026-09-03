# vsoContextM_Check

## Description
Check an item in the context menu of the object during kObjOnContextMenuInit event.

```pascal
PROCEDURE vsoContextM_Check(
				itemID : INTEGER;
				check  : BOOLEAN);
```

```python
def vs.vsoContextM_Check(itemID, check):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|itemID|INTEGER|   |
|check|BOOLEAN|   |

## Examples
```pascal
vsoContextM_Check(1, TRUE);
```
```python
import vs

# Check an item in the context menu of the object during
# kObjOnContextMenuInit event.
itemID = 1
check = True

vs.vsoContextM_Check(itemID, check)
```

## Version
Availability: from Vectorworks 2014

## Category
* [Object Events](../Categories/Object%20Events.md)
