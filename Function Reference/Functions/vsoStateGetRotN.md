# vsoStateGetRotN

```pascal
FUNCTION vsoStateGetRotN(
				hObj           : HANDLE;
				VAR outDiffAng : VECTOR;
				VAR outIs3D    : BOOLEAN): BOOLEAN;
```

```python
def vs.vsoStateGetRotN(hObj):
    return (BOOLEAN, outDiffAng, outIs3D)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObj|HANDLE|   |
|outDiffAng|VECTOR|   |
|outIs3D|BOOLEAN|   |

## Examples
```pascal
BEGIN
	{check for forward translate first}
	IF	( vsoStateGetRotN( parmHand, outDiffAng, outIs3D ) = FALSE )
	&	( vsoStateGet( parmHand, kObjectStateReshaped ) = FALSE )
	&	ValidNumStr( GetRField( parmHand, parmName, kStrHangingAngle ), oldHangingAngle )
	&	ValidNumStr( GetRField( parmHand, parmName, 'Rotation' ), oldSpin ) THEN
	BEGIN
		IF 	( gHangingAngle = 0 ) & ( Spin = 0 )
		& 	( 	( Eq( oldHangingAngle, gHangingAngle, 1 ) = FALSE )
			| 	( Eq( oldSpin, Spin, 1 ) = FALSE )  ) THEN
		{the angles in the matrix are different from the parameters}
		BEGIN
```
```python
import vs

hObj = vs.FSActLayer()  # handle to the first selected object on the active layer

ok, outDiffAng, outIs3D = vs.vsoStateGetRotN(hObj)
vs.Message('vsoStateGetRotN returned: ' + str((ok, outDiffAng, outIs3D)))
```

## Version
Availability: from Vectorworks 2020

## Category
* [Object Events](../Categories/Object%20Events.md)
