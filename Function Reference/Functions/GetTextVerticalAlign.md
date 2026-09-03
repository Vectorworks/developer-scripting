# GetTextVerticalAlign

## Description
Function GetTextVerticalAlign returns the vertical alignment of the referenced text object.

![Text Locus](files/Textlocus.gif)

**Table - Text Vertical Justification**

| Justification        | Constant |
|--------------------- |----------|
| Top of text box      | 1        |
| Top baseline         | 2        |
| Text centerline      | 3        |
| Bottom baseline      | 4        |
| Bottom of text box   | 5        |

```pascal
FUNCTION GetTextVerticalAlign(TextHd : HANDLE): INTEGER;
```

```python
def vs.GetTextVerticalAlign(TextHd):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|TextHd|HANDLE|Handle to text object.|

## Examples
```pascal
textDown := (GetTextVerticalAlign (H) = 1);

textDown := (GetTextVerticalAlign (gRevTextH) = 1);

	END;
PushAttrs;
Marker(0,0,0);
CreateText('X');
VertAlign := GetTextVerticalAlign(LNewObj);{Not currently in Attrs call}
DelObject(LNewObj);
ClName:=ActiveClass;
ALName := GetLName(ActLayer);
 LayerOpt:=GetLayerOptions;
```
```python
import vs

# Function GetTextVerticalAlign returns the vertical alignment of the
# referenced text object.
TextHd = vs.FSActLayer()  # handle to the first selected object on the active layer

resultN = vs.GetTextVerticalAlign(TextHd)
vs.Message('GetTextVerticalAlign returned: ' + str(resultN))
```

## See Also
VS Functions:
* [SetTextVerticalAlign](SetTextVerticalAlign.md) | [SetTextVertAlignN](SetTextVertAlignN.md)
* [GetTextJust](GetTextJust.md) | [SetTextJust](SetTextJust.md) | [SetTextJustN](SetTextJustN.md)

## Version
Availability: from VectorWorks 8.0

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
