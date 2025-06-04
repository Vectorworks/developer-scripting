# SetDimStd

## Description
Procedure SetDimStd changes the default dimension standard of a VectorWorks document. 

Built-in dimension standards are specified using index values of 1 thru 9, corresponding to the dimension standard preference menu. Custom dimensions are specified using indexes 0 thru -8, with 0 being the first custom dimension standard, -1 being the second, and so on.

```pascal
PROCEDURE SetDimStd(whichStandard : INTEGER);
```

```python
def vs.SetDimStd(whichStandard):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|whichStandard|INTEGER|Dimension standard constant.|

## Remarks
Changes the document's default dimension standard.  The whichStandard parameter specifies which dimension standard to change it to. The nine built-in dimension standards are specified using indexes 1 thru 9, and correspond to the ordering in the dimension standard popup menu. Custom dimensions are specified using indexes 0 thru -8, with 0 being the first custom dimension standard, -1 being the second, and so on.

[sd 8/18/98]

## Examples
==== VectorScript ====
```pascal
SetDimStd(2);

{sets the dimension standard to ASME}
```
==== Python ====
```python

```

## Version
Availability: from MiniCAD4.0

## Category
* [Document Settings](../Categories/Document%20Settings.md)
