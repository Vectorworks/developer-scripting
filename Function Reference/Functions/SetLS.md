# SetLS

## Description
<b>Use [[VS:SetLSN| SetLSN]] instead.</b>
Procedure SetLS sets the linestyle of the referenced object.

If the value is in the range 0 to 71, the specified fill pattern is applied as the linestyle; a value in the range of -1 to -8 will apply the specified linestyle.

Fill patterns and their associated constants can be found in the [[VS:Function Reference Appendix#Fill Patterns|VectorScript Appendix]].

```pascal
PROCEDURE SetLS(
				h  : HANDLE;
				ls : INTEGER);
```

```python
def vs.SetLS(h, ls):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|
|ls|INTEGER|Linestyle to apply to object.|

## Remarks
([[User:CBM-c-|_c_]], 2014 Apr. 08):  This Routine can be considered partly obsolete from VW 2013 (VW 18) since it will ignore complex line types. Use [[VS:SetLSN| SetLSN]] instead.

([[User:CBM-c-|_c_]], 2011 May 19): Since VW 2010 the max number of Dash styles increased to 128, thus the limit is now theoretically -128 and not -8. It is to be minded that the function will rise a warning if the dash style index passed doesn't exist. This can happen when users deleted them. 

Thus the secure range to be used is: -1 to -[[VS:NumDashStyles| NumDashStyles]].

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
    cnt :INTEGER;
BEGIN
    PushAttrs;

    TextSize(1);
    TextJust(3);
    TextVerticalAlign(3);

    FOR cnt := -10 TO 71 DO BEGIN
        TextOrigin(-2, cnt);
        CreateText(Concat(cnt));
        MoveTo(0, cnt);
        LineTo(24", cnt);

        SetLS(LNewObj, cnt);
    END;

    PopAttrs;
END;
RUN(Example);
```

```pascal
{ Assigning none (no pattern) to the object pen. }
SetLS(ObjHandle, 0)
```
#### Python ####
```python

```

## See Also
[SetLSN|SetLSN](SetLSN|SetLSN.md) from Vectorworks 2013

## Version
Availability: from All Versions, deprecated from Vectorworks 2013

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
