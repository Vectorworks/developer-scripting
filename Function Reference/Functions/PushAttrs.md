# PushAttrs

## Description
Stores current attribute, tool, text, and constraint settings for later retrieval as the document default settings. Document settings can be modified as needed after using this call, and the stored settings can be restored with a call to PopAttrs.  Calling this function more than once (nested) is allowed.  The settings will be placed on a stack, and will be retrieved by calls to PopAttrs in the correct sequence.

```pascal
PROCEDURE PushAttrs;
```

```python
def vs.PushAttrs():
    return None
```

## Remarks
<pre>
Boolean          textV;     // true if picked up from textNode
Boolean          markV;     // true if picked up from markered object
ObjectColorType  cType;     // color record
short            ppat;      // pen pattern
short            fPat;      // fill pattern
ByClassFlagsType isByClass; // whether graphic attributes are 'by class';
LineType         lType;     // line width-dash
TDashPat         lDashPat;  // dash pattern definition
SegStyleType     sType;     // marker size and placement
short            tFont;     // font number
short            tSize;     // font size in pagespace
Style            tStyle;    // text style
Byte             tSpace;    // text spacing
Byte             tJust;     // text justification
Str255           cName;     // class name
long             wBits;     // bitfield of which attrs to paste
ObjRecHandle     dataList;
short            toolID;    // active tool
</pre>

The fields 'wBits' and 'dataList' do not appear to be used.

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
BEGIN
PushAttrs;
PenFore(215);
PenBack(5);
PenPat(25);
PenSize(42);
PenPat(25);
SetConstrain('q');
CallTool(-201);
PopAttrs;
END;
RUN(Example);
```
#### Python ####
```python

```

## See Also
VS Functions:
[PopAttrs](PopAttrs.md)

## Version
Availability: from MiniCAD4.0

## Category
* [Command](../Categories/Command.md)
