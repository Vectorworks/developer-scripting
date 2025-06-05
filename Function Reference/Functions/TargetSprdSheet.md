# TargetSprdSheet

## Description
Procedure TargetSprdSheet selects the referenced worksheet as the active worksheet for the document. The worksheet is not opened onscreen.

```pascal
PROCEDURE TargetSprdSheet(h : HANDLE);
```

```python
def vs.TargetSprdSheet(h):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to worksheet.|

## Remarks
This selects a spreadsheet for use by the script.  It does not open the spreadsheet. [sd 8/18/98]

## See Also
[SetTopVisibleWS| SetTopVisibleWS](SetTopVisibleWS|%20SetTopVisibleWS.md)

## Version
TargetSprdSheet is obsolete as of VectorWorks 9.0, see new [ SetTopVisibleWS](SetTopVisibleWS.md).

Availability: from VectorWorks 8.0

## Category
* [Worksheets](../Categories/Worksheets.md)
