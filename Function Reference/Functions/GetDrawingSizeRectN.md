# GetDrawingSizeRectN

## Description
Returns the top left and bottom right coordinates of a rectangle surrounding the entire area of the document containing objects.<BR>
<BR>
Similar to GetDrawingSizeRect but can work on specified layer.

```pascal
PROCEDURE GetDrawingSizeRectN(
				hLayer : HANDLE;
				VAR p1 : REAL;
				VAR p2 : REAL);
```

```python
def vs.GetDrawingSizeRectN(hLayer):
    return (p1, p2)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hLayer|HANDLE|The layer to be used for calculating the drawing rectangle.|
|p1|REAL|Returns top left coordinate of drawing rectangle.|
|p2|REAL|Returns bottom right coordinate of drawing rectangle.|

## See Also
VS Functions:
[GetDrawingSizeRect](GetDrawingSizeRect.md)

## Version
Availability: from Vectorworks 2014

## Category
* [Document Settings](../Categories/Document%20Settings.md)
