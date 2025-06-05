# SetUnits

## Description
Procedure SetUnits sets low-level unit values in a VectorWorks document. 

If only one of the units values is to be modified, GetUnits should be called first, and the values retrieved from that call should be passed back into SetUnits. 

To specify a standard units setting with default values, use Units. To specify a standard units setting, but with some modified values, use PrimaryUnit.

**VectorWorks Unit Formats**

| Units Format                | Format Flag |
|-----------------------------|-------------|
| Decimal                     | 0           |
| Fractional                  | 1           |
| Decimal Feet and Inches     | 2           |
| Fractional Feet and Inches  | 3           |

```pascal
PROCEDURE SetUnits(
				fraction   : LONGINT;
				display    : LONGINT;
				format     : INTEGER;
				upi        : REAL;
				name       : STRING;
				squareName : STRING);
```

```python
def vs.SetUnits(fraction, display, format, upi, name, squareName):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|fraction|LONGINT|Stored accuracy for the document.|
|display|LONGINT|Minimum display accuracy for the document.|
|format|INTEGER|Unit format style.|
|upi|REAL|Units per inch.|
|name|STRING|Unit label for displayed values|
|squareName|STRING|Squared unit label for displayed values.|

## Remarks
Sets low-level unit values. If only one of the values is desired to change, GetUnits should be called first, and the values retrieved from that call should be passed back into SetUnits. If a standard unit with default values is desired, the Units procedure should be used, not this one. If a standard unit with some modified values is desired, the PrimaryUnit procedure should be called, not this one.

*sd 8/18/98*

## Examples
#### VectorScript ####
```pascal
SetUnits(4096,64,3,1.0,'&quot;','sq ft');
```
#### Python ####
```python

```

## Version
Availability: from All Versions

## Category
* [Document Settings](../Categories/Document%20Settings.md)
