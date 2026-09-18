# RunPickClrFromPal

## Description
Picks a color from a color palette

```pascal
FUNCTION RunPickClrFromPal(
				VAR filename : STRING;
				VAR index    : LONGINT): BOOLEAN;
```

```python
def vs.RunPickClrFromPal():
    return (BOOLEAN, filename, index)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|filename|STRING|   |
|index|LONGINT|   |

## Examples
```pascal
resultOK := RunPickClrFromPal('file.txt', 1);
```
```python
import vs

# Picks a color from a color palette.
ok, filename, index = vs.RunPickClrFromPal()
vs.Message('RunPickClrFromPal returned: ' + str((ok, filename, index)))
```

## Version
Availability: from Vectorworks 2013

## Category
* [Color](../Categories/Color.md)
