# SetOpacityN

```pascal
FUNCTION SetOpacityN(
				h             : HANDLE;
				inPenOpacity  : INTEGER;
				inFillOpacity : INTEGER): BOOLEAN;
```

```python
def vs.SetOpacityN(h, inPenOpacity, inFillOpacity):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|HANDLE of the object|
|inPenOpacity|INTEGER|Pen opacity value to set.|
|inFillOpacity|INTEGER|Fill opacity value to set.|

## Examples
```pascal
status := GetOpacityN(pluginH, penOpacity, fillOpacity);
status := SetOpacityN(cloudH, penOpacity, fillOpacity);
```
```python
import vs

h = vs.FSActLayer()  # handle to the first selected object on the active layer
inPenOpacity = 1
inFillOpacity = 2

ok = vs.SetOpacityN(h, inPenOpacity, inFillOpacity)
if ok:
    vs.Message('SetOpacityN succeeded')
else:
    vs.Message('SetOpacityN failed')
```

## Version
Availability: from Vectorworks 2017

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
