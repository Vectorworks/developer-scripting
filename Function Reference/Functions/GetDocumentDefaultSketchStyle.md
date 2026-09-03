# GetDocumentDefaultSketchStyle

## Description
Returns the document default sketch style.  Returns the string 'No Sketch' if the current sketch style is ?No Sketch?.

```pascal
FUNCTION GetDocumentDefaultSketchStyle : STRING;
```

```python
def vs.GetDocumentDefaultSketchStyle():
    return STRING
```

## Examples
```pascal
resultStr := GetDocumentDefaultSketchStyle;
```
```python
import vs

# Returns the document default sketch style.
text = vs.GetDocumentDefaultSketchStyle()
vs.Message('GetDocumentDefaultSketchStyle returned: ' + str(text))
```

## Version
Availability: from VectorWorks11.5

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
