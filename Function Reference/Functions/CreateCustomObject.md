# CreateCustomObject

## Description
Creates a custom object instance at the specified location and angle of rotation. For the objectName, use the &quot;internal&quot; plug-in name (the one assigned in the plug-in editor), as opposed to the filename (which can be different).

```pascal
FUNCTION CreateCustomObject(
				objectName    : STRING;
				pX,pY         : REAL;
				rotationAngle : REAL): HANDLE;
```

```python
def vs.CreateCustomObject(objectName, p, rotationAngle):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectName|STRING|Name of object.|
|p|REAL|Insertion point of object instance.|
|rotationAngle|REAL|Rotation angle (in degrees) of object instance.|

## Remarks
Like for objects created through CreateCustomObjectPath, they don't resolve as "new objects" after creation with this routine.

## See Also
VS Functions:
[CreateCustomObjectPath](CreateCustomObjectPath.md)

## Version
Availability: from VectorWorks8.5

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
