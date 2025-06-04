# MoveTo

## Description
Sets the position of the graphics pen in the VectorWorks document using absolute coordinate values. The parameter specifies the X-Y coordinate location where the pen should be moved.

```pascal
PROCEDURE MoveTo(pX,pY : REAL);
```

```python
def vs.MoveTo(p):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|p|REAL|X-Y coordinate location.|

## Remarks
If you want to move a relative distance from the existing pen position, use Move.

## Examples
==== VectorScript ====
```pascal
MoveTo(4,3);
{moves the graphics pen to (4,3)}
```
==== Python ====
```python
vs.MoveTo(4, 3)
```

## See Also
VS Functions:
[Move](Move.md)

## Version
Availability: from All Versions

## Category
* [Command](../Categories/Command.md)
