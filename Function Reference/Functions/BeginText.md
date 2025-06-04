# BeginText

## Description
Procedures BeginText creates a new text object in a VectorWorks document. All text specified between calls to BeginText and EndText will be part of the new text object.
Text may be specified in single quotes, or variables may be used..

To specify the insertion point of the new text object, use TextOrigin.

<b>Note:</b> This function is not available in Python. Use [[VS:CreateText]] instead.

```pascal
PROCEDURE BeginText;
```

## Remarks
([[User:CBM-c-|_c_]], 2015.12.19): If you draw text, it is important to have a proper text size on the document or you'll see the error "An incorrect object is described".

## See Also
VS Functions:
[EndText](EndText.md) 
| [CreateText](CreateText.md)

## Version
Availability: from All Versions

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
