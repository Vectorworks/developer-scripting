# GetComponentName

## Description
Gets the name of a component in an object.

```pascal
FUNCTION GetComponentName(
				obj            : HANDLE;
				componentIndex : INTEGER): STRING;
```

```python
def vs.GetComponentName(obj, componentIndex):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The object. Can be a wall, round wall, slab, Wall Style, Slab Style, the Wall Preferences, or the Slab Preferences.|
|componentIndex|INTEGER|The index of the component, 1-based.|

## See Also
VS Functions:
[SetComponentName](SetComponentName.md)

## Version
Availability: from VectorWorks 2008

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
