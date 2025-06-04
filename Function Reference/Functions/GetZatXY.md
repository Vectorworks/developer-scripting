# GetZatXY

## Description
Returns the Z elevation of a point X,Y on the specified object. If hObject = NIL then searches all visible objects; hObject = layer - all objects on the layer

```pascal
FUNCTION GetZatXY(
				hObject  : HANDLE;
				X        : REAL;
				Y        : REAL;
				VAR outZ : REAL): BOOLEAN;
```

```python
def vs.GetZatXY(hObject, X, Y):
    return (BOOLEAN, outZ)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|   |
|X|REAL|   |
|Y|REAL|   |
|outZ|REAL|   |

## Version
Availability: from Vectorworks 2014

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
