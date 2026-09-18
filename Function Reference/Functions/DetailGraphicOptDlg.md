# DetailGraphicOptDlg

## Description
This brings up the Graphic Options dialog for Detail-Callout Marker and Detail Callout objects.

```pascal
FUNCTION DetailGraphicOptDlg(
				VAR Marker         : STRING;
				VAR ShoulderLength : REAL;
				VAR TagPosIndex    : INTEGER;
				VAR LeaderType     : LONGINT;
				VAR LeaderThick    : INTEGER): BOOLEAN;
```

```python
def vs.DetailGraphicOptDlg(Marker, ShoulderLength, TagPosIndex, LeaderType, LeaderThick):
    return (BOOLEAN, Marker, ShoulderLength, TagPosIndex, LeaderType, LeaderThick)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|Marker|STRING|The name of the selected Marker symbol.|
|ShoulderLength|REAL|The shoulder length for the detail callout object.|
|TagPosIndex|INTEGER|The index of the selected Tag Position.|
|LeaderType|LONGINT|The linetype for the leader lines.|
|LeaderThick|INTEGER|The line thickness for the leader line.|

## Examples
```pascal
gLeaderType := Str2Num(GetRField(pluginH2,pluginName2,kNNA_LeaderType));
gLeaderThickness := Str2Num(GetRField(pluginH2,pluginName2,kNNA_LeaderThick));
origTagPosition := gTagPosition;
IF DetailGraphicOptDlg(gMarker1Name,gShoulderLength,gTagPosition,gLeaderType,gLeaderThickness) THEN
	BEGIN
	SetRField(pluginH2, pluginName2, '__Marker_Style', gMarker1Name);
	ResourceListID := BuildResourceList(16,-kDefConDetailMarkers,kFolderName,NumMarkerSymbols);
	For I := 1 to NumMarkerSymbols DO
		BEGIN
		TempStr := GetNameFromResourceList(ResourceListID,I);
```
```python
import vs

# This brings up the Graphic Options dialog for Detail-Callout Marker and
# Detail Callout objects.
Marker = 'Example'
ShoulderLength = 1.0
TagPosIndex = 1
LeaderType = 0
LeaderThick = 1

ok, Marker, ShoulderLength, TagPosIndex, LeaderType, LeaderThick = vs.DetailGraphicOptDlg(Marker, ShoulderLength, TagPosIndex, LeaderType, LeaderThick)
vs.Message('DetailGraphicOptDlg returned: ' + str((ok, Marker, ShoulderLength, TagPosIndex, LeaderType, LeaderThick)))
```

## Version
Availability: from Vectorworks 2013

## Category
* [Dialogs - Predefined](../Categories/Dialogs%20-%20Predefined.md)
