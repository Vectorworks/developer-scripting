# Units

## Description
Procedure Units specifies a standard units setting for the active document. 

{| class="wikitable_c"
|+ Table - Standard Unit Settings
! Units Setting !! Constant
|-
| Custom
| style="text-align:center"| 0
|-
| Feet/Inches
| style="text-align:center"| 1
|-
| Inches
| style="text-align:center"| 2
|-
| Feet
| style="text-align:center"| 3
|-
| Yards
| style="text-align:center"| 4
|-
| Miles
| style="text-align:center"| 5
|-
| Microns
| style="text-align:center"| 6
|-
| Millimeters
| style="text-align:center"| 7
|-
| Centimeters
| style="text-align:center"| 8
|-
| Meters
| style="text-align:center"| 9
|-
| Kilometers
| style="text-align:center"| 10
|}

```pascal
PROCEDURE Units(i : INTEGER);
```

```python
def vs.Units(i):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|i|INTEGER|Standard units setting index value.|

## Remarks
See [[VS:GetPrimaryUnitInfo| GetPrimaryUnitInfo]] for details on changes in version 9 and again in version 12.

## Version
Availability: from All Versions

## Category
* [Units](../Categories/Units.md)
