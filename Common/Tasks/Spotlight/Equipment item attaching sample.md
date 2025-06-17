By Nikolay Zhelyazkov

## Equipment Item attaching support

From Vectorworks 2023 SP4 Equipment Items can be attached to third party objects. When attached to an object the Equipment Item will follow the object when it gets moved. Additionally, some of the Equipment Item data can be kept in sync with the data of the attached object.

To be able to attach to Equipment Items your plug-in should implement the following event sync function and define the following extension property:

- **kObjXPropAllowEquipmentItemAttach** - Stores the name of the plug-in if it wants equipment items to be able to attach to it
- **OnEquipmentItemDataMessage** - Receives messages from the Equipment Item. **ParametricEquipmentItemDataMessage::EEquipmentItemDataContext** determines if the Equipment Item wants to Read from your plug-in or wants to Write to it.

```cpp
enum class EEquipmentItemDataContext
{
    Read,
    Write,
};
```

**EEquipmentItemField** determines which parameters of the Equipment Item can be kept in sync with your plug-in.

```cpp
enum class EEquipmentItemField
{
    Make,
    Model,
    WidthMM,
    HeightMM,
    DepthMM,
    PowerW,
    WeightKG,
};
```

## SDK Sample

### EventSink Sample

```cpp
class CSampleEquipment_EventSink : public VWParametric_EventSink
{
	// ...existing code...
public:
	virtual EObjectEvent	OnInitXProperties(CodeRefID objectID) override;
	virtual void		OnEquipmentItemDataMessage(ParametricEquipmentItemDataMessage& msg) override;

	// ...existing code...
};
```

### Setting the property

```cpp
EObjectEvent CSampleEquipment_EventSink::OnInitXProperties(CodeRefID objectID)
{
	using namespace VectorWorks::Extension;
	VCOMPtr<IExtendedProps>	extProps( IID_ExtendedProps );

	extProps->InitObjectProperties( objectID );
	// Allow equipment item attachment
	extProps->SetObjectProperty( objectID, kObjXPropAllowEquipmentItemAttach, fUnivName );

	return kObjectEventNoErr;
}
```

### Implementing the event

**Note** The event sends and receives data in the specified units: Width, Height and Depth in millimeters, Power in Watts and Weights in Kilograms. If your plug-in is using different units you have to do unit conversions here.

```cpp
void CSampleEquipment_EventSink::OnEquipmentItemDataMessage(ParametricEquipmentItemDataMessage& msg)
{
	VWParametricObj paramObj( fhObject );

	switch ( msg.fContext )
	{
		case EEquipmentItemDataContext::Read:
		{
			// Equipment item requested to read this data -> send all the data that you want the equipment item to read from your plug-in
			msg.fmapEquipItemFields[ EEquipmentItemField::Make ]		= paramObj.GetParamValue( "make" );
			msg.fmapEquipItemFields[ EEquipmentItemField::Model ]		= paramObj.GetParamValue( "model" );
			msg.fmapEquipItemFields[ EEquipmentItemField::WidthMM ]		= paramObj.GetParamValue( "widthMM" );
			msg.fmapEquipItemFields[ EEquipmentItemField::HeightMM ]	= paramObj.GetParamValue( "heightMM" );
			msg.fmapEquipItemFields[ EEquipmentItemField::DepthMM ]		= paramObj.GetParamValue( "depthMM" );
			msg.fmapEquipItemFields[ EEquipmentItemField::PowerW ]		= paramObj.GetParamValue( "powerW" );
			msg.fmapEquipItemFields[ EEquipmentItemField::WeightKG ]	= paramObj.GetParamValue( "weightKg" );
			break;
		}

		case EEquipmentItemDataContext::Write:
		{
			// Equipment Item sent this data update -> update any of your parameters that you want to be updated from the equipment item
			bool				didChange = false;
			TStringToEquipItemFieldMap	mapFieldToName;

			// Make a map to easily find the parameter name from the equipment item field
			mapFieldToName[ EEquipmentItemField::Make ]	= "make";
			mapFieldToName[ EEquipmentItemField::Model ]	= "model";
			mapFieldToName[ EEquipmentItemField::WidthMM ]	= "widthMM";
			mapFieldToName[ EEquipmentItemField::HeightMM ]	= "heightMM";
			mapFieldToName[ EEquipmentItemField::DepthMM ]	= "depthMM";
			mapFieldToName[ EEquipmentItemField::PowerW ]	= "powerW";
			mapFieldToName[ EEquipmentItemField::WeightKG ]	= "weightKg";

			for ( const auto& equipItemField : msg.fmapEquipItemFields )
			{
				const TXString& paramName = mapFieldToName[ equipItemField.first ];

				if ( equipItemField.second != paramObj.GetParamValue( paramName ) )
				{
					gSDK->AddBothSwapObject( paramObj );
					paramObj.SetParamValue( paramName, equipItemField.second );
					didChange = true;
				}
			}

			if ( didChange )
			{
				paramObj.ResetObject();
			}
			break;
		}

		default: break;
	}
}
```

