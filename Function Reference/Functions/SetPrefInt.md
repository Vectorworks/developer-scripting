# SetPrefInt

## Description
Function SetPrefInt sets the value of a numeric VectorWorks preference setting.

A table of preference dialog items and their corresponding IDs may be found in the [Scirpt Appendix](../Appendix/pages/Appendix%20F%20-%20Preference%20Selectors.md).

```pascal
PROCEDURE SetPrefInt(
				index : INTEGER;
				value : INTEGER);
```

```python
def vs.SetPrefInt(index, value):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|index|INTEGER|Preference item constant.|
|value|INTEGER|New value for preference.|

## Remarks
Sets the value of the specified preference to the value passed.   Similar to SetPref() except it works on preferences for Integer values

## Examples
#### VectorScript ####
```pascal
SetPrefInt(17,FALSE);
```
#### Python ####
```python

```

```pascal
{enable eventing for this plug-in}
SetPrefInt( 590, 1 );
bsb := SetObjPropVS(18, TRUE); {kObjXPropAcceptStates}

BEGIN
	result := SetObjPropVS(kObjXPropHasUIOverride,     TRUE);
	result := SetObjPropVS(12 {kObjXHasCustomWidgetVisibilities}, TRUE);
	result := vsoInsertAllParams;
	SetPrefInt( 590, 1 ); {varParametricEnableStateEventing, kParametricStateEvent_ResetStatesEvent}
	result := SetObjPropVS(18, TRUE); {kObjXPropAcceptStates}
END;

SetObjectVariableBoolean(gPluginH, 702, TRUE);
SetObjectVariableBoolean(gPluginH, 800, TRUE);
prefInt3DRes := GetPrefInt(56);
{ in order to prevent redrawing the document we use pref index 5556 instead of 56. VS, 08/22/2008 }
SetPrefInt(5556, kPrefInt3DRes);
```
```python
vs.SetPrefInt (590,1)
ok = vs.SetObjPropVS( vs.kObjXPropAcceptStates, True )

prefInt3DRes = vs.GetPrefInt( 56 )
vs.SetPrefInt( 5556, kPrefInt3DRes )
vs.Marker( 0, 0, 0 )
vs.ClosePoly()
```

## Version
Availability: from VectorWorks8.0

## Category
* [Document Settings](../Categories/Document%20Settings.md)
