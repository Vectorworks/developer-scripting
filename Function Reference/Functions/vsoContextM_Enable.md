# vsoContextM_Enable

## Description
Enable an item in the context menu of the object during kObjOnContextMenuInit event.

```pascal
PROCEDURE vsoContextM_Enable(
				itemID : INTEGER;
				enable : BOOLEAN);
```

```python
def vs.vsoContextM_Enable(itemID, enable):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|itemID|INTEGER|   |
|enable|BOOLEAN|   |

## Examples
```pascal
vsoContextM_Enable(1, TRUE);
```
```python
import vs

# Enable an item in the context menu of the object during
# kObjOnContextMenuInit event.
itemID = 1
enable = True

vs.vsoContextM_Enable(itemID, enable)
```

## Version
Availability: from Vectorworks 2014

## Category
* [Object Events](../Categories/Object%20Events.md)
