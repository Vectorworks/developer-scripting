# IsPlanarObj

```pascal
FUNCTION IsPlanarObj(
				object    : HANDLE;
				VAR refID : LONGINT): BOOLEAN;
```

```python
def vs.IsPlanarObj(object):
    return (BOOLEAN, refID)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|Object to test|
|refID|LONGINT|If object is planar, returns the planar refID of its plane|

## Remarks
This function always seems to return 0 for refID, no matter which plane the object being tested is located.
Use [GetPlanarRef](GetPlanarRef.md) instead to find the planar refID of a given planar object.

## Version
Availability: from Vectorworks 2016

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
