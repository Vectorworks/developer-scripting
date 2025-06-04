# CreateSymDispCtrlN

## Description
Creates a new symbol display control in the dialog layout.  The control displays the specified symbol in the specified rendering mode and view. Specified image component is used.  The actual size of the symbol is not relevant; it is shown as large as possible in the given height and width (the height to width ratio of the symbol is always preserved).  To show a blank SymbolDisplay control, use an empty string as the symbolName parameter.<BR>
<BR>
<I>Table - Render Modes</I><P>
<CENTER>
<TABLE BORDER=0 ALIGN=CENTER CELLSPACING=1 CELLPADDING=3>
  <TR> 
	<TH ALIGN=CENTER BGCOLOR=#000000><FONT COLOR=#FFFFFF>Render Mode</FONT></TH>
	<TH ALIGN=CENTER BGCOLOR=#000000><FONT COLOR=#FFFFFF>Constant</FONT></TH>
  </TR>
  <TR> 
	<TD ALIGN=CENTER BGCOLOR=#CCCCCC>Wireframe</TD>
	<TD ALIGN=CENTER BGCOLOR=#CCCCFF>0</TD>
  </TR>
  <TR> 
	<TD ALIGN=CENTER BGCOLOR=#CCCCCC>Unshaded Polygon</TD>
	<TD ALIGN=CENTER BGCOLOR=#CCCCFF>2</TD>
  </TR>
  <TR> 
	<TD ALIGN=CENTER BGCOLOR=#CCCCCC>Shaded Polygon</TD>
	<TD ALIGN=CENTER BGCOLOR=#CCCCFF>3</TD>
  </TR>
  <TR> 
	<TD ALIGN=CENTER BGCOLOR=#CCCCCC>Shaded Polygon No Lines</TD>
	<TD ALIGN=CENTER BGCOLOR=#CCCCFF>4</TD>
  </TR>
  <TR> 
	<TD ALIGN=CENTER BGCOLOR=#CCCCCC>Final Shaded Polygon</TD>
	<TD ALIGN=CENTER BGCOLOR=#CCCCFF>5</TD>
  </TR>
  <TR> 
	<TD ALIGN=CENTER BGCOLOR=#CCCCCC>Hidden Line</TD>
	<TD ALIGN=CENTER BGCOLOR=#CCCCFF>6</TD>
  </TR>
  <TR> 
	<TD ALIGN=CENTER BGCOLOR=#CCCCCC>Dashed Hidden Line</TD>
	<TD ALIGN=CENTER BGCOLOR=#CCCCFF>7</TD>
  </TR>
  <TR> 
	<TD ALIGN=CENTER BGCOLOR=#CCCCCC>OpenGL</TD>
	<TD ALIGN=CENTER BGCOLOR=#CCCCFF>11</TD>
  </TR>
  <TR> 
	<TD ALIGN=CENTER BGCOLOR=#CCCCCC>Fast RenderWorks</TD>
	<TD ALIGN=CENTER BGCOLOR=#CCCCFF>12</TD>
  </TR>
  <TR> 
	<TD ALIGN=CENTER BGCOLOR=#CCCCCC>Fast RenderWorks with Shadows</TD>
	<TD ALIGN=CENTER BGCOLOR=#CCCCFF>13</TD>
  </TR>
  <TR> 
	<TD ALIGN=CENTER BGCOLOR=#CCCCCC>Final Quality RenderWorks</TD>
	<TD ALIGN=CENTER BGCOLOR=#CCCCFF>14</TD>
  </TR>
  <TR> 
	<TD ALIGN=CENTER BGCOLOR=#CCCCCC>Custom RenderWorks</TD>
	<TD ALIGN=CENTER BGCOLOR=#CCCCFF>15</TD>
  </TR>
  <TR> 
	<TD ALIGN=CENTER BGCOLOR=#CCCCCC>Artistic RenderWorks</TD>
	<TD ALIGN=CENTER BGCOLOR=#CCCCFF>17</TD>
  </TR>
  <TR> 
	<TD ALIGN=CENTER BGCOLOR=#CCCCCC>Sketch</TD>
	<TD ALIGN=CENTER BGCOLOR=#CCCCFF>18</TD>
  </TR>
