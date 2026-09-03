# Run

## Description
Initiates the execution of a VectorScript command by signalling the VectorScript interpreter to execute the script source code.

The procedure takes a single parameter, which is the name of the VectorScript command as defined at the beginning of the source code listing.

```pascal
PROCEDURE Run(p : PROCEDURE);
```

```python
def vs.Run(p):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|p|PROCEDURE|   |

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
BEGIN
Sysbeep;
Sysbeep;
Sysbeep;
END;
RUN(Example);
```
#### Python ####
```python

```

```pascal
RUN (AngleObjectInch);

RUN (AngleObjectMetric);

		ForEachObjectInLayer(AnnotateThings, 2, 0, 4);
		IF gNothingDrawn THEN AlrtDialog(GetPlugInString(3012));
	END;
END;
RUN(AnnotateSegments);
```
```python
vs.Run((0, 0))
```

## Version
Availability: from All Versions

## Category
* [Command](../Categories/Command.md)
