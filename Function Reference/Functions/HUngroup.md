# HUngroup

## Description
Decomposes the referenced group into component objects.

```pascal
PROCEDURE HUngroup(h : HANDLE);
```

```python
def vs.HUngroup(h):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to group.|

## Remarks
Example, from Beat Fleischli:
```pascal
PROCEDURE ChangeGroupClass;
CONST
oldClass = 'Keine-2';
newClass = 'Keine';
VAR
oHd, lHd :HANDLE;
actClass, activeLayer :STRING;

PROCEDURE DoIt(h :HANDLE);
BEGIN
IF (GetType(h) = 11) AND (GetClass(h) = oldClass) THEN BEGIN
lHd := GetParent(h);
WHILE GetType(lHd) <> 31 DO lHd := GetParent(lHd);
Layer(GetLName(lHd));
DSelectAll;
oHd := FInGroup(h);
WHILE oHd <> NIL DO BEGIN
SetSelect(oHd);
oHd := NextObj(oHd);
END;
HUngroup(h);
Group;
DSelectAll;
END;
END;

BEGIN
actClass := ActiveClass;
activeLayer := GetLName(ActLayer);
NameClass(newClass);
ForEachObject(DoIt,(T=Group));
NameClass(actClass);
Layer(activeLayer);
END;
RUN(ChangeGroupClass);
```

## Version
Availability: from VectorWorks8.5

## Category
* [Objects - Groups](../Categories/Objects%20-%20Groups.md)
