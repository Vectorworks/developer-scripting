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

## Examples
```pascal
if isolate & YNDialog(GetPlugInString(7000)) then BEGIN
	{No need to change the layer & class visibility unless you're searching all layers.}
	if layerOptions = 1 then BEGIN
		SetLayerOptions(5);
		temp_h := FLayer;
		while temp_h <> nil do BEGIN
			Layer(GetLName(temp_h));
			ShowLayer;

Begin
SetLayerOptions(4);
ChangedLayerOpts := True;
End

	gX2 := gXtemp;
	gY2 := gYtemp;
END;
LayerOpt := GetLayerOptions;
IF LayerOpt > 3 THEN SetLayerOptions(5);
gDrawResult := PickPIO(kPIOName, gX1, gY1, gX2, gY2, gIDHand, gIDSymHand, gSourceObjHand, gSourceRec);
IF kDebugMode THEN alrtdialog('Returned from Initial PickPIO');
UserPick := TRUE;
IsDoor := FALSE;
```
```python
import vs

# Sets layer visibility setting for the active document.
layerOpts = 1

vs.SetLayerOptions(layerOpts)
```

## See Also
VS Functions:
[GetLayerOptions](GetLayerOptions.md)

## Version
Availability: from VectorWorks8.5

## Category
* [Layers](../Categories/Layers.md)
