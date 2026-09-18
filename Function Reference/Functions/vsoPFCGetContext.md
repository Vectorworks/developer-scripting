# vsoPFCGetContext

## Description
Retrieve the context parameters from the PrepareForContext (79) message sent to a Script object.

```pascal
PROCEDURE vsoPFCGetContext(
				message          : LONGINT;
				VAR context      : INTEGER;
				VAR viewType     : INTEGER;
				VAR bgRenderMode : INTEGER;
				VAR fgRenderMode : INTEGER);
```

```python
def vs.vsoPFCGetContext(message):
    return (context, viewType, bgRenderMode, fgRenderMode)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|message|LONGINT|   |
|context|INTEGER|   |
|viewType|INTEGER|   |
|bgRenderMode|INTEGER|   |
|fgRenderMode|INTEGER|   |

## Examples
```pascal
vsoPFCGetContext(1, 2, 3, 10, 5);
```
```python
import vs

# Retrieve the context parameters from the PrepareForContext (79) message
# sent to a Script object.
message = 'Hello Vectorworks'

context, viewType, bgRenderMode, fgRenderMode = vs.vsoPFCGetContext(message)
vs.Message('vsoPFCGetContext returned: ' + str((context, viewType, bgRenderMode, fgRenderMode)))
```

## Version
Availability: from Vectorworks 2023

## Category
* [Object Events](../Categories/Object%20Events.md)
