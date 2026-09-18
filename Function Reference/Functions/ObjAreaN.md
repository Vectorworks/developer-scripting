# ObjAreaN

## Description
HObjAreaN, this VS Call is the same as HOBJArea() call but it gives more accurate result when the object is a polyline.

```pascal
FUNCTION ObjAreaN(ObjectHandle : HANDLE): REAL;
```

```python
def vs.ObjAreaN(ObjectHandle ):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|ObjectHandle|HANDLE|   |

## Examples
```pascal
area := HOBJAreaN(object);
```

```pascal
DeckArea := ObjAreaN (LNewObj);
SetRField (ghParm, gPIOName, 'TopSurfaceArea',Concat((Round(DeckArea*100))/100,GetPrefString(178)));

DeckArea := ObjAreaN (OutlinePathHandle);
SetRField (ghParm, gPIOName, 'TopSurfaceArea',Concat((Round(DeckArea*100))/100,GetPrefString(178)));
```
```python
import vs

# HObjAreaN, this VS Call is the same as HOBJArea() call but it gives more
# accurate result when the object is a polyline.
ObjectHandle = vs.FSActLayer()  # handle to the first selected object on the active layer

area = vs.ObjAreaN(ObjectHandle)
vs.Message('ObjAreaN returned: ' + str(area))
```

## Version
Availability: from Vectorworks 2012

## Category
* [Object Info](../Categories/Object%20Info.md)
