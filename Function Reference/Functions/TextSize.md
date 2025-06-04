# TextSize

## Description
Procedure TextSize sets the active text size of a VectorWorks document.

Text size is specified in points (1 point = 1/72&quot;). If 0 is specified, then the font size will default to 12 pt text.

```pascal
PROCEDURE TextSize(size : REAL);
```

```python
def vs.TextSize(size):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|size|REAL|Point size of text.|

## Remarks
The size parameter is now a REAL so fractional point sizes can be specified. This should be fully compatible with existing VectorScript code. [9/14/98 - PCP] 

Text size is in page-space and does not take drawing scale into account.  [9/14/98 - PCP]

## Examples
#### VectorScript ####
```pascal
TextSize(18);
{set the active text size to 18 point}
```
#### Python ####
```python

```

## Version
Availability: from All Versions

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
