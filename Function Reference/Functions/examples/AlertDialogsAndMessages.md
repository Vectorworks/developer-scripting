## VectorScript

```pascal
PROCEDURE Example;
BEGIN
AlrtDialog('AlrtDialog');
AlertInform('AlertInform', 'advice', FALSE);
AlertCritical('AlertCritical', 'advice');
Message(YNDialog('YNDialog'));
Message(AlertQuestion('question', 'advice', 1, 'ok', 'cancel', 'a', 'b'));
END;
RUN(Example);
```

## Python

```python
def Example():
	vs.AlrtDialog('AlrtDialog')
	vs.AlertInform('AlertInform', 'advice', False)
	vs.AlertCritical('AlertCritical', 'advice')	
	vs.Message(vs.YNDialog('YNDialog'))
	vs.Message(vs.AlertQuestion('question', 'advice', 1, 'ok', 'cancel', 'a', 'b'))
Example()
```
