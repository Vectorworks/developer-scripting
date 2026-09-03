# vstNameUndoEvent

## Description
Assigns a name to the undo event. This name will appear in the mode bar if the user undoes the action.

```pascal
PROCEDURE vstnameUndoEvent(inUndoEventName : STRING);
```

```python
def vs.vstNameUndoEvent(inUndoEventName):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inUndoEventName|STRING|   |

## Examples
```pascal
vstNameUndoEvent (GetPluginString(3010));
{DSelectAll;}
vstGetModeValue (1, modeValue_1);
vstGetDataLong (kLongDataID_Style, style, result);
vstGetDataString (kStringDataID_Auth, authorizer, result);

vstNameUndoEvent (GetPluginString(3000));
DSelectAll;
vstGetModeValue (1, modeValue_1);
vstGetModeValue (2, modeValue_2);

BEGIN
	vstNameUndoEvent( 'Create Object' );
	vstGetPt2D( 0, pt1.x, pt1.y, result );
	vstGetPt2D( 1, pt2.x, pt2.y, result );
	rot := Vec2Ang( pt2 - pt1 );
	objHand := CreateCustomObjectN( 'Symmetry Label Object', pt1.x, pt1.y, rot, FALSE );
```
```python
import vs

# Assigns a name to the undo event.
inUndoEventName = 'Example'

vs.vstNameUndoEvent(inUndoEventName)
```

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Tool Events](../Categories/Tool%20Events.md)
