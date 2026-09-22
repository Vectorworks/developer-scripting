# GetPhaseByIndex

## Description
Function GetPhaseByIndex takes in a "index" integer value and returns the information for the phase in the "index" position of the document's phase list.  This information includes the name, date (string), and the description of the phase.  If an invalid index is passed into in, the name, date, and description will be empty and the function will return a fail value.

```pascal
FUNCTION GetPhaseByIndex(
				index           : INTEGER;
				VAR id          : LONGINT;
				VAR name        : STRING;
				VAR date        : STRING;
				VAR description : STRING) : BOOLEAN;
```

```python
def vs.GetPhaseByIndex(index):
    return (BOOLEAN, id, name, date, description)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|index|INTEGER||
|id|LONGINT|The id of the phase located in the "index" position of the document's phase list.|
|name|STRING|The name of the phase located in the "index" position of the document's phase list.|
|date|STRING|The date of the phase located in the "index" position of the document's phase list.|
|description|STRING|The description of the phase located in the "index" position of the document's phase list.|

## Version
Availability: from Vectorworks 2027

## Category
* [Phasing](Categories/Phasing.md)

