## VectorScript

```pascal
PROCEDURE Example;
{ This example demonstrates how to duplicate multiple objects by preserving the constraints between them.}
{ We will duplicate all objects on the active layer, 
{ create a new layer and insert them into it and select them.}
CONST
   newLayerName = 'MyNewLayer';
VAR
 srcLayerH, srcLayerList, newLayerH : HANDLE;  
   
FUNCTION DoMultipleDuplicate(h :HANDLE) :BOOLEAN;
VAR
 dupH : HANDLE;
BEGIN
   
   dupH := CreateDuplicateObject(h, NIL);  { copy and insert into active layer }
   SetSelect(dupH);
   
END;

FUNCTION BuildModel(h :HANDLE) :BOOLEAN;

BEGIN
   BuildConstraintModelForObject(h, FALSE); 
   { 'traverseContainers' is set to FALSE because we are getting here from a ForEach call}
   { that already goes deep inside containers}
END;


BEGIN
 srcLayerH := ActLayer;
 srcLayerList := FActLayer;  
 newLayerH := CreateLayer(newLayerName,1);
 IF ((srcLayerH <> ActLayer) & (srcLayerList <> NIL)) THEN  BEGIN
    { start a multiple objects duplicate that preserves constraints}
    BeginMultipleDuplicate;
    { duplicate all objects }
    ForEachObjectInList(DoMultipleDuplicate, 0, 0, srcLayerList);
    { end the multiple duplicate process} 
    EndMultipleDuplicate;
 END;

 { all objects in the first layer have been duplicated and inserted into the new layer }
 { we must build a contraint model for the duplicated objects }
 ForEachObjectInLayer(BuildModel, 0, 2, 0);

  
END;
RUN(Example);
```

## Python

```python
def DoMultipleDuplicate(h):
	dupH = vs.CreateDuplicateObject(h, None) # copy and insert into active layer
	vs.SetSelect(dupH)

def BuildModel(h):
	vs.BuildConstraintModelForObject(h, False) 
	# 'traverseContainers' is set to FALSE because we are getting here from a ForEach call
	# that already goes deep inside containers

def Example():
	# This example demonstrates how to duplicate multiple objects by preserving the constraints between them.
	# We will duplicate all objects on the active layer, 
	# create a new layer and insert them into it and select them.
	newLayerName = "MyNewLayer"

	srcLayerH = vs.ActLayer()
	srcLayerList = vs.FActLayer()  
	newLayerH = vs.CreateLayer(newLayerName,1)

	if ((srcLayerH != vs.ActLayer()) & (srcLayerList != None)):
		# start a multiple objects duplicate that preserves constraints
		vs.BeginMultipleDuplicate()
		# duplicate all objects
		vs.ForEachObjectInList(DoMultipleDuplicate, 0, 0, srcLayerList)
		# end the multiple duplicate process
		vs.EndMultipleDuplicate()

	# all objects in the first layer have been duplicated and inserted into the new layer
	# we must build a contraint model for the duplicated objects
	vs.ForEachObjectInLayer(BuildModel, 0, 2, 0)

Example()
```
