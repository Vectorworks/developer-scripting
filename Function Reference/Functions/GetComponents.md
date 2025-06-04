# GetComponents

## Description
Gets the components of the object.

```pascal
FUNCTION GetComponents(object : HANDLE): HANDLE;
```

```python
def vs.GetComponents(object):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object. Can be a wall, round wall, slab, Wall Style, Slab Style, the Wall Preferences, or the Slab Preferences.|

## Remarks
[ALandsberger 2021/02/08]
The "components" returned here, node 69, is an object that contains the entire array of components.  This is not something VectorScript developers should need to know about or attempt to interact with directly.  That is why it is not documented or exposed.  I believe this call was added for a very specific purpose, and you shouldn't use it unless you know exactly what you are doing.

To interact with wall components via VectorScript, you should use this call to get the number of components of the wall:
[[VS:GetNumberOfComponents| GetNumberOfComponents]]

Then you can reference each component by index, from 1 to however many components there are.  So you could them get and set a component thickness with these calls, for example:
[[VS:GetComponentWidth| GetComponentWidth]]
[[VS:SetComponentWidth| SetComponentWidth]]

There are similar calls for getting and setting each piece of data for a component.

by CGraye (see: VB-179932: VS: GetComponents only returns one of three wall components)

## Version
Availability: from Vectorworks 2015

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
