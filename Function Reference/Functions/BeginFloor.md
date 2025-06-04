# BeginFloor

## Description
Procedure BeginFloor creates a new floor object in a VectorWorks document. BeginFloor uses 2D object creation procedure calls to define the &quot;template&quot; for the object. 

After specifying object procedure calls to define the floor object, you should call EndGroup to complete the column definition and create the actual object.

```pascal
PROCEDURE BeginFloor(thicknessDistance : REAL);
```

```python
def vs.BeginFloor(thicknessDistance):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|thicknessDistance|REAL|Floor thickness.|

## Examples
==== VectorScript ====
```pascal
BeginFloor(6&quot;);
Rect(1,1,5,5);
EndGroup;
```
==== Python ====
```python
vs.BeginFloor(6)
vs.Rect(1,1,5,5)
vs.EndGroup()
```

## Version
Availability: from MiniCAD4.0

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
