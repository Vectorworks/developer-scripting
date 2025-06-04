# GetSecondaryUnitInfo

## Description
Procedure GetSecondaryUnitInfo sets the secondary unit parameters for the active document.

```pascal
PROCEDURE GetSecondaryUnitInfo(
				VAR style    : INTEGER;
				VAR dimPrec  : LONGINT;
				VAR format   : INTEGER;
				VAR showMark : BOOLEAN;
				VAR dispFrac : BOOLEAN);
```

```python
def vs.GetSecondaryUnitInfo():
    return (style, dimPrec, format, showMark, dispFrac)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|style|INTEGER|Returns active secondary units style.|
|dimPrec|LONGINT|Returns dimension precision.|
|format|INTEGER|Returns decimal formatting.|
|showMark|BOOLEAN|Returns unit mark display setting.|
|dispFrac|BOOLEAN|Returns fractional display setting.|

## Remarks
Returns settings information for secondary units.


See &lt;a href=main.php?name=GetPrimaryUnitInfo&gt;GetPrimaryUnitInfo&lt;/a&gt; for details on changes in version 9, and again in version 12.

## Version
Availability: from VectorWorks8.0

## Category
* [Units](../Categories/Units.md)
