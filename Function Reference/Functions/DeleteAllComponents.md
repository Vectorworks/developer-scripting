# DeleteAllComponents

## Description
Deletes all components in an object.

```pascal
FUNCTION DeleteAllComponents(obj : HANDLE): BOOLEAN;
```

```python
def vs.DeleteAllComponents(obj):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The object. Can be a wall, round wall, Wall Style, or the Wall Preferences.|

## Remarks
*_c_*: 2016.02.03:  As of VW 2016 it doesn't work on other slab types such as Slab styles, Roof Styles. Use [[VS:DeleteComponent]] looping by index.

## Version
Availability: from VectorWorks 12.5

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
