# GetCompWallAssBound

## Description
Gets the wall associated bound of a component in an object.

```pascal
FUNCTION GetCompWallAssBound(
				object                  : HANDLE;
				componentIndex          : INTEGER;
				VAR wallAssociatedBound : INTEGER): BOOLEAN;
```

```python
def vs.GetCompWallAssBound(object, componentIndex):
    return (BOOLEAN, wallAssociatedBound)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object. Can be a roof face, roof, Roof Style, or the Roof Preferences.|
|componentIndex|INTEGER|The index of the component.|
|wallAssociatedBound|INTEGER|Returns the wall associated bound of the component.  0 - Inner face 1 - Outer face of inner component 2 - Inner face of core 3 - Center of core 4 - Outer face of core 5 - Inner face of outer component 6 - Roof edge 7 - Roof axis line|

## See Also
VS Functions:
[SetCompWallAssBound](SetCompWallAssBound.md)

## Version
Availability: from Vectorworks 2016

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
