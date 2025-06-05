# Units

## Description
Procedure Units specifies a standard units setting for the active document. 

**Table - Standard Unit Settings**

| Units Setting | Constant |
|---------------|----------|
| Custom        | 0        |
| Feet/Inches   | 1        |
| Inches        | 2        |
| Feet          | 3        |
| Yards         | 4        |
| Miles         | 5        |
| Microns       | 6        |
| Millimeters   | 7        |
| Centimeters   | 8        |
| Meters        | 9        |
| Kilometers    | 10       |

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
See [GetPrimaryUnitInfo](GetPrimaryUnitInfo.md) for details on changes in version 9 and again in version 12.

## Version
Availability: from All Versions

## Category
* [Units](../Categories/Units.md)
