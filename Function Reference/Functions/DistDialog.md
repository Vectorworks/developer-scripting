# DistDialog

## Description
Function DistDialog displays a dialog box which requests the user to enter a distance value.

DistDialog automatically screens for valid numeric input.

```pascal
FUNCTION DistDialog(
				request : STRING;
				default : STRING): REAL;
```

```python
def vs.DistDialog(request, default):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|request|STRING|Dialog user prompt string.|
|default|STRING|Default value for input field.|

## Examples
#### VectorScript ####
```pascal
Message(DistDialog('Enter a distance value:','0'));
```
#### Python ####
```python
vs.Message(vs.DistDialog('Enter a distance value:','0'))
```

```pascal
BEGIN
	num := DistDialog(GetPlugInString(4004), Num2StrF(pStation_Spacing));
	IF NOT DidCancel THEN BEGIN
		SetRField(objHand, objName, 'Station Spacing', Num2Str(8, num));
		GetStationPoints;
		ReCreateNurbs(FALSE);

		Index := NumVertices - 1;
	END; {IF OnLine}
END; {FOR Index := 1 TO (NumVertices - 1)}
IF AddVert THEN
	VerticalDist := DistDialog(tempPIS3003,''); {What is the vertical travel up and down to be added}
TheDistance := Distance2 - Distance1;
TheDistance := TheDistance + VerticalDist;
DistStr := Num2StrF(TheDistance);
SetDSelect(TheCable);

VerticalDist := DistDialog(GetPlugInString(3000), '0');
CurrClass := ActiveClass; {What is the vertical distance traveled ?}
{NameClass('Cable Length Marker');}
pathHd:= GetCustomObjectPath(TheCable);
NumVertices:= GetVertNum(pathHd);
```
```python
import vs

# Function DistDialog displays a dialog box which requests the user to enter
# a distance value.
request = 'Example'
default = 'Example'

distance = vs.DistDialog(request, default)
vs.Message('DistDialog returned: ' + str(distance))
```

## Version
Availability: from All Versions

## Category
* [Dialogs - Predefined](../Categories/Dialogs%20-%20Predefined.md)
