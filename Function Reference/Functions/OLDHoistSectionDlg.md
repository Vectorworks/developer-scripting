# OLDHoistSectionDlg

## Description
Show Hoist Cross Section dialog.

```pascal
FUNCTION OLDHoistSectionDlg(VAR crossSection : STRING): BOOLEAN;
```

```python
def vs.OLDHoistSectionDlg():
    return (BOOLEAN, crossSection)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|crossSection|STRING|   |

## Examples
```pascal
BEGIN
	crossSectionVal := GetRField( HoistHdl, kHoistPIOName, 'CrossSection' );
	IF OLDHoistSectionDlg( crossSectionVal ) THEN
	BEGIN
		ForEachObjectInLayer( SetCrossSection, 2, 1, 1 );
	END;
```
```python
import vs

# Show Hoist Cross Section dialog.
ok, crossSection = vs.OLDHoistSectionDlg()
vs.Message('OLDHoistSectionDlg returned: ' + str((ok, crossSection)))
```

## Version
Availability: from Vectorworks 2018

## Category
* [Truss Analysis](../Categories/Truss%20Analysis.md)
