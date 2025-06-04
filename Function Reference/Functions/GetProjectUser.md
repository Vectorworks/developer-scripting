# GetProjectUser

## Description
For a given userid in the current Project, get their full name and permission level.<BR>
<BR>
<I>Table - Project Sharing Permissions</I><P>
<CENTER>
<TABLE BORDER=0 ALIGN=CENTER CELLSPACING=1 CELLPADDING=3>
  <TR> 
	<TH ALIGN=CENTER><B>Permission Level></B></TH>
	<TH ALIGN=CENTER><B>Constant</B></TH>
  </TR>
  <TR> 
	<TD ALIGN=LEFT>Read Only</TD>
	<TD ALIGN=CENTER>1</TD>
  </TR>
  <TR> 
	<TD ALIGN=LEFT>Layers-Restricted</TD>
	<TD ALIGN=CENTER>2</TD>
  </TR>
  <TR> 
	<TD ALIGN=LEFT>Layers-Unrestricted</TD>
	<TD ALIGN=CENTER>3</TD>
  </TR>
  <TR> 
	<TD ALIGN=LEFT>Layers and Resources</TD>
	<TD ALIGN=CENTER>4</TD>
  </TR>
  <TR> 
	<TD ALIGN=LEFT>Project</TD>
	<TD ALIGN=CENTER>5</TD>
  </TR>
  <TR> 
	<TD ALIGN=LEFT>Administrative</TD>
	<TD ALIGN=CENTER>6</TD>
  </TR>
</TABLE>
</CENTER>

```pascal
FUNCTION GetProjectUser(
				userId         : STRING;
				VAR fullName   : STRING;
				VAR permission : INTEGER): BOOLEAN;
```

```python
def vs.GetProjectUser(userId):
    return (BOOLEAN, fullName, permission)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|userId|STRING|The userid to look up|
|fullName|STRING|The users full name|
|permission|INTEGER|Permission level of the user|

## See Also
VS Functions:
[GetProjectUserNames](GetProjectUserNames.md)

## Version
Availability: from Vectorworks 2016

## Category
* [Project Sharing](../Categories/Project%20Sharing.md)
