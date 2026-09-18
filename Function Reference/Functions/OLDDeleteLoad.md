# OLDDeleteLoad

## Description
Deletes the load of the specified object, if load with such index exists.

```pascal
PROCEDURE OLDDeleteLoad(
				handle    : HANDLE;
				loadIndex : INTEGER);
```

```python

def vs.OLDDeleteLoad(handle, loadIndex):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|handle|HANDLE||
|loadIndex|INTEGER||

## Examples
```pascal
OLDDeleteLoad(handle, 1);
```
```python
import vs

# Deletes the load of the specified object, if load with such index exists.
handle = vs.FSActLayer()  # handle to the first selected object on the active layer
loadIndex = 1

vs.OLDDeleteLoad(handle, loadIndex)
```

## Version
Availability: from Vectorworks 2025.3

## Category
* [Truss Analysis](../Categories/Truss Analysis.md)
