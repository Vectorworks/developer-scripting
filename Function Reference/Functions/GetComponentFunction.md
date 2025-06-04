# GetComponentFunction

## Description
Gets the function of a component in an object.

```pascal
FUNCTION GetComponentFunction(
				object         : HANDLE;
				componentIndex : INTEGER;
				VAR func       : INTEGER): BOOLEAN;
```

```python
def vs.GetComponentFunction(object, componentIndex):
    return (BOOLEAN, func)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object. Can be a wall, round wall, slab, roof face, roof, Wall Style, Slab Style, Roof Style, the Wall Preferences, the Slab Preferences, or the Roof Preferences.|
|componentIndex|INTEGER|The index of the component.|
|func|INTEGER|Returns the function of the component.  0 - Other 1 - Load-Bearing 2 - Insulation 3 - Inner Finish 4 - Outer Finish 5 - Air Gap|

## See Also
VS Functions:
[SetComponentFunction](SetComponentFunction.md)

## Version
Availability: from Vectorworks 2018

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
