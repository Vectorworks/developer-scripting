# DT_EndMultipleMove

## Description
Returns TRUE if moving system was stoped successful.

```pascal
FUNCTION DT_EndMultipleMove : BOOLEAN;
```

```python
def vs.DT_EndMultipleMove():
    return BOOLEAN
```

## Examples
```pascal
resultOK := DT_EndMultipleMove;
```
```python
import vs

# Returns TRUE if moving system was stoped successful.
ok = vs.DT_EndMultipleMove()
if ok:
    vs.Message('DT_EndMultipleMove succeeded')
else:
    vs.Message('DT_EndMultipleMove failed')
```

## Version
Availability: from Vectorworks 2019

## Category
* [Data Tag Interface Library](../Categories/Data%20Tag%20Interface%20Library.md)
