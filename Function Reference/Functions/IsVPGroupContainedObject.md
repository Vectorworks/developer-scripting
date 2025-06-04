# IsVPGroupContainedObject

## Description
Determines if specified object is contained within a viewport group, and if so which type of group.

```pascal
FUNCTION IsVPGroupContainedObject(
				objectHandle : HANDLE;
				groupType    : INTEGER): BOOLEAN;
```

```python
def vs.IsVPGroupContainedObject(objectHandle, groupType):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHandle|HANDLE|Handle to object|
|groupType|INTEGER|Type of group containing the object: (1 = Crop, 2 = Annotation, 3 = Cache, 4 = Section)|

## Version
Availability: from VectorWorks11.0

## Category
* [Objects - Groups](../Categories/Objects%20-%20Groups.md)
