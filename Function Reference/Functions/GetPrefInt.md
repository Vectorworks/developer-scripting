# GetPrefInt

## Description
Function GetPrefInt returns the value of a numeric VectorWorks preference setting.

A table of preference dialog items and their corresponding IDs may be found in the [Scirpt Appendix](../Appendix/pages/Appendix%20F%20-%20Preference%20Selectors.md).

```pascal
FUNCTION GetPrefInt(prefIndex : INTEGER): INTEGER;
```

```python
def vs.GetPrefInt(prefIndex):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|prefIndex|INTEGER|Preference item constant.|

## Remarks
Returns the status of the specified preference item.  Used for preferences that return an Integer instead of a Boolean (see GetPref)

## Examples
#### VectorScript ####
```pascal
maxUndos:=GetPrefInt(17);
```
#### Python ####
```python
maxUndos = vs.GetPrefInt(17)
```

```pascal
SetObjectVariableBoolean(gPluginH, 702, TRUE);
SetObjectVariableBoolean(gPluginH, 800, TRUE);
prefInt3DRes := GetPrefInt(56);
{ in order to prevent redrawing the document we use pref index 5556 instead of 56. VS, 08/22/2008 }
SetPrefInt(5556, kPrefInt3DRes);

{save the current text style, and font of the doc in order to restore them after the creation of the new callout}
oldDocFontName	:= GetPrefString(100);
oldDocFontStyle	:= GetPrefInt(58);

BEGIN
	IF ResourceIsOK THEN
	wall_cnt := 0;
	saveConRes := GetPrefInt(55);
	SetPrefInt(5555, 32);
	ForEachObjectInLayer(StoreWallFootPrints, 2, 0, 4);
	if wall_cnt = 0 then AlrtDialog(GetPlugInString(5000)) else BEGIN
		Dialog_Setup;
```
```python
docTextAlign = vs.GetPrefInt(83)
docTextJust = vs.GetPrefInt(82)

prefInt3DRes = vs.GetPrefInt( 56 )
vs.SetPrefInt( 5556, kPrefInt3DRes )
vs.Marker( 0, 0, 0 )
vs.ClosePoly()
```

## Version
Availability: from VectorWorks8.0

## Category
* [Document Settings](../Categories/Document%20Settings.md)
