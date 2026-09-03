# SyncMatrixToBound

## Description
Synchronize the object's matrix with the specified story bound.

```pascal
PROCEDURE SyncMatrixToBound(
				obj     : HANDLE;
				BoundID : INTEGER);
```

```python
def vs.SyncMatrixToBound(obj, BoundID):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The object handle.|
|BoundID|INTEGER|The identifier of the story bound.|

## Examples
```pascal
SyncMatrixToBound(obj, 1);
```
```python
import vs

# Synchronize the object's matrix with the specified story bound.
obj = vs.FSActLayer()  # handle to the first selected object on the active layer
BoundID = 1

vs.SyncMatrixToBound(obj, BoundID)
```

## Version
Availability: from Vectorworks 2013

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
