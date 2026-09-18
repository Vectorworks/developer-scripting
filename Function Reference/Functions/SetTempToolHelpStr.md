# SetTempToolHelpStr

## Description
Sets a text to be used as help string for temp tool calls: RunTempTool, TrackObject, GetPt, GetPtL, GetPt3D, and GetPtL3D.<BR>
<BR>
This function should be called prior to calling the tool.<BR>
<BR>
The help string will be used for subsequent temp tool runs until changed.

```pascal
PROCEDURE SetTempToolHelpStr(helpString : STRING);
```

```python
def vs.SetTempToolHelpStr(helpString):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|helpString|STRING|The help string for the next temp tool.|

## Examples
#### VectorScript ####
```pascal
PROCEDURE Test;
VAR h : HANDLE;
  
  FUNCTION CheckObjCallback(h : HANDLE) : BOOLEAN;
  BEGIN
     {any object is ok}
     CheckObjCallback := true;
  END;

BEGIN
SetTempToolHelpStr( 'Select any object' );
TrackObject( CheckObjCallback, h );
SetSelect( h );
END;
RUN( Test );
```
#### Python ####
```python

```

```pascal
NumNFerInstruments := 0;
TempHandle1 := NIL;
TempHandle2 := NIL;
ALLOCATE InstHands [1..5];
SetTempToolHelpStr(GetPlugInString(3007));
STRING3005 := GetPlugInString(3005);
STRING3006 := GetPlugInString(3006);
REPEAT
TrackObject( CheckObjCallback, TempHandle1,TempXLoc, TempYLoc, TempZLoc );

SetTempToolHelpStr( GetPlugInString(5008) );
TrackLightingDevice( TmpPickObjHan, shiftKeyPressed );
WHILE ( TmpPickObjHan <> NIL ) & ( NOT IsCanceled ) DO
BEGIN
	NumInsts := NumInsts + 1;
```
```python
vs.SetTempToolHelpStr('Example')
```

## Version
Availability: from Vectorworks 2010

## Category
* [User Interactive](../Categories/User%20Interactive.md)
