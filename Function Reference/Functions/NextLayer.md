# NextLayer

## Description
Function NextLayer returns a handle to the next layer in the document after the referenced. If the end of the list has been reached, the function returns NIL.

```pascal
FUNCTION NextLayer(h : HANDLE): HANDLE;
```

```python
def vs.NextLayer(h):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to layer.|

## Examples
[TraverseObjects](examples/TraverseObjects.md)

```pascal
	NumDesignLayers := NumDesignLayers+1;
	ExistLayer[NumDesignLayers,1] := GetLName(hTempLayer);
	ExistLayer[NumDesignLayers,2]:=kStrDisplay;
	END;
hTempLayer := NextLayer(hTempLayer);
IF kDebugGetData THEN Writeln(NumDesignLayers, ' : ',ExistLayer[I,1],' , ',ExistLayer[I,2]);
END;

BEGIN { TraverseLayers }
	hLayer := FLayer;
	WHILE ( NIL <> hLayer ) DO BEGIN
		TraverseGroups( FInLayer( hLayer ), bFMOnly );
		hLayer := NextLayer( hLayer );
	END;

	BEGIN
	AddChoice(dialog1,   5, GetLName(hTempLayer), 0);	{Layers}
	IF htempLayer = ActLayer THEN SelectChoice(dialog1, 5,0,TRUE);
	END;
hTempLayer := NextLayer(hTempLayer);
END;
```
```python
import vs

# Function NextLayer returns a handle to the next layer in the document after
# the referenced.
h = vs.FSActLayer()  # handle to the first selected object on the active layer

objHandle = vs.NextLayer(h)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```
See also in tutorials: [29. Cross-Layer Summary](ai%20examples/29_WorksheetCrossLayerSummary.md)

## Version
Availability: from All Versions

## Category
* [Document List Handling](../Categories/Document%20List%20Handling.md)
