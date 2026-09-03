# GetComponentClass

## Description
Gets the class of a component in an object.

```pascal
FUNCTION GetComponentClass(
				obj                : HANDLE;
				componentIndex     : INTEGER;
				VAR componentClass : LONGINT): BOOLEAN;
```

```python
def vs.GetComponentClass(obj, componentIndex):
    return (BOOLEAN, componentClass)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The object. Can be a wall, round wall, slab, Wall Style, Slab Style, the Wall Preferences, or the Slab Preferences.|
|componentIndex|INTEGER|The index of the component.|
|componentClass|LONGINT|Returns the class of the component.|

## Remarks
To get the name of the class, use [Index2Name](Index2Name.md), not [ClassList](ClassList.md) to convert componentClass to a STRING.

## Examples
```pascal
resultOK := GetComponentClass(obj, 1, 2);
```
```python
import vs

# Gets the class of a component in an object.
obj = vs.FSActLayer()  # handle to the first selected object on the active layer
componentIndex = 1

ok, componentClass = vs.GetComponentClass(obj, componentIndex)
vs.Message('GetComponentClass returned: ' + str((ok, componentClass)))
```

## See Also
VS Functions:
[SetComponentClass](SetComponentClass.md)

## Version
Availability: from VectorWorks 2008

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
