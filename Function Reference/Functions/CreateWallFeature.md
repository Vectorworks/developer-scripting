# CreateWallFeature

## Description
Creates a Wall Feature in the wall from the profile object.  The Wall Feature can be a projection from the wall or a recess in the wall.

```pascal
FUNCTION CreateWallFeature(
				wall            : HANDLE;
				profile         : HANDLE;
				wallFeatureType : INTEGER): HANDLE;
```

```python
def vs.CreateWallFeature(wall, profile, wallFeatureType):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|wall|HANDLE|The handle to the wall in which to create the Wall Feature.|
|profile|HANDLE|The handle to the object to use as the Wall Feature profile.|
|wallFeatureType|INTEGER|The Wall Feature type.||0 - Projection|1 - Recess|

## Version
Availability: from Vectorworks 2010

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
