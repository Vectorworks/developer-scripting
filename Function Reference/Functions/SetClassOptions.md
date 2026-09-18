# SetClassOptions

## Description
Sets class visibility setting for the active document.

<CENTER>
<TABLE BORDER=0 ALIGN=CENTER CELLSPACING=1 CELLPADDING=3>
<TR> 
<TH ALIGN=CENTER BGCOLOR=#000000><FONT COLOR=#FFFFFF>Visibility</FONT></TH>
<TH ALIGN=CENTER BGCOLOR=#000000><FONT COLOR=#FFFFFF>Index</FONT></TH>
</TR>
<TR> 
<TD ALIGN=CENTER BGCOLOR=#CCCCCC>Active Only</TD>
<TD ALIGN=CENTER BGCOLOR=#CCCCFF>1</TD>
</TR>
<TR> 
<TD ALIGN=CENTER BGCOLOR=#CCCCCC>Gray Others</TD>
<TD ALIGN=CENTER BGCOLOR=#CCCCFF>2</TD>
</TR>
<TR> 
<TD ALIGN=CENTER BGCOLOR=#CCCCCC>Gray/Snap Others</TD>
<TD ALIGN=CENTER BGCOLOR=#CCCCFF>6</TD>
</TR>
<TR> 
<TD ALIGN=CENTER BGCOLOR=#CCCCCC>Show Others</TD>
<TD ALIGN=CENTER BGCOLOR=#CCCCFF>3</TD>
</TR>
<TR> 
<TD ALIGN=CENTER BGCOLOR=#CCCCCC>Show/Snap Others</TD>
<TD ALIGN=CENTER BGCOLOR=#CCCCFF>4</TD>
</TR>
<TR> 
<TD ALIGN=CENTER BGCOLOR=#CCCCCC>Show/Snap/Modify Others</TD>
<TD ALIGN=CENTER BGCOLOR=#CCCCFF>5</TD>
</TR>
</TABLE>
</CENTER>

```pascal
PROCEDURE SetClassOptions(classOpts : INTEGER);
```

```python
def vs.SetClassOptions(classOpts):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|classOpts|INTEGER|New class visibility setting.|

## Examples
```pascal
		Layer(GetLName(temp_h));
		ShowLayer;
		temp_h := NextObj(temp_h);
	END;
	SetClassOptions(5);
	for i := 1 to ClassNum DO ShowClass(ClassList(i));
END;

BEGIN
		SetClassOptions(5);
		SetLayerOptions(5);
		DSelectAll;
		Layer(kStrErrorLayer);
		SetLayerOptions(1);

{set the Class Setting to Show/Snap/Modify Others}
SetClassOptions (5);
```
```python
curClassVis = vs.GetClassOptions()
vs.SetClassOptions( 5 ) #Set to Show/Snap/Modify to fix VB-116777
```

## Version
Availability: from VectorWorks8.5

## Category
* [Classes](../Categories/Classes.md)
