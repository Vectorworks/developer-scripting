# EditObjectSpecial

## Description
Edit the specified object.

```pascal
PROCEDURE EditObjectSpecial(
				h        : HANDLE;
				editMode : INTEGER);
```

```python
def vs.EditObjectSpecial(h, editMode):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|The object to edit.|
|editMode|INTEGER|The edit mode: 0-Default; 2-Properties; 3-Reshape; 4-Edit group like;|

## Examples
```pascal
EditObjectSpecial(h, 1);
```
```python
import vs

# Edit the specified object.
h = vs.FSActLayer()  # handle to the first selected object on the active layer
editMode = 0

vs.EditObjectSpecial(h, editMode)
```

## Version
Availability: from Vectorworks 2013

## Category
* [Object Editing](../Categories/Object%20Editing.md)
