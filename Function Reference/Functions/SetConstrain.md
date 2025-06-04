# SetConstrain

## Description
Procedure SetConstrain sets the active drawing constraints for the document. Each constraint is represented by an ASCII character identifier; these characters are assembled into a string which determines the constraints to be activated.

<I>VectorWorks Constraint Identifiers</I><P>
<CENTER>
<TABLE BORDER=0 ALIGN=CENTER CELLSPACING=1 CELLPADDING=3>
<TR> 
<TH ALIGN=CENTER BGCOLOR=#000000><FONT COLOR=#FFFFFF>Constraint</FONT></TH>
<TH ALIGN=CENTER BGCOLOR=#000000><FONT COLOR=#FFFFFF>Identifier</FONT></TH>
</TR>
<TR> 
<TD ALIGN=CENTER BGCOLOR=#CCCCCC>Snap To Grid</TD>
<TD ALIGN=CENTER BGCOLOR=#CCCCFF>A</TD>
</TR>
<TR> 
<TD ALIGN=CENTER BGCOLOR=#CCCCCC>Snap To Objects</TD>
<TD ALIGN=CENTER BGCOLOR=#CCCCFF>Q</TD>
</TR>
<TR> 
<TD ALIGN=CENTER BGCOLOR=#CCCCCC>Constrain Angle</TD>
<TD ALIGN=CENTER BGCOLOR=#CCCCFF>S</TD>
</TR>
<TR> 
<TD ALIGN=CENTER BGCOLOR=#CCCCCC>Snap Intersection</TD>
<TD ALIGN=CENTER BGCOLOR=#CCCCFF>W</TD>
</TR>
<TR> 
<TD ALIGN=CENTER BGCOLOR=#CCCCCC>Smart Points</TD>
<TD ALIGN=CENTER BGCOLOR=#CCCCFF>D</TD>
</TR>
<TR> 
<TD ALIGN=CENTER BGCOLOR=#CCCCCC>Snap To Distance</TD>
<TD ALIGN=CENTER BGCOLOR=#CCCCFF>E</TD>
</TR>
<TR> 
<TD ALIGN=CENTER BGCOLOR=#CCCCCC>Smart Edge</TD>
<TD ALIGN=CENTER BGCOLOR=#CCCCFF>F</TD>
</TR>
<TR> 
<TD ALIGN=CENTER BGCOLOR=#CCCCCC>Constrain Tangent</TD>
<TD ALIGN=CENTER BGCOLOR=#CCCCFF>R</TD>
</TR>
</TABLE>
</CENTER>

```pascal
PROCEDURE SetConstrain(str : STRING);
```

```python
def vs.SetConstrain(str):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|str|STRING|Constraint constant string.|

## Examples
==== VectorScript ====
```pascal
SetConstrain('QD');

{activates the snap objects and smart point constraints and deactivates the others}
```
==== Python ====
```python

```

## Version
Availability: from All Versions

## Category
* [Document Settings](../Categories/Document%20Settings.md)
