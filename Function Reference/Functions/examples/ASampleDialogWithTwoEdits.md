#### Python

```python
def UIAskForStringsToReplace():
	# control IDs
	kOK             = 1
	kCancel         = 2
	kTxt1           = 4
	kTxt2           = 5
	kEdit1          = 6
	kTxt3           = 7
	kEdit2          = 8
	
	# dialog data
	UIAskForStringsToReplace.strFind		= ''
	UIAskForStringsToReplace.strReplace		= ''

	def CreateDialog():
		# Alignment constants
		kRight                = 1
		kBottom               = 2
		kLeft                 = 3
		kColumn               = 4
		kResize               = 0
		kShift                = 1

		dialog = vs.CreateResizableLayout( 'Rename All Symbols', True, 'OK', 'Cancel', True, False )

		# create controls
		vs.CreateStaticText( dialog, kTxt1, 'Replace a sub-string from all symbol names:', -1 )
		vs.CreateStaticText( dialog, kTxt2, 'Old sub-string:', -1 )
		vs.CreateEditText( dialog, kEdit1, '', 25 )
		vs.CreateStaticText( dialog, kTxt3, 'New sub-string:', -1 )
		vs.CreateEditText( dialog, kEdit2, '', 25 )

		# set relations
		vs.SetFirstLayoutItem( dialog, kTxt1 )
		vs.SetBelowItem( dialog, kTxt1, kTxt2, 0, 0 )
		vs.SetRightItem( dialog, kTxt2, kEdit1, 0, 0 )
		vs.SetBelowItem( dialog, kTxt2, kTxt3, 0, 0 )
		vs.SetRightItem( dialog, kTxt3, kEdit2, 0, 0 )

		# set alignments
		vs.AlignItemEdge( dialog, kEdit1, kLeft, 1, kShift )
		vs.AlignItemEdge( dialog, kEdit2, kLeft, 1, kShift )

		# set bindings
		vs.SetEdgeBinding        ( dialog, kEdit1, True, True, False, False )
		vs.SetEdgeBinding        ( dialog, kEdit2, True, True, False, False )

		return dialog
		
	def DialogHandler(item, data):
		if item == kOK: 
			UIAskForStringsToReplace.strFind		= vs.GetItemText( dialog, kEdit1 )
			UIAskForStringsToReplace.strReplace		= vs.GetItemText( dialog, kEdit2 )
	
		return item 
		
	dialog = CreateDialog()
	result = False
	if vs.RunLayoutDialog( dialog, DialogHandler ) == kOK:
		result = True
        
	return result, UIAskForStringsToReplace.strFind, UIAskForStringsToReplace.strReplace
	

ok, strFind, strReplace = UIAskForStringsToReplace()
vs.AlrtDialog( ok, ' - ', strFind, '-', strReplace )
```
