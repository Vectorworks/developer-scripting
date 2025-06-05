#### VectorScript

```pascal
PROCEDURE Example;
VAR
i : INTEGER;
BEGIN
i := IntDialog('Enter an integer:', '0');
IF NOT DidCancel THEN BEGIN
i := i*3;
Message(i);
END;
END;
RUN(Example);
```

#### Python

```python
def Example():
	i = vs.IntDialog('Enter an integer:', '0');
	if not vs.DidCancel():
		i = i*3
		vs.Message(i)
Example()
```
