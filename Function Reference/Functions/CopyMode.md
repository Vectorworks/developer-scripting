# CopyMode

## Description
Procedure CopyMode sets the transfer mode for the active design layer.  If a sheet layer is active, the procedure has no effect.

<I>Transfer Modes</I><P>
<CENTER>
<TABLE BORDER=0 ALIGN=CENTER CELLSPACING=1 CELLPADDING=3>
<TR> 
<TH ALIGN=CENTER BGCOLOR=#000000><FONT COLOR=#FFFFFF>Transfer Mode</FONT></TH>
<TH ALIGN=CENTER BGCOLOR=#000000><FONT COLOR=#FFFFFF>Index Value</FONT></TH>
</TR>
<TR> 
<TD ALIGN=CENTER BGCOLOR=#CCCCCC>Copy</TD>
<TD ALIGN=CENTER BGCOLOR=#CCCCFF>8</TD>
</TR>
<TR> 
<TD ALIGN=CENTER BGCOLOR=#CCCCCC>OR</TD>
<TD ALIGN=CENTER BGCOLOR=#CCCCFF>9</TD>
</TR>
<TR> 
<TD ALIGN=CENTER BGCOLOR=#CCCCCC>XOR</TD>
<TD ALIGN=CENTER BGCOLOR=#CCCCFF>10</TD>
</TR>
<TR> 
<TD ALIGN=CENTER BGCOLOR=#CCCCCC>BIC</TD>
<TD ALIGN=CENTER BGCOLOR=#CCCCFF>11</TD>
</TR>
<TR> 
<TD ALIGN=CENTER BGCOLOR=#CCCCCC>Inverse Copy</TD>
<TD ALIGN=CENTER BGCOLOR=#CCCCFF>12</TD>
</TR>
<TR> 
<TD ALIGN=CENTER BGCOLOR=#CCCCCC>Inverse OR</TD>
<TD ALIGN=CENTER BGCOLOR=#CCCCFF>13</TD>
</TR>
<TR> 
<TD ALIGN=CENTER BGCOLOR=#CCCCCC>Inverse XOR</TD>
<TD ALIGN=CENTER BGCOLOR=#CCCCFF>14</TD>
</TR>
<TR> 
<TD ALIGN=CENTER BGCOLOR=#CCCCCC>Inverse BIC</TD>
<TD ALIGN=CENTER BGCOLOR=#CCCCFF>15</TD>
</TR>
</TABLE>
</CENTER>

The design layer will only be imaged with the transfer mode on systems which support it, like Windows.  Setting the transfer mode to a mode other than Copy (i.e. 8, Paint mode), when the current layer transparency percentage is 0, will also automatically change the layer transparency percentage to 50.  Similarly, setting the transfer mode to Copy, when the current layer transparency percentage is greater than 0, will also automatically change the layer transparency percentage to 0.  This is to approximately preserve the appearance of the layer on systems that don't support transfer modes, like Quartz on the Mac.

```pascal
PROCEDURE CopyMode(mode : INTEGER);
```

```python
def vs.CopyMode(mode):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|mode|INTEGER|Mode index value.|

## Remarks
Sets the layer transfer mode for the actlve layer.

Valid mode values are:
8 - Copy
9 - OR
10 - XOR
11 - BIC
12 - Inverse Copy
13 - Inverse OR
14 - Inverse XOR
15 - Inverse BIC

This procedure may also set the layer transparency to approximate the given transfer mode on systems that don't support transfer modes.

## See Also
VS Functions:
[SetLayerTransparency](SetLayerTransparency.md)

## Version
Availability: from All Versions

## Category
* [Layers](../Categories/Layers.md)
