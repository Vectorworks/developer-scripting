## VectorScript

```pascal
PROCEDURE Example;
VAR
hDTM :HANDLE;
hPoly3D : HANDLE;
x :REAL;
y :REAL;
z :REAL;
result :BOOLEAN;
BEGIN
	Poly(0,0,-0.5,1,0.5,1.5,2,1,1,-0.5);
	hPoly3D := LObject;
	hDTM := DTM6_GetDTMObject(ActLayer, True);
	IF DTM6_IsDTM6Object(hDTM) AND DTM6_IsObjectReady(hDTM) THEN 
	BEGIN
		IF DTM6_IsTypeVisible(hDTM, 4{is existing visible in 3D}) THEN 
		BEGIN
			result :=DTM6_GetZatXY(hDTM, 0{Existing}, x, y, z);
			result :=DTM6_SendToSurface(hDTM, hPoly3D, 0{Existing} );
		END else
		BEGIN
			result :=DTM6_GetZatXY(hDTM, 1{Proposed}, x, y, z);
			result :=DTM6_SendToSurface(hDTM, hPoly3D, 1{Proposed} );
		END;
	END;
END;
RUN(Example);
```

## Python

```python
def Example():
	vs.Poly(0,0,-0.5,1,0.5,1.5,2,1,1,-0.5)
	hPoly3D = vs.LObject()
	hDTM = vs.DTM6_GetDTMObject(vs.ActLayer(), True)
	if vs.DTM6_IsDTM6Object(hDTM) and vs.DTM6_IsObjectReady(hDTM):
		if vs.DTM6_IsTypeVisible(hDTM, 4):
			result, z = vs.DTM6_GetZatXY(hDTM, 0, x, y)
			result = vs.DTM6_SendToSurface(hDTM, hPoly3D, 0 )
		else:	
			result, z = vs.DTM6_GetZatXY(hDTM, 1, x, y)
			result = vs.DTM6_SendToSurface(hDTM, hPoly3D, 1)

Example()
```
