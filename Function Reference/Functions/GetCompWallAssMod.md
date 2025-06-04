# GetCompWallAssMod

## Description
Gets the wall associated modification of a component in an object.

```pascal
FUNCTION GetCompWallAssMod(
				object                         : HANDLE;
				componentIndex                 : INTEGER;
				VAR wallAssociatedModification : INTEGER): BOOLEAN;
```

```python
def vs.GetCompWallAssMod(object, componentIndex):
    return (BOOLEAN, wallAssociatedModification)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object. Can be a roof face, roof, Roof Style, or the Roof Preferences.|
|componentIndex|INTEGER|The index of the component.|
|wallAssociatedModification|INTEGER|Returns the wall associated modification of the component.  0 - None 1 - Clip walls 2 - Clipped by walls|

## See Also
VS Functions:
[SetCompWallAssMod](SetCompWallAssMod.md)

## Version
Availability: from Vectorworks 2016

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
