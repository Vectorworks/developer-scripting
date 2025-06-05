#### VectorScript

```pascal
{ example from unknown author on Vectorlab, Dec 2006 }
PROCEDURE IsolateLayer; {sets selected object's layer to active and greys all others}
VAR
    x, y: Real;
    h, layHand: Handle;
    layName: STRING;
BEGIN
    GetPt(x, y);
    h := PickObject(x, y);

    IF h <> NIL THEN BEGIN
        SetSelect(h);
        layHand := GetLayer(h);
        layName := GetLName(layHand);
        Layer(layName);
        SetLayerOptions(2);

        SetDSelect(h);
    END;
END;
Run(IsolateLayer);
```

#### Python

```python
def PickPointCallback(pt):
	h = vs.PickObject(pt[0], pt[1])
	if h != None:
		vs.SetSelect(h)
		layHand = vs.GetLayer(h)
		layName = vs.GetLName(layHand)
		vs.Layer(layName)
		vs.SetLayerOptions(2)
		vs.SetDSelect(h)
    
def IsolateLayer(): # sets selected object's layer to active and greys all others
    vs.GetPt(PickPointCallback)
    
IsolateLayer()
```
