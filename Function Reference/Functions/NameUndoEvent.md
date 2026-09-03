# NameUndoEvent

## Description
Procedure NameUndoEvent names the undo event that is currently being built by VectorScript execution. Parameter eventName is the name of the undo event.

```pascal
PROCEDURE NameUndoEvent(eventName : STRING);
```

```python
def vs.NameUndoEvent(eventName):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|eventName|STRING|Name of undo event.|

## Remarks
Names the undo event that is currently being built.

## Examples
```pascal
NameUndoEvent(GetPlugInString(4011));
VSOSetEventResult(kObjectUIButtonHitOK);
END

	BEGIN
	TempHand := GetObject(marker2ActualName);
	IF TempHand <> NIL THEN DelObj(TempHand);
	END;
NameUndoEvent(GetPlugInString(4011));
VSOSetEventResult(kObjectUIButtonHitOK);
END

	NameUndoEvent('Camera Match Mask');
(*
1:
*)
END; {MAIN}
```
```python
vs.ResetObject( gObjHandle )
vs.NameUndoEvent( vs.GetPluginString( 3001 ) )
vs.vsoSetEventResult( vs.kObjectUIButtonHitOK )
```

## Version
Availability: from VectorWorks8.0

## Category
* [Utility](../Categories/Utility.md)
