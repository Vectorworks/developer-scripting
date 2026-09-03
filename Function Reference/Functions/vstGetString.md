# vstGetString

## Description
Gets a string from the resource file.

```pascal
PROCEDURE vstGetString(
				inStrListID   : INTEGER;
				inStrID       : INTEGER;
				VAR outString : STRING);
```

```python
def vs.vstGetString(inStrListID, inStrID):
    return outString
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inStrListID|INTEGER|   |
|inStrID|INTEGER|   |
|outString|STRING|Output parameter.|

## Examples
```pascal
vstGetString(1, 2, 'Example');
```
```python
import vs

# Gets a string from the resource file.
inStrListID = 1
inStrID = 2

text = vs.vstGetString(inStrListID, inStrID)
vs.Message('vstGetString returned: ' + str(text))
```

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Tool Events](../Categories/Tool%20Events.md)
