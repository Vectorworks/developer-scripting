# GetClUseTexture

## Description
Function GetClUseTexture returns whether a classes' texture attributes will be used at object creation.

```pascal
FUNCTION GetClUseTexture(className : STRING): BOOLEAN;
```

```python
def vs.GetClUseTexture(className):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|className|STRING|Class name.|

## Remarks
Returns whether the class is set to use its texture attributes at object creation.


Respective [SetClUseTexture](SetClUseTexture.md).

## Version
Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
