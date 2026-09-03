# vsoPFCSetChanged

## Description
Provide the object Changed result for the PrepareForContext (79) message sent to a Script object.

```pascal
PROCEDURE vsoPFCSetChanged(
				message   : LONGINT;
				didChange : BOOLEAN);
```

```python
def vs.vsoPFCSetChanged(message, didChange):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|message|LONGINT|   |
|didChange|BOOLEAN|   |

## Examples
```pascal
vsoPFCSetChanged(1, TRUE);
```
```python
import vs

# Provide the object Changed result for the PrepareForContext (79) message
# sent to a Script object.
message = 'Hello Vectorworks'
didChange = True

vs.vsoPFCSetChanged(message, didChange)
```

## Version
Availability: from Vectorworks 2023

## Category
* [Object Events](../Categories/Object%20Events.md)
