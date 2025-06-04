# SetTextAdorner

## Description
This function creates a relationship between the specified text block and the text adorner such that when theText Block is scaled in a VP, the text adorner is also scaled. Several objects can be adorned to the same text object.

```pascal
FUNCTION SetTextAdorner(
				textBlock   : HANDLE;
				textAdorner : HANDLE;
				p           : REAL): Boolean;
```

```python
def vs.SetTextAdorner(textBlock, textAdorner, p):
    return Boolean
```

## Parameters
|Name|Type|Description|
|---|---|---|
|textBlock|HANDLE|The Text object being adorned.|
|textAdorner|HANDLE|The object used to adorn the specified text.|
|p|REAL|The point by which texts will be scaled.|

## Examples
```pascal
PROCEDURE Example;
VAR
theText      :HANDLE;
theShape : HANDLE;
restult :      BOOLEAN;
BEGIN
TextVerticalAlign(3);
TextJust(2);
MoveTo(0,0);
RectangleN(-.5&quot;,      -.5&quot;, 1, 0, 1&quot;, 1&quot;);
theShape :=      lNewObj;
CreateText('ID1');
theText :=      lNewObj;
restult :=      SetTextAdorner(theText,theShape,0,0);
END;
RUN(Example);
```

## Version
Availability: from Vectorworks 2011

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
