# Space_AddRoomID

## Description
Add a new RoomID to the space object.

```pascal
PROCEDURE Space_AddRoomID(
				space  : HANDLE;
				roomID : STRING);
```

```python
def vs.Space_AddRoomID(space, roomID):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|space|HANDLE|   |
|roomID|STRING|   |

## Examples
```pascal
Space_AddRoomID(space, 'Example');
```
```python
import vs

# Add a new RoomID to the space object.
space = vs.FSActLayer()  # handle to the first selected object on the active layer
roomID = 'Example'

vs.Space_AddRoomID(space, roomID)
```

## Version
Availability: from Vectorworks 2014

## Category
* [SpaceObjectCoreTools](../Categories/SpaceObjectCoreTools.md)
