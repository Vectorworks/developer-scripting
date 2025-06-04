# GetComponentPenColors

## Description
Gets the colors of the pens of a component in an object.

```pascal
FUNCTION GetComponentPenColors(
				obj                   : HANDLE;
				componentIndex        : INTEGER;
				VAR leftPenForeColor  : INTEGER;
				VAR leftPenBackColor  : INTEGER;
				VAR rightPenForeColor : INTEGER;
				VAR rightPenBackColor : INTEGER): BOOLEAN;
```

```python
def vs.GetComponentPenColors(obj, componentIndex):
    return (BOOLEAN, leftPenForeColor, leftPenBackColor, rightPenForeColor, rightPenBackColor)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The object. Can be a wall, round wall, slab, Wall Style, Slab Style, the Wall Preferences, or the Slab Preferences.|
|componentIndex|INTEGER|The index of the component.|
|leftPenForeColor|INTEGER|Returns the fore color of the left pen.|
|leftPenBackColor|INTEGER|Returns the back color of the left pen.|
|rightPenForeColor|INTEGER|Returns the fore color of the right pen.|
|rightPenBackColor|INTEGER|Returns the back color of the right pen.|

## See Also
VS Functions:
[SetComponentPenColors](SetComponentPenColors.md)

## Version
Availability: from VectorWorks 2008

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
