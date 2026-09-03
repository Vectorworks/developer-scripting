# OLDGetCountLoads

## Description
Returns the loads count of the specified object.

```pascal
FUNCTION OLDGetCountLoads(handle : HANDLE) : INTEGER;
```

```python

def vs.OLDGetCountLoads(handle):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|handle|HANDLE||

## Examples
```pascal
resultN := OLDGetCountLoads(handle);
```
```python
import vs

# Returns the loads count of the specified object.
handle = vs.FSActLayer()  # handle to the first selected object on the active layer

count = vs.OLDGetCountLoads(handle)
vs.Message('OLDGetCountLoads returned: ' + str(count))
```

## Version
Availability: from Vectorworks 2025.3

## Category
* [Truss Analysis](../Categories/Truss Analysis.md)
