# TextFlip

## Description
Procedure TextFlip flips newly created text vertically or horizontally. Parameter FlipType specifies the flip effect to be applied to the text.

**Table - Text Flip Style**

| Flip Style                        | Constant |
|-----------------------------------|----------|
| No reflection                     | 0        |
| Horizontal reflection thru origin | 1        |
| Vertical reflection thru origin   | 2        |

```pascal
PROCEDURE TextFlip(FlipType : INTEGER);
```

```python
def vs.TextFlip(FlipType):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|FlipType|INTEGER|Text flip setting for text.|

## Examples
#### VectorScript ####
```pascal
TextFlip(1);
CreateText('Sample text string');
```
#### Python ####
```python

```

```pascal
{ ----- set the text parameters  ----- }
TextSize (gCellLabelSize);
PushAttrs;
{TextFace ([bold]);}
TextFlip (0);
TextRotate (#0);
TextSpace (2);
TextJust (2);
TextVerticalAlign (3);

BEGIN
	TextFlip( 2 );
	textAlignTop := NOT textAlignTop;
END;

ALLOCATE spaces [1..temp_i];
space_cnt := 0;
ForEachObject(LoadSpaceArray, (R IN ['Space']));
SortArray(spaces, space_cnt, 3);
TextFlip(0);
TextRotate(0);
TextSpace(2);
TextVerticalAlign(3);
TextWidth := 0;
```
```python
vs.TextFlip(FlipType)
```

## Version
Availability: from All Versions

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
