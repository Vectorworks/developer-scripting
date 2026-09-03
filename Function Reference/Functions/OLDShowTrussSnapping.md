# OLDShowTrussSnapping

## Description
Call this function On Drag event to enable Braceworks snapping while dragging single object

```pascal
FUNCTION OLDShowTrussSnapping : BOOLEAN;
```

```python
def vs.OLDShowTrussSnapping():
    return BOOLEAN
```

## Examples
```pascal
resultOK := OLDShowTrussSnapping;
```
```python
import vs

# Call this function On Drag event to enable Braceworks snapping while
# dragging single object.
ok = vs.OLDShowTrussSnapping()
if ok:
    vs.Message('OLDShowTrussSnapping succeeded')
else:
    vs.Message('OLDShowTrussSnapping failed')
```

## Version
Availability: from Vectorworks 2018

## Category
* [Truss Analysis](../Categories/Truss%20Analysis.md)
