# UpdateSymDispCtrlN

## Description
Updates a pre-existing symbol display control in the dialog with a new symbol, rendering mode, view or image component.  The dialog ID and item ID must refer to symbol display control created with CreateSymDispCtrlN.  To show a blank SymbolDisplay control, use an empty string as the symbolName parameter.<BR>
<BR>
<I>Table - Render Modes</I>
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
<I>Table - Components</I>
<CENTER>
<TABLE BORDER=0 ALIGN=CENTER CELLSPACING=1 CELLPADDING=3>
  <TR> 
	<TH ALIGN=CENTER BGCOLOR=#000000><FONT COLOR=#FFFFFF>Component</FONT></TH>
	<TH ALIGN=CENTER BGCOLOR=#000000><FONT COLOR=#FFFFFF>Constant</FONT></TH>
  </TR>
  <TR> 
	<TD ALIGN=CENTER BGCOLOR=#CCCCCC>3D</TD>
	<TD ALIGN=CENTER BGCOLOR=#CCCCFF>0</TD>
  </TR>
  <TR> 
	<TD ALIGN=CENTER BGCOLOR=#CCCCCC>2D</TD>
	<TD ALIGN=CENTER BGCOLOR=#CCCCFF>1</TD>
  </TR>
  <TR> 
	<TD ALIGN=CENTER BGCOLOR=#CCCCCC>2D Cut</TD>
	<TD ALIGN=CENTER BGCOLOR=#CCCCFF>2</TD>
  </TR>
  <TR> 
	<TD ALIGN=CENTER BGCOLOR=#CCCCCC>Not set</TD>
	<TD ALIGN=CENTER BGCOLOR=#CCCCFF>4</TD>
  </TR>
</TABLE>
</CENTER>

```pascal
PROCEDURE UpdateSymDispCtrlN(
				dialogID    : LONGINT;
				itemID      : LONGINT;
				symbolName  : STRING;
				view        : INTEGER;
				renderMode  : INTEGER;
				component   : INTEGER;
				scaleByZoom : BOOLEAN);
```

```python
def vs.UpdateSymDispCtrlN(dialogID, itemID, symbolName, view, renderMode, component, scaleByZoom):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The ID of the dialog in which to create the control.|
|itemID|LONGINT|The item ID of the control.|
|symbolName|STRING|The name of the symbol to display.|
|view|INTEGER|The view in which to display the symbol.|
|renderMode|INTEGER|The render mode in which to display the symbol.|
|component|INTEGER|The image component.|
|scaleByZoom|BOOLEAN|Whether the sizing is done by zoom or layer scale.|

## See Also
VS Functions:
[CreateSymDispCtrlN](CreateSymDispCtrlN.md)

## Version
Availability: from Vectorworks 2019

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
