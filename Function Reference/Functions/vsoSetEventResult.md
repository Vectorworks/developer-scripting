# vsoSetEventResult

## Description
?

```pascal
PROCEDURE vsoSetEventResult(inEventResult : LONGINT);
```

```python
def vs.vsoSetEventResult(inEventResult):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inEventResult|LONGINT|   |

## Examples
```pascal
	vsoSetEventResult(kObjectEventHandled);
END;

	vsoWidgetSetVisible(9, FALSE);
	vsoWidgetSetEnable(5, (wallH <> NIL));
	vsoWidgetSetEnable(6, ((wallH <> NIL) & pSize_TO_Wall_Length));
	vsoWidgetSetEnable(7, ((wallH <> NIL) & pSize_to_Wall_Length));
	vsoSetEventResult( -8 {kObjectEventHandled} );
END;

BEGIN
	vsoSetEventResult( kEditPluginStyleDefault );
END;
```
```python
	# Default - First case
	vs.vsoWidgetSetEnable( kWidgetID_DetailNo, 	False )
	vs.vsoWidgetSetEnable( kWidgetID_Separator, False )
vs.vsoSetEventResult( vs.kObjectEventHandled );

# this is very important! this is how the system knows we've handled this
vs.vsoSetEventResult( vs.kObjectEventHandled );
```

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Object Events](../Categories/Object%20Events.md)
