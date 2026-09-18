# DT_BeginMultipleMove

## Description
Returns TRUE if moving system was started successful.

```pascal
FUNCTION DT_BeginMultipleMove : BOOLEAN;
```

```python
def vs.DT_BeginMultipleMove():
    return BOOLEAN
```

## Examples
```pascal
resultOK := DT_BeginMultipleMove;
```
```python
import vs

# Returns TRUE if moving system was started successful.
ok = vs.DT_BeginMultipleMove()
if ok:
    vs.Message('DT_BeginMultipleMove succeeded')
else:
    vs.Message('DT_BeginMultipleMove failed')
```

## Version
Availability: from Vectorworks 2019

## Category
* [Data Tag Interface Library](../Categories/Data%20Tag%20Interface%20Library.md)
