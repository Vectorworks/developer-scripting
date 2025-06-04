# StairSetOptTotalRise

## Description
<lineList ident=2>
<line>
Sets Stair Total Rise Option - not recommended for use
</line>
<line>
0: By value
</line>
<line>
1: By layer elevation
</line>

<line>
See SDKLib/Include/Interfaces/Vectorworks/Extension/IStairCWSupport.h for more details.
</line>
</lineList>

```pascal
FUNCTION StairSetOptTotalRise(
				stair           : HANDLE;
				OptionTotalRise : INTEGER): BOOLEAN;
```

```python
def vs.StairSetOptTotalRise(stair, OptionTotalRise):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|stair|HANDLE|   |
|OptionTotalRise|INTEGER|   |

## Version
Availability: from Vectorworks 2021

## Category
* [Objects - Stairs](../Categories/Objects%20-%20Stairs.md)
