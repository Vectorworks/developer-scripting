# GetType

## Description
DON'T USE THIS ANYMORE. Switch over to [ GetTypeN](GetTypeN.md).

Returns the type index of the referenced object.

A complete listing of supported object types may be found in the [Script Appendix](../Appendix/pages/Appendix%20D%20-%20Vectorworks%20Object%20Types%20and%20Subtypes.md).

```pascal
FUNCTION GetType(h : HANDLE): INTEGER;
```

```python
def vs.GetType(h):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
	str :STRING;
	h :HANDLE;
BEGIN
	str := StrDialog('Enter the name:', 'Window');
	IF NOT DidCancel THEN BEGIN
		h := GetObject(str);
		IF h <> NIL THEN BEGIN
			CASE GetType(h) OF
				2: str := 'Line';
				3: str := 'Rectangle';
				4: str := 'Ellipse';
				5: str := 'Polygon';
				6: str := 'Arc/Circle';
				8: str := 'Freehand Line';
				9: str := '3D Locus';
				10: str := 'Text';
				11: str := 'Group';
				12: str := 'Quarter Arc';
				13: str := 'Rounded Rectangle';
				14: str := 'Image (GIF, JPG, BMP)';
				15: str := 'Placed Symbol';
				16: str := 'Symbol Definition';
				17: str := '2D Locus';
				18: str := 'Worksheet';
				21: str := 'Polyline';
				22: str := 'PICT Image';
				24: str := 'Extrude';
				25: str := '3D Polygon';
				29: str := 'Layer Link';
				30: str := 'Dash Pattern';
				31: str := 'Layer';
				32: str := 'Header';
				33: str := 'RefList';
				34: str := 'Sweep';
				35: str := 'Class List';
				38: str := 'Multiple Extrusion';
				39: str := 'Dim Standard';
				40: str := 'Mesh';
				41: str := 'Mesh Vertex';
				42: str := 'd33Node';
				43: str := 'Saved View';
				44: str := 'Render Spec';
				45: str := 'EPS';
				47: str := 'Record Format';
				48: str := 'PIO Record Format';
				49: str := 'Saved Sheet';
				51: str := 'Script Palette';
				54: str := 'SymList';
				55: str := 'RefName';
				56: str := 'Worksheet Image';
				57: str := 'Data';
				58: str := 'Linked Text';
				59: str := 'Macro';
				60: str := 'Worksheet Database';
				61: str := 'Worksheet Index';
				62: str := 'Worksheet Leader';
				63: str := 'Dimension';
				64: str := 'stringTD';
				65: str := 'Hatch Container';
				66: str := 'Hatch';
				67: str := 'bspProp';
				68: str := 'Wall';
				69: str := 'innerLines';
				71: str := 'Floor, column, or roof face';
				72: str := 'lineCol';
				74: str := 'fontTable';
				76: str := 'userData';
				77: str := 'workingPlane';
				78: str := 'wpList';
				79: str := 'PatList';
				80: str := 'ColorPalette';
				81: str := 'Light';
				82: str := 'Roof Edge';
				83: str := 'Roof';
				84: str := 'Solid CSG (addition, subtraction, union)';
				85: str := 'BoundaryRep';
				86: str := 'Plug-In Object';
				87: str := 'Roof Dormer';
				88: str := 'Subscribe';
				89: str := 'Rounded Wall';
				90: str := 'UndoPlaceholder';
				91: str := 'TextureSpace';
				92: str := 'Symbol Folder';
				93: str := 'Texture';
				94: str := 'Class';
				95: str := 'Solid (sphere, hemisphere, cone)';
				97: str := 'Texture Definition';
				98: str := 'ADSymDefHandler';
				99: str := 'ADSymbolHandler';
				110: str := 'Constraint';
				111: str := 'NURBS Curve';
				112: str := 'CorePrintInfo';
				113: str := 'NURBS Surface';
				114: str := 'CompositeSurface';
				115: str := 'RenderBackground';
				116: str := 'PolyBreak';
				117: str := 'BatchRenderJob';
				118: str := 'BatchRenderJobList';
				119: str := 'Image Fill Definition';
				120: str := 'Gradient Fill Definition';
				121: str := 'Fill Space';
				122: str := 'Viewport';
				123: str := 'Render Style';
				124: str := 'Association';
				127: str := 'Wall Style';
		END;
			AlrtDialog(Concat('Object is a ', str));
		END;
	END;
END;
RUN(Example);
```
#### Python ####
```python
def Example():
	objectTypes = {
			2: 'Line',
			3: 'Rectangle',
			4: 'Ellipse',
			5: 'Polygon',
			6: 'Arc/Circle',
			8: 'Freehand Line',
			9: '3D Locus',
			10: 'Text',
			11: 'Group',
			12: 'Quarter Arc',
			13: 'Rounded Rectangle',
			14: 'Image (GIF, JPG, BMP)',
			15: 'Placed Symbol',
			16: 'Symbol Definition',
			17: '2D Locus',
			18: 'Worksheet',
			21: 'Polyline',
			22: 'PICT Image',
			24: 'Extrude',
			25: '3D Polygon',
			29: 'Layer Link',
			30: 'Dash Pattern',
			31: 'Layer',
			32: 'Header',
			33: 'RefList',
			34: 'Sweep',
			35: 'Class List',
			38: 'Multiple Extrusion',
			39: 'Dim Standard',
			40: 'Mesh',
			41: 'Mesh Vertex',
			42: 'd33Node',
			43: 'Saved View',
			44: 'Render Spec',
			45: 'EPS',
			47: 'Record Format',
			48: 'PIO Record Format',
			49: 'Saved Sheet',
			51: 'Script Palette',
			54: 'SymList',
			55: 'RefName',
			56: 'Worksheet Image',
			57: 'Data',
			58: 'Linked Text',
			59: 'Macro',
			60: 'Worksheet Database',
			61: 'Worksheet Index',
			62: 'Worksheet Leader',
			63: 'Dimension',
			64: 'stringTD',
			65: 'Hatch Container',
			66: 'Hatch',
			67: 'bspProp',
			68: 'Wall',
			69: 'innerLines',
			71: 'Floor, column, or roof face',
			72: 'lineCol',
			74: 'fontTable',
			76: 'userData',
			77: 'workingPlane',
			78: 'wpList',
			79: 'PatList',
			80: 'ColorPalette',
			81: 'Light',
			82: 'Roof Edge',
			83: 'Roof',
			84: 'Solid CSG (addition, subtraction, union)',
			85: 'BoundaryRep',
			86: 'Plug-In Object',
			87: 'Roof Dormer',
			88: 'Subscribe',
			89: 'Rounded Wall',
			90: 'UndoPlaceholder',
			91: 'TextureSpace',
			92: 'Symbol Folder',
			93: 'Texture',
			94: 'Class',
			95: 'Solid (sphere, hemisphere, cone)',
			97: 'Texture Definition',
			98: 'ADSymDefHandler',
			99: 'ADSymbolHandler',
			110: 'Constraint',
			111: 'NURBS Curve',
			112: 'CorePrintInfo',
			113: 'NURBS Surface',
			114: 'CompositeSurface',
			115: 'RenderBackground',
			116: 'PolyBreak',
			117: 'BatchRenderJob',
			118: 'BatchRenderJobList',
			119: 'Image Fill Definition',
			120: 'Gradient Fill Definition',
			121: 'Fill Space',
			122: 'Viewport',
			123: 'Render Style',
			124: 'Association',
			127: 'Wall Style'
	}

	str = vs.StrDialog('Enter the name:', 'Window')
	if not vs.DidCancel():
		h = vs.GetObject(str)
		if h != None:		
			vs.AlrtDialog(vs.Concat('Object is a ', objectTypes[vs.GetType(h)]))


Example()
```

## See Also
From VW 2010+: [GetTypeN| GetTypeN](GetTypeN|%20GetTypeN.md)

## Version
Availability: from All Versions. Deprecated from VW 2010+.

## Category
* [Object Info](../Categories/Object%20Info.md)
