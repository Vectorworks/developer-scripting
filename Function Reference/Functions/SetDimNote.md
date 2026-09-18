# SetDimNote

## Description
Procedure SetDimNote sets the note text of the referenced dimension to the specified value.

```pascal
PROCEDURE SetDimNote(
				h    : HANDLE;
				note : STRING);
```

```python
def vs.SetDimNote(h, note):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to dimension.|
|note|STRING|Note string.|

## Remarks
Sets note text (text under dimension line or dimension text) of the referenced dimension to the specified value.<BR>
<BR>
[ao 3/6/14]

## Examples
```python
SetDimNote(dimHandle,'DLO');
```

```pascal
SetDimNote(h, 'Example');
```
```python
import vs

# Procedure SetDimNote sets the note text of the referenced dimension to the
# specified value.
h = vs.FSActLayer()  # handle to the first selected object on the active layer
note = 'Example'

vs.SetDimNote(h, note)
```

## Version
Availability: from Vectorworks 2015

## Category
* [Dimensions](../Categories/Dimensions.md)
