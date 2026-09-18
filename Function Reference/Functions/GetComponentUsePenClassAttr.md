# GetComponentUsePenClassAttr

## Description
Gets the use class attributes flags of the pens of a component in an object.

```pascal
FUNCTION GetComponentUsePenClassAttr(
				obj                            : HANDLE;
				componentIndex                 : INTEGER;
				VAR useLeftPenClassAttributes  : BOOLEAN;
				VAR useRightPenClassAttributes : BOOLEAN): BOOLEAN;
```

```python
def vs.GetComponentUsePenClassAttr(obj, componentIndex):
    return (BOOLEAN, useLeftPenClassAttributes, useRightPenClassAttributes)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The object. Can be a wall, round wall, slab, Wall Style, Slab Style, the Wall Preferences, or the Slab Preferences.|
|componentIndex|INTEGER|The index of the component.|
|useLeftPenClassAttributes|BOOLEAN|Returns whether or not the component is using class attributes for its left pen.|
|useRightPenClassAttributes|BOOLEAN|Returns whether or not the component is using class attributes for its right pen.|

## Examples
```pascal
resultOK := GetComponentUsePenClassAttr(obj, 1, TRUE, FALSE);
```
```python
import vs

# Gets the use class attributes flags of the pens of a component in an object.
obj = vs.FSActLayer()  # handle to the first selected object on the active layer
componentIndex = 1

ok, useLeftPenClassAttributes, useRightPenClassAttributes = vs.GetComponentUsePenClassAttr(obj, componentIndex)
vs.Message('GetComponentUsePenClassAttr returned: ' + str((ok, useLeftPenClassAttributes, useRightPenClassAttributes)))
```

## See Also
VS Functions:
[SetComponentUsePenClassAttr](SetComponentUsePenClassAttr.md)

## Version
Availability: from VectorWorks 2008

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
