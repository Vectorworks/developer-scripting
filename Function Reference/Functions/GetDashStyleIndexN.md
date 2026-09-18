# GetDashStyleIndexN

## Description
Function GetDashStyleIndexN searches for the pattern specified by the parameters. If it exists, then the negative value of the dash pattern's internal index is returned. If it does not exist, then it is added to the document and the negative value of the new dash pattern's internal index is returned.

```pascal
FUNCTION GetDashStyleIndexN(
				swt      : BOOLEAN;
				numPairs : INTEGER;
				pair1    : REAL;
				pair2    : REAL;
				pair3    : REAL;
				pair4    : REAL;
				pair5    : REAL): LONGINT;
```

```python
def vs.GetDashStyleIndexN(swt, numPairs, pair1, pair2, pair3, pair4, pair5):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|swt|BOOLEAN|   |
|numPairs|INTEGER|   |
|pair1|REAL|   |
|pair2|REAL|   |
|pair3|REAL|   |
|pair4|REAL|   |
|pair5|REAL|   |

## Examples
```python
GetDashStyleIndexN(TRUE, 2, 0.12, 0.18, 0.03, 0.07);

GetDashStyleIndexN(TRUE, 3, 0.12, 0.18, 0.03, 0.07, 0.2, 0.05);
```

```pascal
resultN := GetDashStyleIndexN(TRUE, 1, 1.0, 2.0, 0.5, 1.5, 3.0);
```
```python
import vs

# Function GetDashStyleIndexN searches for the pattern specified by the
# parameters.
swt = True
numPairs = 5
pair1 = 1.0
pair2 = 2.0
pair3 = 0.5
pair4 = 3.0
pair5 = 1.0

index = vs.GetDashStyleIndexN(swt, numPairs, pair1, pair2, pair3, pair4, pair5)
vs.Message('GetDashStyleIndexN returned: ' + str(index))
```

## See Also
VS Functions:
[GetDashDataValPrAtN](GetDashDataValPrAtN.md) 
| [GetNumDashDataPairsN](GetNumDashDataPairsN.md)

## Version
Availability: from Vectorworks 2019

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
