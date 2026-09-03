# Min

## Description
Returns the minimum of the two numbers.

```pascal
FUNCTION Min(
				val1 : REAL;
				val2 : REAL): REAL;
```

```python
def vs.Min(val1, val2):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|val1|REAL|   |
|val2|REAL|   |

## Examples
```pascal
BEGIN
	IF dividerDepth < 0 THEN dividerDepth := 0;
	baseWidth := baseWidth - (2 * dividerDepth);
	baseDepth := baseDepth - (2 * dividerDepth);
	maxRadius := Min(baseWidth/2, baseDepth/2);

BEGIN
	gThdLength := Min( kThdLength*gScrewLength, gScrewLength/2 + 1/2" );
	BeginGroup;

{Along the line segment}
len := Distance(xp,yp,x,y);
w := Random * Min(0.8 * len, 0.5 * cVar);
x := x + w * (xp - x) / len;
y := y + w * (yp - y) / len;
```
```python
import vs

# Returns the minimum of the two numbers.
val1 = 1.0
val2 = 2.0

value = vs.Min(val1, val2)
vs.Message('Min returned: ' + str(value))
```

## Version
Availability: from Vectorworks 2014

## Category
* [Math - General](../Categories/Math%20-%20General.md)
