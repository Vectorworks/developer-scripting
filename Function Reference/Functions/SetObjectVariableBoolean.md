# SetObjectVariableBoolean

## Description
Sets the ON-OFF status of a VectorWorks object property.

For specific object selector index values, see the [Script Appendix](../Appendix/pages/Appendix%20G%20-%20Object%20Selectors.md).

```pascal
PROCEDURE SetObjectVariableBoolean(
				h      : HANDLE;
				index  : INTEGER;
				status : BOOLEAN);
```

```python
def vs.SetObjectVariableBoolean(h, index, status):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|
|index|INTEGER|Object property index.|
|status|BOOLEAN|New status for property.|

## Examples
#### VectorScript ####
```pascal
SetObjectVariableBoolean(obj, 17, FALSE);
```
#### Python ####
```python

```

```pascal
SetObjectVariableBoolean(parmHand, 800, TRUE);
PushAttrs;

ELSE BEGIN
	shaftH := WholeRRect(-gShaftWidth/2, gShaftDepth/2, gShaftWidth/2, -gShaftDepth/2, gShaftRadius);
	parmClassName := GetClass(gPluginH);
	Locus(0, 0);
 			SetObjectVariableBoolean(LNewObj, kOvMasterSnapPoint, TRUE);
 			SetObjectVariableBoolean(LNewObj, kOvShowMasterSnapOutsideSnapbox, FALSE);
 			SetClass(LNewObj, parmClassName);
	Locus(gShaftWidth/2, gShaftWidth/2);
 			SetObjectVariableBoolean(LNewObj, kOvMasterSnapPoint, TRUE);

	NewField(kHidRecName, kDatabaseUUID, '', 4, 0);
	NewField(kHidRecName, kNoteDescrip,  '', 4, 0);
	NewField(kHidRecName, kNoteUUID,     '', 4, 0);
	NewField(kHidRecName, kText,         '', 4, 0);
	SetObjectVariableBoolean(GetObject(kHidRecName), 900, kRNDebugMode);
END;
```
```python
vs.SetObjectVariableBoolean( gObjHandle, 800, True )
```
See also in tutorials: [03. Build a Curved Path with Mixed Vertex Types](ai%20examples/03_CurvedPolylinePath.md), [Plug-in with widgets, basic example (Python)](../../Common/Tasks/Parametrics/Plug-in%20with%20widget%20basic%20example.md)

## Version
Availability: from VectorWorks 9.0

## Category
* [Object Info](../Categories/Object%20Info.md)
