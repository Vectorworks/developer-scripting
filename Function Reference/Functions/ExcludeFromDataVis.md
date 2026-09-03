# ExcludeFromDataVis

## Description
Use this method to exclude the object from Data Visualizations. Graphical attributes of the object will not be overridden.

```pascal
PROCEDURE ExcludeFromDataVis(
				objHandle : HANDLE;
				exclude   : BOOLEAN);
```

```python

def vs.ExcludeFromDataVis(objHandle, exclude):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objHandle|HANDLE|Object handle|
|exclude|BOOLEAN|If TRUE the object will be excluded from Data Visualizations|

## Examples
```pascal
ExcludeFromDataVis(objHandle, TRUE);
```
```python
import vs

# Use this method to exclude the object from Data Visualizations.
objHandle = vs.FSActLayer()  # handle to the first selected object on the active layer
exclude = True

vs.ExcludeFromDataVis(objHandle, exclude)
```

## Version
Availability: from Vectorworks 2025.3

## Category
* [Object Attributes](../Categories/Object Attributes.md)
