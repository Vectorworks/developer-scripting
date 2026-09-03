# CreateDuplicateObjN

## Description
Duplicates the specified object and inserts the new  object into the container.  If container is nil, the new object will be inserted in the active container (Functionality of CreateDuplicateObject). This functions add an extra input parameter to maintain height relative to the specified layer.

```pascal
FUNCTION CreateDuplicateObjN(
				objectToDuplicate             : HANDLE;
				containerHandle               : HANDLE;
				maintainHeightRelativeToLayer : BOOLEAN): HANDLE;
```

```python
def vs.CreateDuplicateObjN(objectToDuplicate, containerHandle, maintainHeightRelativeToLayer):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectToDuplicate|HANDLE|   |
|containerHandle|HANDLE|   |
|maintainHeightRelativeToLayer|BOOLEAN|   |

## Examples
```pascal
	BEGIN
		IF I > steps-2 THEN	clipflag := 2;
{		incr := incr / 3;}
		incr := incr / 1.5;
 		hBoundary := CreateDuplicateObjN(poly_h, NIL, TRUE);
```
```python
import vs

# Duplicates the specified object and inserts the new object into the container.
objectToDuplicate = vs.FSActLayer()  # handle to the first selected object on the active layer
containerHandle = vs.NextSObj(vs.FSActLayer())  # handle to the next selected object
maintainHeightRelativeToLayer = True

objHandle = vs.CreateDuplicateObjN(objectToDuplicate, containerHandle, maintainHeightRelativeToLayer)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from Vectorworks 2020

## Category
* [Object Editing](../Categories/Object%20Editing.md)
