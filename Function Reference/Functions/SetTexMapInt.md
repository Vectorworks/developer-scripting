# SetTexMapInt

## Description
Set map info for specific part of object. partID is texture part, overall is 3. Selector should be 1 to set the map type integer.

```pascal
PROCEDURE SetTexMapInt(
				h        : HANDLE;
				partID   : LONGINT;
				selector : INTEGER;
				value    : INTEGER);
```

```python
def vs.SetTexMapInt(h, partID, selector, value):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|   |
|partID|LONGINT|   |
|selector|INTEGER|   |
|value|INTEGER|   |

## Remarks
Value is one of the:
<code lang="pas">
kPlaneSpace = 0;
kSphereSpace = 1;
kCylinderSpace = 2;
kAlgorithmicSpace = 3; {Space that wraps around the object most}
</code>

Algorithmic means either the "perimeter" or "roof" mapping type.

## See Also
[GetTexMapInt](GetTexMapInt.md)

## Version
Availability: from Vectorworks14.0

## Category
* [Textures](../Categories/Textures.md)
