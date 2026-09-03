# vsoContextM_AddSep

## Description
Add a separator to the context menu of the object during kObjOnContextMenuInit event.

```pascal
PROCEDURE vsoContextM_AddSep(itemID : INTEGER);
```

```python
def vs.vsoContextM_AddSep(itemID):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|itemID|INTEGER|   |

## Examples
```pascal
vsoContextM_AddSep(1);
```
```python
import vs

# Add a separator to the context menu of the object during
# kObjOnContextMenuInit event.
itemID = 1

vs.vsoContextM_AddSep(itemID)
```

## Version
Availability: from Vectorworks 2014

## Category
* [Object Events](../Categories/Object%20Events.md)
