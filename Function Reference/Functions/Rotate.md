# Rotate

## Description
Procedure Rotate rotates the currently selected objects on the active layer. The rotation angle may be specified in any valid angle format. When a locus is selected with a group of objects, the objects are rotated around the locus. If two or more loci are selected, the objects are rotated around the center of the selected objects.

```pascal
PROCEDURE Rotate(rotationAngle : REAL);
```

```python
def vs.Rotate(rotationAngle):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|rotationAngle|REAL|Rotation angle.|

## Examples
#### VectorScript ####
```pascal
Rotate(45d15'23");
```
#### Python ####
```python

```

## Version
Availability: from All Versions

## Category
* [General Edit](../Categories/General%20Edit.md)
