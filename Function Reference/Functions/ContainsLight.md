# ContainsLight

## Description
Function ContainsLight returns TRUE if the referenced object contains a light.  This function works with container objects such as groups, symbols, layers, etc.

```pascal
FUNCTION ContainsLight(containerObject : HANDLE): BOOLEAN;
```

```python
def vs.ContainsLight(containerObject):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|containerObject|HANDLE|Handle to object.|

## Remarks
Returns true if object contains a light object in it.  This function works for container-type objects (groups, symbols, layers, etc.).

## Version
Availability: from VectorWorks8.0

## Category
* [Objects - Lights](../Categories/Objects%20-%20Lights.md)
