# SetDimText

## Description
Procedure SetDimText will set the dimension text of the referenced dimension to the specified value. 

The maximum length for dimension text is 60 characters.  The first 30 characters of the specified dimension text string will be displayed in the primary dimension string; the remaining characters will be displayed in the secondary dimension string, if it exists.

```pascal
PROCEDURE SetDimText(
				h             : HANDLE;
				leaderTrailer : STRING);
```

```python
def vs.SetDimText(h, leaderTrailer):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to a dimension object.|
|leaderTrailer|STRING|Dimension text string.|

## Examples
#### VectorScript ####
```pascal
SetDimText(dimHandle,'Length varies');
```
#### Python ####
```python

```

## Version
Availability: from MiniCAD4.0

## Category
* [Dimensions](../Categories/Dimensions.md)
