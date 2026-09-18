# NumSObj

## Description
Function NumSObj returns the number of selected objects on the referenced layer.

```pascal
FUNCTION NumSObj(h : HANDLE): LONGINT;
```

```python
def vs.NumSObj(h):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to layer.|

## Examples
```pascal
BEGIN
SetName(GetLayerByName(ExistLayer[(LayerMaping[I,1]),1]),NewLayer[I,1]);
IF kDebugText THEN Writeln ( 'Renamed : Old ',ExistLayer[(LayerMaping[I,1]),1],'New ',NewLayer[I,1],' Num of Elements ',NumSObj(ActLayer));
END

BEGIN
	IF ( NumSObj( GetLayer ( objHand ) )  > 1 ) THEN
	BEGIN
		vsoWidgetSetEnable( 1, FALSE );
	END

	END; {NOT End of Infile}
Wait(1);
ClrMessage;
Close(InFile);
IF (NumSObj(ActLayer) > 0) THEN
			BEGIN
				AlrtDialog(GetPlugInString(5006));
			END;
```
```python
import vs

# Function NumSObj returns the number of selected objects on the referenced
# layer.
h = vs.FSActLayer()  # handle to the first selected object on the active layer

count = vs.NumSObj(h)
vs.Message('NumSObj returned: ' + str(count))
```

## Version
Availability: from All Versions

## Category
* [Selection](../Categories/Selection.md)
