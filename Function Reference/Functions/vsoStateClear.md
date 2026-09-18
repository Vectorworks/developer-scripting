# vsoStateClear

## Description
Clears states between events. Must be called during the regen event 3 (kParametricRecalculate).

See [[VS:Parametric_State_Notifications#Reset_event]]

```pascal
PROCEDURE vsoStateClear(hObj : HANDLE);
```

```python
def vs.vsoStateClear(hObj):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObj|HANDLE|   |

## Remarks
{ Orso quoting Vlado: In order to receive correct information on received states in between resets, IT IS EXTREMELY IMPORTANT to call VS:vsoStateClear at the end of the reset event }

## Examples
```pascal
3: {kParametricRecalculate}
  BEGIN
    { ... }
    vsoStateClear( objectHand );
  END;
```

```pascal
BEGIN
	ResetEventHandler;
	vsoStateClear(parmHand);
END;

	SetCursor (SmCrossC);
	PopAttrs;
	SetVersion(pluginH, recordName);
	SetDownObject;
	vsoStateClear(pluginH);
END;

BEGIN
	HexBoltObjectInch;
	vsoStateClear(gPluginH);
END;
```
```python
elif theEvent == vs.kParametricRecalculate:
	ResetEventHandler()
	vs.vsoStateClear( gObjHandle )
```

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Object Events](../Categories/Object%20Events.md)
