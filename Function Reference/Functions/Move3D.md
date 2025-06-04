# Move3D

## Description
Procedure Move3D moves the most recently created three-dimensional object a relative distance from it's original location. The object is moved relative to its center.

```pascal
PROCEDURE Move3D(
				xDistance : REAL;
				yDistance : REAL;
				zDistance : REAL);
```

```python
def vs.Move3D(xDistance, yDistance, zDistance):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|xDistance|REAL|X offset distance.|
|yDistance|REAL|Y offset distance.|
|zDistance|REAL|Z offset ditance.|

## Examples
#### VectorScript ####
```pascal
BeginXtrd(0',2&quot;);
Rect(0&quot;,1&quot;,1&quot;,0&quot;);
EndXtrd;
Move3D(3&quot;,1&quot;,2&quot;);
```
#### Python ####
```python

```

## Version
Availability: from All Versions

## Category
* [Object Editing](../Categories/Object%20Editing.md)
