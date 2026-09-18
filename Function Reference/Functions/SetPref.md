# SetPref

## Description
Procedure SetPref sets the on-off status of a VectorWorks preference dialog item. Parameter index specifies the preference item, and parameter status sets the on-off status of the item.

A table of preference dialog items and their corresponding IDs may be found in the [Scirpt Appendix](../Appendix/pages/Appendix%20F%20-%20Preference%20Selectors.md).

```pascal
PROCEDURE SetPref(
				index  : INTEGER;
				status : BOOLEAN);
```

```python
def vs.SetPref(index, status):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|index|INTEGER|Preference item constant.|
|status|BOOLEAN|On- off status of preference.|

## Remarks
Running the following script:

```pascal
SetPref(21, False); {Stop VectorScript on Warnings}
```

results in a total system freeze requiring a forced restart.
This problem has been in VW9 (w/ Mac OS 9.2) and is still in VW 9.5b1.

'Hidden' preference 12348 allows us to turn on and off dialog list box refresh.  This is a significant performance enhancement for any dialog that loads list boxes.  Just do [SetPref](SetPref.md)(12348, False) load your list box(es) and then [SetPref](SetPref.md)(12348, True) to re-enable list refreshing.  I believe this must be called after the dialog is on screen, so after the GetDialog Call for classic dialogs and in the handler procedure for modern dialogs.

## Examples
#### VectorScript ####
```pascal
SetPref(17,FALSE);
```
#### Python ####
```python

```

```pascal
angle := GetPrefReal(93);
planrotation := GetPref(92);
SetPref(92, FALSE);
PushAttrs;
GetOrigin(PX, PY);
TextJust (1);
TextVerticalAlign (1);

Options[2] := 'SeatingLayoutPick'; {Saved xml Item}
Options[3] := ''; {Check Box String}
AlertInformDontShowAgain(GetPlugInString(3010),'', FALSE, Options);
PenFore(45000, 45000, 45000);
SetPref(9871, TRUE);
GetOrigin(OriginX,OriginY);
Is3dView := GetProjection(ActLayer)<>6;
RunTempTool(TempToolCallback, TRUE);

BEGIN
	UseDefaultContent := GetPref(130);
	IF NOT(UseDefaultContent) THEN SetPref(130,TRUE);
	{Search the default folder}
	gMarker1Name := gStartMarkerName;
	ResourceListID := BuildResourceList(16,-kDefConDetailMarkers,kFolderName,NumMarkerSymbols);
	FoundMarker := FALSE;
```
```python
if not UseDefaultContent:
	vs.SetPref( 130, True )
```
See also in tutorials: [Plug-in with widgets, basic example (Python)](../../Common/Tasks/Parametrics/Plug-in%20with%20widget%20basic%20example.md)

## See Also
[GetPref](GetPref.md)

## Version
Availability: from MiniCAD6.0

## Category
* [Document Settings](../Categories/Document%20Settings.md)
