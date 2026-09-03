# BeginMultDashConvert

## Description
Used when a number of pseudo index to dash style conversion operations (or vice versa) are going to be performed. <BR>
<BR>
Use EndMultDashConvert when the conversions are complete.

```pascal
PROCEDURE BeginMultDashConvert;
```

```python
def vs.BeginMultDashConvert():
    return None
```

## Examples
```pascal
BeginMultDashConvert;
```
```python
import vs

# Used when a number of pseudo index to dash style conversion operations (or
# vice versa) are going to be performed.
vs.BeginMultDashConvert()
newObj = vs.LNewObj()  # handle to the newly created object
```

## See Also
VS Functions:
[GetPseudoIndFromDash](GetPseudoIndFromDash.md) 
| [GetDashFromPseudoInd](GetDashFromPseudoInd.md) 
| [EndMultDashConvert](EndMultDashConvert.md)

## Version
Availability: from Vectorworks 2019

## Category
* [Utility](../Categories/Utility.md)
