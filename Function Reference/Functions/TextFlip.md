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

## Version
Availability: from All Versions

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
