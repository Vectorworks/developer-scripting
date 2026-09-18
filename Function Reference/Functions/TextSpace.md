# TextSpace

## Description
Procedure TextSpace sets the active spacing for a VectorWorks document. 

**Table - Text Spacing**

| Leading        | Constant |
|----------------|----------|
| Single space   | 2        |
| 1 1/2 space    | 3        |
| Double space   | 4        |

```pascal
PROCEDURE TextSpace(spacing : INTEGER);
```

```python
def vs.TextSpace(spacing):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|spacing|INTEGER|Spacing style for text.|

## Examples
#### VectorScript ####
```pascal
TextSpace(4);
{set the active leading to double space}
```
#### Python ####
```python

```

```pascal
PushAttrs;
{TextFace ([bold]);}
TextFlip (0);
TextRotate (#0);
TextSpace (2);
TextJust (2);
TextVerticalAlign (3);
FillPat (kFPat0);

ForEachObject(LoadSpaceArray, (R IN ['Space']));
SortArray(spaces, space_cnt, 3);
TextFlip(0);
TextRotate(0);
TextSpace(2);
TextVerticalAlign(3);
TextWidth := 0;
for cnt1 := 1 to space_cnt do BEGIN
	CreateText(spaces[cnt1].name);

ForEachObject(AddEmUp, ((R IN ['Space Link'])));
PushAttrs;
TextFlip(0);
TextRotate(0);
TextSpace(2);
TextVerticalAlign(3);
scoreTxt := GetPlugInString(3000);
CreateText(Concat(scoreTxt, Num2Str(0,total)));
PopAttrs;
```
```python
vs.TextSpace(spacing)
```

## Version
Availability: from All Versions

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
