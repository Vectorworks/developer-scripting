# GetDrawingSizeRect

## Description
Returns  the top left and bottom right coordinates of a rectangle surrounding the entire area of the document containing objects.

```pascal
PROCEDURE GetDrawingSizeRect(
				VAR p1X,p1Y : REAL;
				VAR p2X,p2Y : REAL);
```

```python
def vs.GetDrawingSizeRect():
    return (p1, p2)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|p1|REAL|Returns top left coordinate of drawing rectangle.|
|p2|REAL|Returns bottom right coordinate of drawing rectangle.|

## Remarks
(*\_c\_*, 2014.08.19): The returned coordinates are (current units, page) the top-left, bottom-right coordinates of the printable page in the active layer. These coordinates can vary if the active layer is sheet or design layer. The newer routine SetDrawingRectN allows to pass a handle to a layer.

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
p1X, p1Y, p2X, p2Y :REAL;
BEGIN
GetDrawingSizeRect(p1X, p1Y, p2X, p2Y);
Message(p1X, ' ', p1Y, ' ', p2X, ' ', p2Y);
END;
RUN(Example);
```
#### Python ####
```python
def Example():
	p1, p2 = vs.GetDrawingSizeRect()
	vs.Message(p1[0], ' ', p1[1], ' ', p2[0], ' ', p2[1])

Example()
```

```pascal
BEGIN
	GetDrawingSizeRect (p1X, p1Y, p2X, p2Y);
	size := p2X - p1X;
	IF (p1Y - p2Y) < size THEN size := p1Y - p2Y;
	SetRField (pluginH, pluginName, 'size', Num2StrF (size));
END

BEGIN
	GetDrawingSizeRect (p1X, p1Y, p2X, p2Y);
	xLength := p2X - p1X;
	yLength := p1Y - p2Y;
	SetRField (pluginH, recordName, 'xLength', Num2StrF (xLength));
	SetRField (pluginH, recordName, 'yLength', Num2StrF (yLength));

BEGIN
	GetDrawingSizeRect (p1X, p1Y, p2X, p2Y);
	scaleF := GetLScale (ActLayer);
	vertDim := ((p1Y - p2Y) / scaleF)/GetPrefReal (152);
	horizDim := ((p2X - p1X) / scaleF)/GetPrefReal (152);
```
```python
import vs

# Returns the top left and bottom right coordinates of a rectangle
# surrounding the entire area of the document containing objects.
p1, p2 = vs.GetDrawingSizeRect()
vs.Message('GetDrawingSizeRect returned: ' + str((p1, p2)))
```

## See Also
VS Functions:
* [SetDrawingRect](SetDrawingRect.md)
* SetDrawingRectN

## Version
Availability: from VectorWorks 8.0

## Category
* [Document Settings](../Categories/Document%20Settings.md)
