# ConvertToPolygon

## Description
Converts object to polygon.

```pascal
FUNCTION ConvertToPolygon(
				h          : HANDLE;
				resolution : INTEGER): HANDLE;
```

```python
def vs.ConvertToPolygon(h, resolution):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|   |
|resolution|INTEGER|   |

## Remarks
Notes: (RMullin - 2020 Mar 03)
- Setting "resolution" higher creates more vertices. Magic numbers for "resolution" are [0, 8, 16, 32, 64, 128, 256, 512].
 - Integer values between the numbers in this list generate duplicate results.
 - Values outside this range do not appear to affect the number of vertices generated.
- This function creates a duplicate object, so you don't have to duplicate the object beforehand if you want to retain the original object.
- If the original is selected, the duplicate will be selected, and vice versa.

## Version
Availability: from Vectorworks 2014

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
