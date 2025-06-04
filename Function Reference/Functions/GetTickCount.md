# GetTickCount

## Description
Returns number of ticks (1/60th second) since system startup.

```pascal
FUNCTION GetTickCount : LONGINT;
```

```python
def vs.GetTickCount():
    return LONGINT
```

## Examples
==== VectorScript ====
```pascal
PROCEDURE Example;
VAR
tick1, tick2 :LONGINT;
BEGIN
tick1 := GetTickCount;
ForEachObject(ResetObject, (T=86));
tick2 := GetTickCount;
Message('Seconds elapsed equals: ', (tick2 - tick1) / 60);
END;
Run(Example);
```
==== Python ====
```python
def ResetObjectWrap(h):
	vs.ResetObject(h)

def Example():
	tick1 = vs.GetTickCount()
	vs.ForEachObject(ResetObjectWrap, '((T=86))')
	tick2 = vs.GetTickCount()
	vs.Message('Seconds elapsed equals: ', (tick2 - tick1) / 60)

Example()
```

## Version
Availability: from VectorWorks8.5

## Category
* [Utility](../Categories/Utility.md)
