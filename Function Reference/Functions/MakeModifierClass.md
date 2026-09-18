# MakeModifierClass

## Description
Creates special class for modifiers (if it not exists).

```pascal
PROCEDURE MakeModifierClass(modifierClass : STRING);
```

```python
def vs.MakeModifierClass(modifierClass):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|modifierClass|STRING|   |

## Examples
```pascal
{Create the polygon for the texture bed.}
if gDraw3D then BEGIN
	MakeModifierClass(GetLocStr(12013, 22));
	h1 := MakePolygon(gPolyHandle);
	SetLSN(h1, 0);
	HMoveBackward(h1, TRUE);
	SetClass(h1, GetLocStr(12013, 22));

{set polygon attributes}
kModifierClass := GetLocStr(12013,22);
IF NOT(ClassExists(kModifierClass)) THEN MakeModifierClass(kModifierClass);

Begin
	kModifierClass := GetLocStr(12013,22);	{ "Site-DTM-Modifier' }
	If Not(ClassExists(kModifierClass)) then MakeModifierClass(kModifierClass);
```
```python
import vs

# Creates special class for modifiers (if it not exists).
modifierClass = 'None'

vs.MakeModifierClass(modifierClass)
```

## Version
Availability: from Vectorworks 2015

## Category
* [SiteModel Interface Library](../Categories/SiteModel%20Interface%20Library.md)
