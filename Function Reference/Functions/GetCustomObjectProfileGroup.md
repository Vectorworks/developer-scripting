# GetCustomObjectProfileGroup

## Description
Returns a handle to the profile group of a path custom object.

A path object has two &quot;containers&quot; for storing subordinate objects: the path, and the profile. As an example, if a path object is going to do an extrude along path, it will store the path in the path container, and the shape to be extruded in the profile container. The code within the object will then supply the handles to the path and the profile to the CreateExtrudeAlongPath call.

```pascal
FUNCTION GetCustomObjectProfileGroup(objectHand : HANDLE): HANDLE;
```

```python
def vs.GetCustomObjectProfileGroup(objectHand):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHand|HANDLE|Handle to path custom object.|

## See Also
VS Functions:
[SetCustomObjectProfileGroup](SetCustomObjectProfileGroup.md)

## Version
Availability: from VectorWorks8.5

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
