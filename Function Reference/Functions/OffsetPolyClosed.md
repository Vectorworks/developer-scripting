# OffsetPolyClosed

## Description
Offsets a polyline or polygon, then uses the original geometry to construct a closed profile.

```pascal
FUNCTION OffsetPolyClosed(
				obj           : HANDLE;
				offset        : REAL;
				smoothCorners : BOOLEAN): HANDLE;
```

```python
def vs.OffsetPolyClosed(obj, offset, smoothCorners):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|   |
|offset|REAL|   |
|smoothCorners|BOOLEAN|   |

## Remarks
'''Notes:''' (ptr - 2020 apr 10)
The offset is always in mm. So please convert your document units to mm:
<code lang="py">
result = vs.OffsetPolyClosed(obj, offset /vs.GetPrefReal(152)*25.4, smoothCorners)
</code>

## Version
Availability: from Vectorworks 2018

## Category
* [Objects - 2D](../Categories/Objects%20-%202D.md)
