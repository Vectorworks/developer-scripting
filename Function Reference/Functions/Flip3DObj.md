# Flip3DObj

## Description
This function will flip a 3D object either horizontally or vertically. Its main use is for withing plugin objects when building their geometry and there is a need to mirror a piece.<BR>
<BR>
The supported types are: Extrude, Sweep, MultiExtrude, Symbol, Mesh and CSGNode.

```pascal
PROCEDURE Flip3DObj(
				h     : HANDLE;
				horiz : BOOLEAN);
```

```python
def vs.Flip3DObj(h, horiz):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|The handle of the 3D object to flip.|
|horiz|BOOLEAN|TRUE for a horizonal flip, FALSE for a vertical flip.|

## Examples
```pascal
PROCEDURE FlipTest;
{This script will create an extrude, dupicate it and then flip it horizontally}
VAR h1, h2 : HANDLE;

BEGIN

ClosePoly;

BeginXtrd(0', 4');
    BeginPoly;
	AddPoint( -5', 3' );
	AddPoint( 0, 3' );
	AddPoint( 0, 6' );
	AddPoint( 5', 0 );
	AddPoint( 0, -6');
	AddPoint( 0', -3');
	AddPoint(-5', -3');
    EndPoly;
EndXtrd;

h1 := LNewObj;


Move3DObj( h1, 5', 0 , 0 );
h2 := CreateDuplicateObject( h1, NIL );

Flip3DObj( h2 , TRUE );
Move3DObj( h2, -5', 0, 0 );

END;

Run(FlipTest);
```

## Version
Availability: from Vectorworks 2010

## Category
* [Objects - 3D](../Categories/Objects%20-%203D.md)
