# GetPseudoIndFromDash

## Description
Supplies a pseudo index for a dashed style. The returned index is not guaranteed to produce the same line type from file to file, nor even in the same file if line types change.<BR>
Returns TRUE if successful.

```pascal
FUNCTION GetPseudoIndFromDash(
				dashStyle          : LONGINT;
				VAR outPseudoIndex : INTEGER): BOOLEAN;
```

```python
def vs.GetPseudoIndFromDash(dashStyle):
    return (BOOLEAN, outPseudoIndex)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dashStyle|LONGINT|Negative internal index of a dashed line type.|
|outPseudoIndex|INTEGER|Pseudo index (a negative number) corresponding to the dash style.  The psuedo index is not guaranteed to produce the same line across files (or even in the same file if line types are changed).|

## See Also
VS Functions:
[GetDashFromPseudoInd](GetDashFromPseudoInd.md) 
| [BeginMultDashConvert](BeginMultDashConvert.md) 
| [EndMultDashConvert](EndMultDashConvert.md)

## Version
Availability: from Vectorworks 2019

## Category
* [Utility](../Categories/Utility.md)
