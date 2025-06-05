If you need to traverse all objects in the document, you'll have to traverse all layers and then list the objects in each one:

## VectorScript

```pascal
PROCEDURE ListDocument;
VAR
	hLayer, h : HANDLE;
BEGIN
	hLayer := GetParent( FObject );
	WHILE hLayer <> NIL DO BEGIN
		h := FInLayer( hLayer );
		WHILE h <> NIL DO BEGIN
			AlrtDialog( Concat( 'h=', h, ' type=', GetTypeN(h) ) );

			h := NextObj( h );
		END;

		hLayer := NextLayer( hLayer );
	END;
END;
Run(ListDocument);
```

## Python

```python
def ListDocument():
	hLayer = vs.GetParent( vs.FObject() )
	while hLayer != None:
		h = vs.FInLayer( hLayer )
		while h != None:
			vs.AlrtDialog( vs.Concat( 'h=', h, ' type=', vs.GetTypeN(h) ) )
			h = vs.NextObj( h )
		hLayer = vs.NextLayer( hLayer )

ListDocument()
```
