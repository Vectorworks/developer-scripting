# SetPrimaryDim

## Description
Procedure SetPrimaryDim sets the primary dimension options for single and dual dimensions.

```pascal
PROCEDURE SetPrimaryDim(
				h         : HANDLE;
				showValue : BOOLEAN;
				boxText   : BOOLEAN;
				leader    : STRING;
				trailer   : STRING;
				precision : LONGINT);
```

```python
def vs.SetPrimaryDim(h, showValue, boxText, leader, trailer, precision):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to dimension.|
|showValue|BOOLEAN|Display dimension value flag.|
|boxText|BOOLEAN|Display box around dimension text flag.|
|leader|STRING|Leader string.|
|trailer|STRING|Trailer string.|
|precision|LONGINT|Precision setting for displayed dimension value.|

## Remarks
Sets dimension values that are specific to the primary portion of a dual dimension. This procedure can also be used for non-dual dimensions.

[sd 8/18/98]

## Examples
#### VectorScript ####
```pascal
SetPrimaryDim(dimHd,TRUE,FALSE,'Approx.','',64);
```
#### Python ####
```python

```

## Version
Availability: from MiniCAD7.0

## Category
* [Document Settings](../Categories/Document%20Settings.md)
