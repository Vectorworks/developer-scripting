# vsoContextM_GetItem

## Description
Get selected object context menu item during kObjOnContextMenuEvent event.

```pascal
FUNCTION vsoContextM_GetItem : INTEGER;
```

```python
def vs.vsoContextM_GetItem():
    return INTEGER
```

## Examples
```pascal
resultN := vsoContextM_GetItem;
```
```python
import vs

# Get selected object context menu item during kObjOnContextMenuEvent event.
resultN = vs.vsoContextM_GetItem()
vs.Message('vsoContextM_GetItem returned: ' + str(resultN))
```

## Version
Availability: from Vectorworks 2014

## Category
* [Object Events](../Categories/Object%20Events.md)
