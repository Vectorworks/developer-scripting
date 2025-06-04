# StairSetConfigType

## Description
Sets Stair Configuration Type. Not recommended for use as stair might end up with inconsistent and contradictory parameters.
<desc>
<lineList ident=2>

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
FUNCTION StairSetConfigType(
				stair             : HANDLE;
				ConfigurationType : INTEGER): BOOLEAN;
```

```python
def vs.StairSetConfigType(stair, ConfigurationType):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|stair|HANDLE|   |
|ConfigurationType|INTEGER|   |

## Version
Availability: from Vectorworks 2021

## Category
* [Objects - Stairs](../Categories/Objects%20-%20Stairs.md)
