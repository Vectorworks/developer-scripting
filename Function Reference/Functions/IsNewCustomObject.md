# IsNewCustomObject

## Description
Function IsNewCustomObject returns whether the specified plug-in object is a new object, indicating that the object is being regenerated for the first time.

New object status is useful in specifying initialization and setup data, as well as calling initialization specific subroutines. This function should only be called in plug-in objects.

```pascal
FUNCTION IsNewCustomObject(objectName : STRING): BOOLEAN;
```

```python
def vs.IsNewCustomObject(objectName):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectName|STRING|Name of plugin object.|

## Remarks
*\_c\_* (2008.04.05): IsNewCustomObject will never return TRUE on: objects created by[CreateCustomObjectPath](CreateCustomObjectPath.md), objects duplicated by alt-click + drag, by Duplicate command, etc.

To detect a duplicated object you can use the name unicity rule of VW:
* create a text field with default: '' <empty string>. Call it for example '__UUID' (the two preceeding underscores will make it invisible)
* if it's a new pio object, this field will be empty (according to the default): load the field with a new UUID value, use it also as object name (what shows in the name field of the data Tab in the Object Info Palette, the OIP).
* if it's an edit to an existing pio object: field __UUID = object name.
* upon duplicating a pio object: the OIP's name field will be instantly deleted by VW, which doesn't allow two objects with the same name

```pascal
theUUID := P__UUID; { fetch the UUID value stored. It will be empty on new object }

{ a duplicate never triggers IsNewCustomObject }
IF IsNewCustomObject(pioName) THEN BEGIN 
	{ these below should not be repeated but belong to a sub-routine }
	theUUID := CreateUUID; { create a new unique name for the pio object }
	SetRField(pioHandle, pioName, '__UUID', theUUID); { now the field _UUID stores a name }
	SetName(pioHandle, theUUID); { name the pio object with the UUID }
END;

gIsCopy := theUUID <> GetName(pioHandle); { upon pio instance duplication, the name will be overwritten by VW with a 'none' string }
IF gIsCopy THEN BEGIN
	{ ... do something ... }

	{ these below should not be repeated but belong to a sub-routine }
	theUUID := CreateUUID; { create a new unique name for the pio object }
	SetRField(pioHandle, pioName, '__UUID', theUUID); { now the field _UUID stores a name }
	SetName(pioHandle, theUUID); { name the pio object with the UUID }
END;
```

(Unsigned:)

IsNewCustomObject will never return TRUE on: objects created by Call from CustomObject scripts only.  Returns true for new objects, meaning this is the first time the regeneration script is being called.

(Unsigned:)

Returns false when a new object is placed into a wall, due to the dual regen issue. What you have to do is to create an invisible parameter to trap the new status on the first regen, then check that parameter in the second regen, react accordingly, then reset the parameter to its default value.

So this will evaluate on the first regen:

```pascal
IF IsNewCustomObject(MyObject) & p__IsNew THEN 
    SetRField(ghParm, MyObject, '__IsNew', 'True');
```

And this on the second regen:

```pascal
IF p__IsNew & (hWall <> Nil) THEN BEGIN
    SetRField(ghParm, MyObject, '__IsNew', 'False' );
    DoMyStuffHere...
END;
```

## Examples
```pascal
BEGIN
	IF (p__Version = 0) & NOT(IsNewCustomObject(parmName)) THEN
		Translate120 := TRUE
	ELSE
		Translate120 := FALSE;
	IF Translate120 THEN {Translate the class texture to the object}
		BEGIN
		TextureIDX := GetClTextureG(pHidden);
		IF TextureIDX <> 0 THEN

BEGIN
	IF (NOT IsNewCustomObject(gPluginName)) & (p__version < 1600) THEN
	BEGIN
		{Empty string means container class}
		kRealNoneClass := ClassList(1);
		IF pShaft_Finish = kRealNoneClass THEN
			SetRField (h, gPluginName, 'Shaft Finish','');
		IF pCapital_Finish = kRealNoneClass THEN
			SetRField (h, gPluginName, 'Capital Finish','');

BEGIN
result := GetPluginChoiceIndex(parmName,'LineMode',pLineMode,LLChoice);
{Handle Versioning -- if old instance, convert to only previous mode, Fixed}
IF (p__Version < 1400) & NOT(IsNewCustomObject(parmName)) THEN
	BEGIN
	SetRField(parmHand,parmName,'LineMode','Fixed');
	LLChoice := 1;
	END;
```
```python
	showFence = vs.PUse_Fence
else:
	showFence = False
if ( vs.IsNewCustomObject( gObjName ) ):
	if ( vs.GetObject( kStrExistDTM ) != 0 ):
		vs.SetRField( gObjHandle, gObjName, 'Show Fences', 'True' )
		showPad = True

if useModifiers:
	useFence = vs.PUse_Fence
kStrExistDTM	= vs.GetResourceString( kMiscStrID, 1 )
if ( vs.IsNewCustomObject( gObjName ) ):
	if ( vs.GetObject( kStrExistDTM ) != 0 ):
		vs.SetRField( gObjHandle, gObjName, 'Use Site Modifiers', 'True' )
		useModifiers = True
DTMModification(useModifiers, useFence, width, length)

# Initialize GetLocStr variable
kStrExistDTM = vs.GetResourceString( kMisc_str_ID, 1 )
if ( vs.IsNewCustomObject( gObjName ) ):
	if ( vs.GetObject( kStrExistDTM ) != 0 ):
		vs.SetRField( gObjHandle, gObjName, 'Show Fences', 'True' )
		showPad = True
```

## See Also
VS Functions:
[GetCustomObjectInfo](GetCustomObjectInfo.md)

## Version
Availability: from VectorWorks 8.0

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