## VectorScript Sample

```pascal
PROCEDURE Main;
VAR
	theEvent 	: LONGINT;
	theButton 	: LONGINT;
	objName 	: STRING;
	hObj		: HANDLE;
	hRec		: HANDLE;
	hWall		: HANDLE;
	bOK		: BOOLEAN;
	context 	: INTEGER;
	value 		: STRING;

BEGIN
	vsoGetEventInfo(theEvent, theButton);
	bOK := GetCustomObjectInfo(objName, hObj, hRec, hWall);

	CASE theEvent OF
		3:{Reset}
		BEGIN
			RectangleN(0, 0, 1, 0, pWidth, pDepth);			
			BeginXtrd(0, pHeight);
			RectangleN(0, 0, 1, 0, pWidth, pDepth);
			EndXtrd;
		END;

		5:{Init}
		BEGIN
			bOK := SetObjPropTxtVS(105{kObjXPropAllowEquipmentItemAttach}, objName);
		END;

		92:{ParametricEquipmentItemDataMessage}
		BEGIN
			context := vsoEIDataGetContext(theButton);
			
			IF context = 0 {Read}THEN
			BEGIN
				{Equipment items requested to read this data.}
				vsoEquipItemDataSet(theButton, 0{Make}, 	pMake);
				vsoEquipItemDataSet(theButton, 1{Model}, 	pModel);
				vsoEquipItemDataSet(theButton, 2{WidthMM}, 	Num2StrF(pWidth));
				vsoEquipItemDataSet(theButton, 3{HeightMM}, Num2StrF(pHeight));
				vsoEquipItemDataSet(theButton, 4{DepthMM}, 	Num2StrF(pDepth));
				vsoEquipItemDataSet(theButton, 5{PowerW}, 	Num2StrF(pPower));
				vsoEquipItemDataSet(theButton, 6{WeightKG}, Num2StrF(pWeight));
			END
			ELSE {Write}
			BEGIN
				bOK := FALSE;
				
				{Equipment Item sent this data update}
				IF vsoEquipItemDataGet(theButton, 0{Make}, value) THEN
				BEGIN
					IF value <> GetRField(hObj, objName, 'Make') THEN
					BEGIN
						SetRField(hObj, objName, 'Make', value);
						bOK := TRUE;
					END;
				END;
				
				IF vsoEquipItemDataGet(theButton, 1{Model}, value) THEN
				BEGIN
					IF value <> GetRField(hObj, objName, 'Model') THEN
					BEGIN
						SetRField(hObj, objName, 'Model', value);
						bOK := TRUE;
					END;
				END;
				
				{Do unit conversions if needed. Value in milimeters expected.}
				IF vsoEquipItemDataGet(theButton, 2{WidthMM}, value) THEN
				BEGIN
					IF value <> GetRField(hObj, objName, 'Width') THEN
					BEGIN
						SetRField(hObj, objName, 'Width', value);
						bOK := TRUE;
					END;
				END;
				
				{Do unit conversions if needed. Value in milimeters expected.}
				IF vsoEquipItemDataGet(theButton, 3{HeightMM}, value) THEN
				BEGIN
					IF value <> GetRField(hObj, objName, 'Height') THEN
					BEGIN
						SetRField(hObj, objName, 'Height', value);
						bOK := TRUE;
					END;
				END;
				
				{Do unit conversions if needed. Value in milimeters expected.}
				IF vsoEquipItemDataGet(theButton, 4{DepthMM}, value) THEN
				BEGIN
					IF value <> GetRField(hObj, objName, 'Depth') THEN
					BEGIN
						SetRField(hObj, objName, 'Depth', value);
						bOK := TRUE;
					END;
				END;
				
				{Do unit conversions if needed. Value in Watts expected.}
				IF vsoEquipItemDataGet(theButton, 5{PowerW}, value) THEN
				BEGIN
					IF value <> GetRField(hObj, objName, 'Power') THEN
					BEGIN
						SetRField(hObj, objName, 'Power', value);
						bOK := TRUE;
					END;
				END;
				
				{Do unit conversions if needed. Value in Kilograms expected.}
				IF vsoEquipItemDataGet(theButton, 6{WeightKG}, value) THEN
				BEGIN
					IF value <> GetRField(hObj, objName, 'Weight') THEN
					BEGIN
						SetRField(hObj, objName, 'Weight', value);
						bOK := TRUE;
					END;
				END;
				
				IF bOK THEN ResetObject(hObj);
			END;
		END;
	END;
END;

RUN(Main);
