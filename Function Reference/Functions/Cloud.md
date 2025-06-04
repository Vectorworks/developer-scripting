# Cloud

## Description
Draws a cloud. Varies the billows of the clouds randomly between rMin and rMax. The hFactor is the height of each individual arc in the cloud.

```pascal
FUNCTION Cloud(
				h                   : HANDLE;
				rMin                : REAL;
				rMax                : REAL;
				hFactor             : REAL;
				convex              : BOOLEAN;
				removeIntersections : BOOLEAN): HANDLE;
```

```python
def vs.Cloud(h, rMin, rMax, hFactor, convex, removeIntersections):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|   |
|rMin|REAL|   |
|rMax|REAL|   |
|hFactor|REAL|   |
|convex|BOOLEAN|   |
|removeIntersections|BOOLEAN|   |

## Version
Availability: from Vectorworks 2014

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
