# vstAddButtonMode

## Description
Used in the initialization of an event-enabled tool, add a mode bar button.

(Seems like this has been replaced by [AddButtonMode](AddButtonMode.md))

```pascal
PROCEDURE vstAddButtonMode(inIconID : DYNARRAY OF CHAR);
```

```python
def vs.vstAddButtonMode(inIconSpecification):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inIconID|INTEGER|   |

## Examples
```pascal
vstAddButtonMode(inIconID);
```
```python
import vs

# Used in the initialization of an event-enabled tool, add a mode bar button.
inIconSpecification = 'Example'

vs.vstAddButtonMode(inIconSpecification)
```

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Tool Events](../Categories/Tool%20Events.md)
