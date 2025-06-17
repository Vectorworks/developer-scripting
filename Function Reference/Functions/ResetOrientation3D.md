# ResetOrientation3D

## Description
ResetOrientation3D resets the 3D environment parameters of the active VectorWorks document. 

Call this procedure after 3D object creation to ensure correct orientation and display of the new object in 3D space.

```pascal
PROCEDURE ResetOrientation3D;
```

```python
def vs.ResetOrientation3D():
    return None
```

## Remarks
[[User: CBM-c-| _c_]]: (2021.04.11):

Used in Plug-in Object, '''ResetOrientation''' removes the rotation of a solid, if any, so be careful:
```pascal
Set3DRot(solidHandle, 0, 90, 0, 0, 0, 0);
ResetOrientation3D;
{ in PIO ResetOrientation3D removes the rotation of solidHandle! }
```

## Examples
#### VectorScript ####
```pascal
Poly3D(1,1,0,1.5,1.5,1,2.5,1.5,1,);
ResetOrientation3D;
```
#### Python ####
```python

```

## Version
Availability: from MiniCAD 5.0.2

## Category
* [General Edit](../Categories/General%20Edit.md)
