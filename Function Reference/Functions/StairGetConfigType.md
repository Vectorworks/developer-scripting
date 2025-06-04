# StairGetConfigType

## Description
<lineList ident=2>
<line>
Returns Stair Configuration Type.
</line>
<line>
ErrorStandardConfiguration = -1, /* Returned by VCOM functions if some error occurs */
</line>
<line>
                StraightStair = 1 /* Numbers need to match strings in string files and need to be consistent for compatibility so do not change order and values of these constants */
</line>
<line>
                StraightTwoRuns = 2
</line>
<line>
                LSingleLanding = 3
</line>
<line>
                USingleLanding = 4
</line>
<line>
                UDoubleLandings = 5
</line>
<line>
                LWinder = 6
</line>
<line>
                UDoubleWinder = 7
</line>
<line>
                USingleWinder = 8
</line>
<line>
                CircularStair = 9
</line>
<line>
                Unused1 /* Required for compatibility */
</line>
<line>
                StraightThreeRuns = 11
</line>
<line>
                LFixedAngleWinder = 12
</line>
<line>
                UDoubleFixedAngleWinder = 13
</line>
<line>
                USingleFixedAngleWinder = 14
</line>
<line>
                ZSingleLanding = 15 /* not supported yet */
</line>
<line>
                ZDoubleLandings = 16/* not supported yet */
</line>
<line>
                DoubleUDoubleLandings = 17 /* O-Stair with two 180 degree landings */
</line>
<line>
                OStairTripleLandings  = 18 /* O-Stair with three 90 degree landings */
</line>
<line>
See SDKLib/Include/Interfaces/Vectorworks/Extension/IStairCWSupport.h for more details.
</line>
</lineList>

```pascal
FUNCTION StairGetConfigType(stair : HANDLE): INTEGER;
```

```python
def vs.StairGetConfigType(stair):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|stair|HANDLE|   |

## Version
Availability: from Vectorworks 2021

## Category
* [Objects - Stairs](../Categories/Objects%20-%20Stairs.md)
