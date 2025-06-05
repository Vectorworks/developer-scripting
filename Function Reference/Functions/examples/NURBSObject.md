#### VectorScript

```pascal
PROCEDURE Example;
VAR
h :HANDLE;
BEGIN
h := FSActLayer;
h := ConvertToNURBS(h, FALSE);
h := CreateOffsetNurbsObjectHandle(h, 1);
END;
RUN(Example);
```

#### Python

```python
def Example():
	h = vs.FSActLayer()
	h = vs.ConvertToNURBS(h, False)
	h = vs.CreateOffsetNurbsObjectHandle(h, 1)
Example()
```
