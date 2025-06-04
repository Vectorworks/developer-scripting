# GetDashStyleN

## Description
Function GetDashStyleN searches for the pattern specified by the parameters. If it exists, then the negative value of the dash pattern's internal index is returned. If it does not exist, then it is added to the document and the negative value of the dash pattern's internal index is returned.

```pascal
FUNCTION GetDashStyleN(
				swt      : BOOLEAN;
				numPairs : INTEGER;
				pair1    : REAL;
				pair2    : REAL;
				pair3    : REAL;
				pair4    : REAL;
				pair5    : REAL): LONGINT;
```

```python
def vs.GetDashStyleN(swt, numPairs, pair1, pair2, pair3, pair4, pair5):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|swt|BOOLEAN|scales with thickness|
|numPairs|INTEGER|count of used pairs|
|pair1|REAL|   |
|pair2|REAL|   |
|pair3|REAL|   |
|pair4|REAL|   |
|pair5|REAL|   |

## Remarks
Searches for the pattern specified by the parameters. If it exists, then the negative value of the dash pattern's internal index is returned. If it does not exist, then it is added to the document and the negative value of the dash pattern's internal index is returned.

## Examples
```python
currLS:=GetDashStyleN;
```

## Version
Availability: from Vectorworks 2019

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
