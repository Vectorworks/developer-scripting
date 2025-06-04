# GetNumberOfComponents

## Description
Gets the number of components in an object.

```pascal
FUNCTION GetNumberOfComponents(
				obj               : HANDLE;
				VAR numComponents : INTEGER): BOOLEAN;
```

```python
def vs.GetNumberOfComponents(obj):
    return (BOOLEAN, numComponents)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The object. Can be a wall, round wall, slab, Wall Style, Slab Style, the Wall Preferences, or the Slab Preferences.|
|numComponents|INTEGER|Returns the number of components.|

## Version
Availability: from VectorWorks 12.0

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
