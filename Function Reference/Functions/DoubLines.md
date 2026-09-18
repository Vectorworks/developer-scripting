# DoubLines

## Description
_DoubLines is obsolete as of VectorWorks12.5_
Procedure DoubLines sets the line spacing width for double-line tools.

```pascal
PROCEDURE DoubLines(doubleLineDistance : REAL);
```

```python
def vs.DoubLines(doubleLineDistance):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|doubleLineDistance|REAL|Width between lines.|

## Examples
[CreateWallObject2](examples/CreateWallObject2.md)

```pascal
DoubLines(6*upi);
ResetOrientation3D;
SetZVals(0.0,0.0);
ClearCavities;
```
```python
import vs

# 5_ Procedure DoubLines sets the line spacing width for double-line tools.
doubleLineDistance = 1.0

vs.DoubLines(doubleLineDistance)
```

## Version
DoubLines is obsolete as of VectorWorks12.5<P>

Availability: from All Versions

## Category
* [Document Settings](../Categories/Document%20Settings.md)
