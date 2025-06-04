# SetObjArrow

## Description
Procedure SetObjArrow sets the arrow style parameters for the indicated object.

<I>Marker Styles</I><P>
<CENTER>
<TABLE BORDER=0 ALIGN=CENTER CELLSPACING=1 CELLPADDING=3>
<TR> 
<TH ALIGN=CENTER BGCOLOR=#000000><FONT COLOR=#FFFFFF>Marker 
Style</FONT></TH>
<TH ALIGN=CENTER BGCOLOR=#000000><FONT COLOR=#FFFFFF>Constant</FONT></TH>
</TR>
<TR> 
<TD ALIGN=CENTER BGCOLOR=#CCCCCC>Filled Arrow</TD>
<TD ALIGN=CENTER BGCOLOR=#CCCCFF>0</TD>
</TR>
<TR> 
<TD ALIGN=CENTER BGCOLOR=#CCCCCC>Empty Arrow</TD>
<TD ALIGN=CENTER BGCOLOR=#CCCCFF>1</TD>
</TR>
<TR> 
<TD ALIGN=CENTER BGCOLOR=#CCCCCC>Open Arrow</TD>
<TD ALIGN=CENTER BGCOLOR=#CCCCFF>2</TD>
</TR>
<TR> 
<TD ALIGN=CENTER BGCOLOR=#CCCCCC>Filled Circle</TD>
<TD ALIGN=CENTER BGCOLOR=#CCCCFF>3</TD>
</TR>
<TR> 
<TD ALIGN=CENTER BGCOLOR=#CCCCCC>Empty Circle</TD>
<TD ALIGN=CENTER BGCOLOR=#CCCCFF>4</TD>
</TR>
<TR> 
<TD ALIGN=CENTER BGCOLOR=#CCCCCC>Slash</TD>
<TD ALIGN=CENTER BGCOLOR=#CCCCFF>5</TD>
</TR>
<TR> 
<TD ALIGN=CENTER BGCOLOR=#CCCCCC>Cross</TD>
<TD ALIGN=CENTER BGCOLOR=#CCCCFF>6</TD>
</TR>
</TABLE>
</CENTER>

```pascal
PROCEDURE SetObjArrow(
				obj   : HANDLE;
				style : INTEGER;
				size  : REAL;
				angle : INTEGER;
				start : BOOLEAN;
				end   : BOOLEAN);
```

```python
def vs.SetObjArrow(obj, style, size, angle, start, end):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The indicated object.|
|style|INTEGER|The arrow style.|
|size|REAL|The arrow size in inches measured in page space.|
|angle|INTEGER|The arrow angle (in degrees).|
|start|BOOLEAN|Whether the start point of the object has an arrow.|
|end|BOOLEAN|Whether the endpoint of the object has an arrow.|

## Remarks
OBSOLETE for VW2008: Use SetObjBeginningMarker and/or SetObjEndMarker instead.
Style indicates the index of the arrow style to be used.

Size is in page-inches. Legal values are 0.0 to 2.0.

Angle is in degrees.

## Examples
==== VectorScript ====
```pascal
PROCEDURE SetObjArrowValues;
BEGIN
SetObjArrow(FSActLayer, 1, .25, 15, TRUE, TRUE);
END;
RUN(SetObjArrowValues);
```
==== Python ====
```python

```

## Version
SetObjArrow is obsolete as of VectorWorks13.0<P>


Availability: from VectorWorks10.0

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
