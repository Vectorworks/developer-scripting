# GetLocPt

## Description
Procedure GetLocPt returns the coordinate location of the referenced locus.

```pascal
PROCEDURE GetLocPt(
				h         : HANDLE;
				VAR pX,pY : REAL);
```

```python
def vs.GetLocPt(h):
    return p
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to locus.|
|p|REAL|Coordinates of locus point.|

## Remarks
([[User:CBM-c-|_c_]], 2022.01.19) In Python the tuple returned is always bidimensional in the form (0, 0).

Remember to add a third item (0, 0, 0) for usage in the Vector Routines such as [[VS:Vec2Ang]] or they will return gibberish.

## Examples
#### VectorScript ####
```python
PROCEDURE TEST;
VAR
	pt : VECTOR;
BEGIN
	Message( 'Set begin point' );
	CallTool( -221 ); { activates the locus tool }
	GetLocPt( FSActLayer, pt.x, pt.y );
	Message( pt );
END;
Run(TEST);
```
#### Python ####
```python
locObj = vs.FSActLayer()

# make sure a locus is selected or there will be an error. 
# Due to the nature of Python, CallTool from the example above 
# is not usable for fetching LSActLayer in the same running script.
if locObj!= vs.Handle() and vs.GetTypeN( locObj ) == 17: 
	pt = vs.GetLocPt( locObj )
	vs.AlrtDialog( str(pt) )
else:
	vs.AlrtDialog( 'Select a locus' )
```

## Version
Availability: from All Versions

## Category
* [Objects - 2D](../Categories/Objects%20-%202D.md)
