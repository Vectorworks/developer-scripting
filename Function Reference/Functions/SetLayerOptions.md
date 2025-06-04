# SetLayerOptions

## Description
Sets layer visibility setting for the active document.

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
PROCEDURE SetLayerOptions(layerOpts : INTEGER);
```

```python
def vs.SetLayerOptions(layerOpts):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|layerOpts|INTEGER|New layer visibility setting for document.|

## See Also
VS Functions:
[GetLayerOptions](GetLayerOptions.md)

## Version
Availability: from VectorWorks8.5

## Category
* [Layers](../Categories/Layers.md)
