# GetViewMatrix

## Description
Gets view matrix for layer or viewport object.

```pascal
FUNCTION GetViewMatrix(
				objectHandle                : HANDLE;
				VAR offsetX,offsetY,offsetZ : REAL;
				VAR rotationXAng            : REAL;
				VAR rotationYAng            : REAL;
				VAR rotationZAng            : REAL): BOOLEAN;
```

```python
def vs.GetViewMatrix(objectHandle):
    return (BOOLEAN, offset, rotationXAng, rotationYAng, rotationZAng)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHandle|HANDLE|   |
|offset|REAL|   |
|rotationXAng|REAL|   |
|rotationYAng|REAL|   |
|rotationZAng|REAL|   |

## Version
Availability: from VectorWorks10.5

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
