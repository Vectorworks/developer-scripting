# GetPhaseStatus

## Description
Function GetPhaseStatus takes in a handle and returns a string indicating the handle's phasing status in the active phase.<BR>
<BR>
<I>Table - Phasing Statuses</I><P>
<CENTER>
<TABLE BORDER=0 ALIGN=CENTER CELLSPACING=1 CELLPADDING=3>
  <TR> 
	<TH ALIGN=CENTER BGCOLOR=#000000><FONT COLOR=#FFFFFF>Phasing Status</FONT></TH>
	<TH ALIGN=CENTER BGCOLOR=#000000><FONT COLOR=#FFFFFF>Status ID</FONT></TH>
  </TR>
  <TR> 
	<TD ALIGN=CENTER BGCOLOR=#CCCCCC>Unphased</TD>
	<TD ALIGN=CENTER BGCOLOR=#CCCCFF>0</TD>
  </TR>
  <TR> 
	<TD ALIGN=CENTER BGCOLOR=#CCCCCC>New</TD>
	<TD ALIGN=CENTER BGCOLOR=#CCCCFF>1</TD>
  </TR>
  <TR> 
	<TD ALIGN=CENTER BGCOLOR=#CCCCCC>Existing</TD>
	<TD ALIGN=CENTER BGCOLOR=#CCCCFF>2</TD>
  </TR>
  <TR> 
	<TD ALIGN=CENTER BGCOLOR=#CCCCCC>Demolished</TD>
	<TD ALIGN=CENTER BGCOLOR=#CCCCFF>3</TD>
  </TR>
  <TR> 
	<TD ALIGN=CENTER BGCOLOR=#CCCCCC>Removed</TD>
	<TD ALIGN=CENTER BGCOLOR=#CCCCFF>4</TD>
  </TR>
  <TR> 
	<TD ALIGN=CENTER BGCOLOR=#CCCCCC>Relocated</TD>
	<TD ALIGN=CENTER BGCOLOR=#CCCCFF>5</TD>
  </TR>
  <TR> 
	<TD ALIGN=CENTER BGCOLOR=#CCCCCC>Temporary</TD>
	<TD ALIGN=CENTER BGCOLOR=#CCCCFF>6</TD>
  </TR>
  <TR> 
	<TD ALIGN=CENTER BGCOLOR=#CCCCCC>Past</TD>
	<TD ALIGN=CENTER BGCOLOR=#CCCCFF>7</TD>
  </TR>
  <TR> 
	<TD ALIGN=CENTER BGCOLOR=#CCCCCC>Future</TD>
	<TD ALIGN=CENTER BGCOLOR=#CCCCFF>8</TD>
  </TR>
</TABLE>
</CENTER>

```pascal
FUNCTION GetPhaseStatus(hObject : HANDLE) : INTEGER;
```

```python
def vs.GetPhaseStatus(hObject):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|The object to get the status of.|

## See Also
VS Functions:
[GetStatusInPhase](GetStatusInPhase.md)| [IsPresentInPhase](IsPresentInPhase.md)

## Version
Availability: from Vectorworks 2027

## Category
* [Phasing](Categories/Phasing.md)

