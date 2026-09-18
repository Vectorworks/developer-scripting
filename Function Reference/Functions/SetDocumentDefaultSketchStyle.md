# SetDocumentDefaultSketchStyle

## Description
Sets the document default sketch style.  Set sketchName to 'No Sketch' to set the document default sketch to 'No Sketch'.

```pascal
FUNCTION SetDocumentDefaultSketchStyle(sketchName : STRING): BOOLEAN;
```

```python
def vs.SetDocumentDefaultSketchStyle(sketchName):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|sketchName|STRING|Sketch Style name.|

## Examples
```pascal
resultOK := SetDocumentDefaultSketchStyle('Example');
```
```python
import vs

# Sets the document default sketch style.
sketchName = 'Example'

ok = vs.SetDocumentDefaultSketchStyle(sketchName)
if ok:
    vs.Message('SetDocumentDefaultSketchStyle succeeded')
else:
    vs.Message('SetDocumentDefaultSketchStyle failed')
```

## Version
Availability: from VectorWorks11.5

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
