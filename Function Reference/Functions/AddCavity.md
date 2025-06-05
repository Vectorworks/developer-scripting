# AddCavity

## Description
Procedure AddCavity creates a wall cavity in a new wall object. The newly defined cavity becomes the default for all subsequently defined walls.

To apply a bitmap fill pattern, use positive value corresponding to the index  of the bitmap pattern.  To apply a vector fill pattern, use the negative of the vector fill index (index * -1). 

Fill patterns and their associated constants can be found in the [VectorScript Appendix](../Appendix/pages/Appendix%20E%20-%20Miscellaneous%20Selectors.md#fill-patterns).

```pascal
PROCEDURE AddCavity(
				pair             : BOOLEAN;
				leftOffDistance  : REAL;
				rightOffDistance : REAL;
				pairFill         : LONGINT);
```

```python
def vs.AddCavity(pair, leftOffDistance, rightOffDistance, pairFill):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|pair|BOOLEAN|Double line display mode.|
|leftOffDistance|REAL|Left edge offset from wall centerline.|
|rightOffDistance|REAL|Right edge offset from wall centerline.|
|pairFill|LONGINT|Fill index for filled cavities.|

## Remarks
(NZH 5-9-05) OBSOLETE for Version 12: Use [InsertNewComponent](InsertNewComponent.md) instead.

## Examples
#### VectorScript ####
```pascal
{ Create wall object with 1" wide cavity using black pattern fill.}
DoubLines(6");
AddCavity(True, 1", 2", 2);
Wall(0, 1, 9, 1);

{ Create wall object with 1" wide cavity using a custom hatch fill.}
DoubLines(6");
AddCavity(True, 1", 2", -Name2Index('My Hatch'));
Wall(0, 1, 9, 1);
```

#### Python ####
```python
#{ Create wall object with 1" wide cavity using black pattern fill.}
vs.DoubLines(6)
vs.AddCavity(1, 1, 2, 2)
vs.Wall(0, 1, 9, 1)

#{ Create wall object with 1" wide cavity using a custom hatch fill.}
vs.DoubLines(6)
vs.AddCavity(1, 1, 2, -vs.Name2Index('My Hatch'))
vs.Wall(0, 1, 9, 1)
```

## See Also
VS Functions:
[InsertNewComponent | InsertNewComponent](InsertNewComponent%20| InsertNewComponent.md)

## Version
AddCavity is obsolete as of VectorWorks 12.0.

Availability: from MiniCAD 4.0

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
