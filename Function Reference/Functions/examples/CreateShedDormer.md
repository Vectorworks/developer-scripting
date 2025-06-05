==== VectorScript ====
```pascal
PROCEDURE Test; 
VAR
    roofHandle : HANDLE; 
	shedID : INTEGER;
BEGIN
    roofHandle := CreateRoof(TRUE,5 1/2",5 1/2",4,9.52627");
	AppendRoofEdge(roofHandle,-77'10",-25'3.18078",#45,2'0",10'0");
	AppendRoofEdge(roofHandle,-41'2",-25'3.18078",#45,2'0",10'0");
	AppendRoofEdge(roofHandle,-41'2",21'4.81922",#45,2'0",10'0");
	AppendRoofEdge(roofHandle,-77'10",21'4.81922",#45 ,2'0",10'0");
	shedID:=CreateShedDormer(roofHandle);
	SetShedAttributes(roofHandle,shedID,TRUE,6'0",10'0",2'0",#8);
	SetDormerAttributes(roofHandle,shedID,3,18'4",TRUE,3'0",63,FALSE, 3'0");
	SetDormerThick(roofHandle, 2",1.83333");
END; 
RUN(Test);
```

==== Python ====
```python
def Test():
	roofHandle = vs.CreateRoof(True,5*12+1/2,5*12+1/2,4,9.52627)
	vs.AppendRoofEdge(roofHandle,-77*12+10,-25*12+3.18078,45,2*12,10*12)
	vs.AppendRoofEdge(roofHandle,-41*12+2,-25*12+3.18078,45,2*12,10*12)
	vs.AppendRoofEdge(roofHandle,-41*12+2,21*12+4.81922,45,2*12,10*12)
	vs.AppendRoofEdge(roofHandle,-77*12+10,21*12+4.81922,45 ,2*12,10*12)
	shedID=vs.CreateShedDormer(roofHandle)
	vs.SetShedAttributes(roofHandle,shedID,True,6*12,10*12,2*12,8)
	vs.SetDormerAttributes(roofHandle,shedID,3,18*12+4,True,3*12,63,False, 3*12)
	vs.SetDormerThick(roofHandle, 2,1.83333)
Test()
```
