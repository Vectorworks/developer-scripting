# HAngle

## Description
Function HAngle returns the angle of the referenced object.

```pascal
FUNCTION HAngle(h : HANDLE): REAL;
```

```python
def vs.HAngle(h):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|

## Remarks
You can use this routines for getting the angle (slope) of a straight wall as well.
It will also detect the eventual reversion of the wall, consistent with the OIP.

On round walls the eventual reversion is NOT detected. Check if the wall is counterclockwise:
<code lang="pas">
IF NOT GetObjectVariableBool(wallH, 570) THEN
  wallRot := -wallrot;
</code>

For rotated rectangle and oval, the angle is in range [-180;180].

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
BEGIN
CallTool(-202);
Message(HAngle(FSActLayer));
END;
RUN(Example);
```
#### Python ####
```python
def Example():
	vs.CallTool(-202)
	vs.Message(vs.HAngle(vs.FSActLayer()))

Example()
```

## Version
Availability: from All Versions

## Category
* [Object Info](../Categories/Object%20Info.md)
