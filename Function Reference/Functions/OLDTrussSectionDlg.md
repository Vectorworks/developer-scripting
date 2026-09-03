# OLDTrussSectionDlg

## Description
Show Truss Cross Section dialog.

```pascal
FUNCTION OLDTrussSectionDlg(
				VAR crossSection  : STRING;
				VAR height        : REAL;
				VAR width         : REAL;
				VAR design        : INTEGER;
				VAR chordDiameter : REAL): BOOLEAN;
```

```python
def vs.OLDTrussSectionDlg():
    return (BOOLEAN, crossSection, height, width, design, chordDiameter)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|crossSection|STRING|   |
|height|REAL|   |
|width|REAL|   |
|design|INTEGER|   |
|chordDiameter|REAL|   |

## Examples
```pascal
BEGIN
	crossSection := GetRField( parmHand, parmName, kStrCrossSection );
	IF OLDTrussSectionDlg( crossSection, Height, Width, Design, ChordWidth ) THEN
	BEGIN
		ForEachObjectInLayer( SetCrossSection, 2, 1, 1 );
	END;

BEGIN
	crossSection := GetRField( parmHand, parmName, kStrCrossSection );
	IF OLDTrussSectionDlg( crossSection, Height, Width, Design, ChordWidth ) THEN
		ForEachObjectInLayer( SetCrossSection, 2, 1, 1 )
	ELSE
		vsoSetEventResult(-5 {kObjectUIButtonHitCancel});
END;
```
```python
import vs

# Show Truss Cross Section dialog.
ok, crossSection, height, width, design, chordDiameter = vs.OLDTrussSectionDlg()
vs.Message('OLDTrussSectionDlg returned: ' + str((ok, crossSection, height, width, design, chordDiameter)))
```

## Version
Availability: from Vectorworks 2018

## Category
* [Truss Analysis](../Categories/Truss%20Analysis.md)