</TABLE>
</CENTER>
<BR>
<BR>
<I>Table - Views</I>
<CENTER>
<TABLE BORDER=0 ALIGN=CENTER CELLSPACING=1 CELLPADDING=3>
  <TR> 
	<TH ALIGN=CENTER BGCOLOR=#000000><FONT COLOR=#FFFFFF>View</FONT></TH>
	<TH ALIGN=CENTER BGCOLOR=#000000><FONT COLOR=#FFFFFF>Constant</FONT></TH>
  </TR>
  <TR> 
	<TD ALIGN=CENTER BGCOLOR=#CCCCCC>Top/Plan</TD>
	<TD ALIGN=CENTER BGCOLOR=#CCCCFF>2</TD>
  </TR>
  <TR> 
	<TD ALIGN=CENTER BGCOLOR=#CCCCCC>Front</TD>
	<TD ALIGN=CENTER BGCOLOR=#CCCCFF>3</TD>
  </TR>
  <TR> 
	<TD ALIGN=CENTER BGCOLOR=#CCCCCC>Back</TD>
	<TD ALIGN=CENTER BGCOLOR=#CCCCFF>4</TD>
  </TR>
  <TR> 
	<TD ALIGN=CENTER BGCOLOR=#CCCCCC>Left</TD>
	<TD ALIGN=CENTER BGCOLOR=#CCCCFF>5</TD>
  </TR>
  <TR> 
	<TD ALIGN=CENTER BGCOLOR=#CCCCCC>Right</TD>
	<TD ALIGN=CENTER BGCOLOR=#CCCCFF>6</TD>
  </TR>
  <TR> 
	<TD ALIGN=CENTER BGCOLOR=#CCCCCC>Top</TD>
	<TD ALIGN=CENTER BGCOLOR=#CCCCFF>7</TD>
  </TR>
  <TR> 
	<TD ALIGN=CENTER BGCOLOR=#CCCCCC>Bottom</TD>
	<TD ALIGN=CENTER BGCOLOR=#CCCCFF>8</TD>
  </TR>
  <TR> 
	<TD ALIGN=CENTER BGCOLOR=#CCCCCC>Right Isometric</TD>
	<TD ALIGN=CENTER BGCOLOR=#CCCCFF>9</TD>
  </TR>
  <TR> 
	<TD ALIGN=CENTER BGCOLOR=#CCCCCC>Left Isometric</TD>
	<TD ALIGN=CENTER BGCOLOR=#CCCCFF>10</TD>
  </TR>
  <TR> 
	<TD ALIGN=CENTER BGCOLOR=#CCCCCC>Right Rear Isometric</TD>
	<TD ALIGN=CENTER BGCOLOR=#CCCCFF>11</TD>
  </TR>
  <TR> 
	<TD ALIGN=CENTER BGCOLOR=#CCCCCC>Left Rear Isometric</TD>
	<TD ALIGN=CENTER BGCOLOR=#CCCCFF>12</TD>
  </TR>
  <TR> 
	<TD ALIGN=CENTER BGCOLOR=#CCCCCC>Bottom Right Isometric</TD>
	<TD ALIGN=CENTER BGCOLOR=#CCCCFF>13</TD>
  </TR>
  <TR> 
	<TD ALIGN=CENTER BGCOLOR=#CCCCCC>Bottom Left Isometric</TD>
	<TD ALIGN=CENTER BGCOLOR=#CCCCFF>14</TD>
  </TR>
  <TR> 
	<TD ALIGN=CENTER BGCOLOR=#CCCCCC>Bottom Right Rear Isometric</TD>
	<TD ALIGN=CENTER BGCOLOR=#CCCCFF>15</TD>
  </TR>
  <TR> 
	<TD ALIGN=CENTER BGCOLOR=#CCCCCC>Bottom Left Rear Isometric</TD>
	<TD ALIGN=CENTER BGCOLOR=#CCCCFF>16</TD>
  </TR>
</TABLE>
</CENTER>
<BR>
<BR>
Table - Components:     <BR>
Component			Constant<BR>
&quot;3D&quot; 				0<BR>
&quot;2D&quot;				1<BR>
&quot;2D Cut&quot;			                2<BR>
&quot;Not set&quot;			                4

```pascal
PROCEDURE CreateSymDispCtrlN(
				dialogID    : LONGINT;
				itemID      : LONGINT;
				symbolName  : STRING;
				width       : INTEGER;
				height      : INTEGER;
				margin      : INTEGER;
				view        : INTEGER;
				renderMode  : INTEGER;
				component   : INTEGER;
				scaleByZoom : BOOLEAN);
```

```python
def vs.CreateSymDispCtrlN(dialogID, itemID, symbolName, width, height, margin, view, renderMode, component, scaleByZoom):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The ID of the dialog in which to create the control.|
|itemID|LONGINT|The item ID of the control.|
|symbolName|STRING|The name of the symbol to display.|
|width|INTEGER|The width of the control in pixels.|
|height|INTEGER|The height of the control in pixels.|
|margin|INTEGER|The margin between the border of the control and the symbol in pixels.|
|view|INTEGER|The view in which to display the symbol.|
|renderMode|INTEGER|The render mode in which to display the symbol.|
|component|INTEGER|The image component.|
|scaleByZoom|BOOLEAN|Whether the sizing is done by zoom or layer scale.|

## See Also
VS Functions:
[UpdateSymDispCtrlN](UpdateSymDispCtrlN.md)

## Version
Availability: from Vectorworks 2019

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
