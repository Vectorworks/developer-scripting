# SetLayerRenderMode

## Description
Sets the render mode of the referenced layer.

```pascal
PROCEDURE SetLayerRenderMode(
				theLayer      : HANDLE;
				newRenderMode : INTEGER;
				immediate     : BOOLEAN;
				doProgress    : BOOLEAN);
```

```python
def vs.SetLayerRenderMode(theLayer, newRenderMode, immediate, doProgress):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|theLayer|HANDLE|Handle of the layer|
|newRenderMode|INTEGER|New render mode to set|
|immediate|BOOLEAN|If true, then all rendering will take place before the call returns. Otherwise, any rendering that can take place in the background will be postponed until program execution re-enters the main event loop|
|doProgress|BOOLEAN|controls whether progress information is displayed during the operation|

## Remarks
newRenderMode index corresponds to those listed above in getlayerrendermode call. 

RenderNow  - controls whether the specified layer will be re-rendered when the render mode is changed or not.  

Display progress -  ??  This might control whether the screen updates as it is rendering or not.  I haven't been able to figure out a definite effect of this parameter.

## Examples
```pascal
{ restore saved view and delete it. }
VRestore( 'TempView' );
VDelete( 'TempView' );
SetLayerRenderMode( hObjLayer, nObjRender, TRUE, TRUE );
Layer(GetLName(ActLayer));{looks useless, but forces a layer redraw}

BEGIN
	Layer(GetLName(GetLayer(GetObject(RefGridPIOName))));
	SetLayerRenderMode( GetLayer(GetObject(RefGridPIOName)), pioTuneRenderMode, TRUE, TRUE );
	SetObjectVariableLongint( GetLayer(GetObject(RefGridPIOName)), 591, Name2Index( pioRWBackRsrcName ) );

BEGIN
	setview(rx,ry,rz,vx,vy,vz);
	SetPref (9873,FALSE);
	IF GetLayerRenderMode(hActLayer) <> LyrRendModeIndex THEN
		SetLayerRenderMode(hActLayer,LyrRendModeIndex,FALSE,TRUE);
END;
```
```python
import vs

# Sets the render mode of the referenced layer.
theLayer = vs.ActLayer()  # handle to the active design layer
newRenderMode = 0
immediate = True
doProgress = True

vs.SetLayerRenderMode(theLayer, newRenderMode, immediate, doProgress)
```

## Version
Availability: from VectorWorks10.0

## Category
* [Layers](../Categories/Layers.md)
