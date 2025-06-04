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

## Version
Availability: from Vectorworks 2013

## Category
* [Dialogs - Predefined](../Categories/Dialogs%20-%20Predefined.md)
