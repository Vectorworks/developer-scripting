# RevolveWithRail

## Description
Creates a NURBS surface or a group of surfaces by revolving a profile about an axis and following a rail guide curve on a plane perpendicular to the plane containing the axis and the profile.

```pascal
FUNCTION RevolveWithRail(
				profileH : HANDLE;
				railH    : HANDLE;
				axisH    : HANDLE): HANDLE;
```

```python
def vs.RevolveWithRail(profileH, railH, axisH):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|profileH|HANDLE|Handle to a NURBS curve to be used as the profile object.|
|railH|HANDLE|Handle to a NURBS curve to be used as the rail guide object|
|axisH|HANDLE|Handle to a linear NURBS curve about which the|profile would be revolved|

## Version
Availability: from VectorWorks10.0

## Category
* [Objects - NURBS](../Categories/Objects%20-%20NURBS.md)
