#### VectorScript

```pascal
PROCEDURE Example;
{ Create a new hatch and add it to the resource list. }
VAR
	roofHandle : HANDLE;
	gabID : INTEGER;
	batID : INTEGER;
	hID : INTEGER;
BEGIN
	roofHandle:=CreateRoof(TRUE,5 1/2",5 1/2",4,9.52627");
	AppendRoofEdge(roofHandle,-77'10",-25'3.18078",45",2'0",10'0");
	AppendRoofEdge(roofHandle,-41'2",-25'3.18078",45",2'0",10'0");
	AppendRoofEdge(roofHandle,-41'2",21'4.81922",45",2'0",10'0");
	AppendRoofEdge(roofHandle,-77'10",21'4.81922",45" ,2'0",10'0");
	gabID:=CreateGableDormer(roofHandle);
	SetGableAttributes(roofHandle,gabID,TRUE,6'0",10'0",2'0",#45,#45);
	SetDormerAttributes(roofHandle,gabID,3,18'4",TRUE,3'0",63,FALSE,
	3'0");
	SetDormerThick(roofHandle, 2",1.83333");
	
	batID := CreateBatDormer(roofHandle);
	SetBatAttributes(roofHandle,batID,TRUE,5'0",10'0",4'0",6'3",2'0",#8);
	SetDormerAttributes(roofHandle,batID,3,18'4",TRUE,3'0",63,FALSE,3'0");
	SetDormerThick(roofHandle, 2",1.83333");
	
	hID := CreateHipDormer(roofHandle);
	SetHipAttributes(roofHandle, hID,TRUE,6'0",10'0",2'0",#45,#45,#45);
	SetDormerAttributes(roofHandle,hID,3,18'4",TRUE,3'0",63,FALSE,3'0");
	SetDormerThick(roofHandle, 2",1.83333");
END;
RUN(Example);
```

#### Python

```python
def Example():
	roofHandle = vs.CreateRoof(True,5.5,5.5,4,9.52627)
	vs.AppendRoofEdge(roofHandle,-77*12+10,-25*12+3.18078,45,2*12,10*12)
	vs.AppendRoofEdge(roofHandle,-41*12+2,-25*12+3.18078,45,2*12,10*12)
	vs.AppendRoofEdge(roofHandle,-41*12+2,21*12+4.81922,45,2*12,10*12)
	vs.AppendRoofEdge(roofHandle,-77*12+10,21*12+4.81922,45 ,2*12,10*12)
	
	gabID = vs.CreateGableDormer(roofHandle)
	vs.SetGableAttributes(roofHandle,gabID,True,6*12,10*12,2*12,45,45)
	vs.SetDormerAttributes(roofHandle,gabID,3,18*12+4,True,3*12,63,False,3*12)
	vs.SetDormerThick(roofHandle, 2,1.83333)
	
	batID = vs.CreateBatDormer(roofHandle)
	vs.SetBatAttributes(roofHandle,batID,True,5*12,10*12,4*12,6*12 + 3,2*12,8)
	vs.SetDormerAttributes(roofHandle,batID,3,18*12 + 4,True,3*12,63,False,3*12)
	vs.SetDormerThick(roofHandle, 2,1.83333)
	
	hID = vs.CreateHipDormer(roofHandle)
	vs.SetHipAttributes(roofHandle, hID,True,6*12,10*12,2*12,45,45,45)
	vs.SetDormerAttributes(roofHandle,hID,3,18*12+4,True,3*12,63,False,3*12)
	vs.SetDormerThick(roofHandle, 2,1.83333)
Example()
```
