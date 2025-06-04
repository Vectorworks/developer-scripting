# GetDashFromPseudoInd

## Description
Gets the dash style that corresponds to the pseudo index and returns the style's internal index. Returns TRUE if successful.<BR>
<BR>

```pascal
FUNCTION GetDashFromPseudoInd(
				pseudoIndex      : INTEGER;
				VAR outDashStyle : LONGINT): BOOLEAN;
```

```python
def vs.GetDashFromPseudoInd(pseudoIndex):
    return (BOOLEAN, outDashStyle)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|pseudoIndex|INTEGER|Pseudo index (negative value)  for which a dash style is requested.|
|outDashStyle|LONGINT|Negative internal index of a dashed line type corresponding to the psuedo index.|

## See Also
VS Functions:
[GetPseudoIndFromDash](GetPseudoIndFromDash.md) 
| [BeginMultDashConvert](BeginMultDashConvert.md) 
| [EndMultDashConvert](EndMultDashConvert.md)

## Version
Availability: from Vectorworks 2019

## Category
* [Utility](../Categories/Utility.md)
