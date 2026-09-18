# SetComponentUsePenClassAttr

## Description
Sets the use class attributes flags of the pens of a component in an object.

```pascal
FUNCTION SetComponentUsePenClassAttr(
				obj                        : HANDLE;
				componentIndex             : INTEGER;
				useLeftPenClassAttributes  : BOOLEAN;
				useRightPenClassAttributes : BOOLEAN): BOOLEAN;
```

```python
def vs.SetComponentUsePenClassAttr(obj, componentIndex, useLeftPenClassAttributes, useRightPenClassAttributes):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The object. Can be a wall, round wall, slab, Wall Style, Slab Style, the Wall Preferences, or the Slab Preferences.|
|componentIndex|INTEGER|The index of the component.|
|useLeftPenClassAttributes|BOOLEAN|Whether or not the component will use class attributes for its left pen.|
|useRightPenClassAttributes|BOOLEAN|Whether or not the component will use class attributes for its right pen.|

## Remarks
CJG 3-23-07

## Examples
```pascal
resultOK := SetComponentUsePenClassAttr(obj, 1, TRUE, FALSE);
```
```python
import vs

# Sets the use class attributes flags of the pens of a component in an object.
obj = vs.FSActLayer()  # handle to the first selected object on the active layer
componentIndex = 1
useLeftPenClassAttributes = True
useRightPenClassAttributes = True

ok = vs.SetComponentUsePenClassAttr(obj, componentIndex, useLeftPenClassAttributes, useRightPenClassAttributes)
if ok:
    vs.Message('SetComponentUsePenClassAttr succeeded')
else:
    vs.Message('SetComponentUsePenClassAttr failed')
```

## See Also
VS Functions:
[GetComponentUsePenClassAttr](GetComponentUsePenClassAttr.md)

## Version
Availability: from VectorWorks 2008

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
