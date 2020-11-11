# Realms Invasion 'Info Center': **Tutorials - Prototypes - Protoframe - Debug System**

Welcome to the **Tutorials - Prototypes - Protoframe - Debug System ** page of the Realms Invasion Info Center. 
This 'Info Center' is the public knowledge database for the Realms Invasion Mods for Project Zomboid

A few things to note, 
Realms Invasion is a new and WIP project which means that things are subject to change alot between releases so please I ask you keep coming back from time to time

This page covers how to work with Invade 'Protoframe's Debug System

## **Index**
- [**Home**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/README.md)
- [**About the Repo**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/README.md#about-the-repo)
- [**About Project 'Realms'**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/AboutProjectRealms.md)
- [**What is Realms Invasion**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/README.md#what-is-realms-invasion)
    - [**What is Realms of Reality**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/AboutRealmsOfReality.md)
    - [**Realms Invasion Features**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/README.md#realms-invasion-features)
- [**Tutorials Home**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Tutorials/TutorialsHome.md)
- [**Index**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Tutorials/Prototypes/Protoframe/DebugSystem.md#index)
    - [**About**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Tutorials/Prototypes/Protoframe/DebugSystem.md#about)
    - [**Required Apps**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Tutorials/Prototypes/Protoframe/DebugSystem.md#required-apps)
    - [**Required knowledge**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Tutorials/Prototypes/Protoframe/DebugSystem.md##required-knowledge)
    - [**Sections**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Tutorials/Prototypes/Protoframe/DebugSystem.md#sections)
		- [**Load Enforcement**]()
		- [**Broken State**]()
		- [**Debug Logging Feature**]()
		- [**Call Result Feature**]()
		- [**Try Catch Feature**]()
		- [**Basic Errors Feature**]()
    - [**Related Tutorials**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Tutorials/Prototypes/Protoframe/DebugSystem.md#related-tutorials)

### **About**

This system provides some advanced high level features which are used to make the lives of modders much easier by providing a set of tools to help with the debugging and Error handling in a easy to use way.

### **Required Apps**

The following apps are required to complete this tutorial.

|**AppName**|**Req Type**|**Desc**|
|:---:|:---:|:---|
|Text Editor|Required|A text editor or a IDE is required due to editing lua files which are text|
|Visual Studio Code|Perfered|A free coding IDE with components what make it much better|

### **Required knowledge**

The following knowledge or the will to learn are required before attempting

|**Knowledge**|**Level**|**Desc**|
|:---:|:---:|:---|
|Lua|Basic|A basic understand of the lua language is required to understand this tutorial|
|[Load Enforcement]()|Basic|A basic understanding of the concept used to ensure systems are loaded and installed|
|[Broken State]()|Basic|A basic understanding of the concept used to ensure that the system your working with is not broken is required.

### **Sections**

#### **Load Enforcement**

To ensure that that both the Debug System and Error System are installed we put the following lines of code at the top of all files that are going to use this system (Which when working with 'Protoframe' or 'Prototype' this will be required)

```lua
-- First check to make sure that the 'Framework System' is Installed and loaded
if not Invade then require "Invade/Frame" end;
-- Check to make sure the debugging system is Installed and Ready for use
if not Invade.Debug then require "Invade/Debug" end;
```

#### **Broken State**

The next step we need to do is make sure that the Debug system is not broken, Unlike most system the Debug system uses a function call to know if it is broken. If it is I recomemend exiting out the script to keep from extensive errors from building up. This looks like the following below our load enforcement.

```lua
-- Check to make sure the Debug System is not broken
if Invade.Debug.IsBroken() then return end;
```

#### **Debug Logging Feature**

This system uses a custom logging feature which is built ontop of the normal 'print' feature of lua. This system is used along side [Call Result Feature](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Tutorials/Prototypes/Protoframe/DebugSystem.md#call-result-feature), [Try Catch Feature](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Tutorials/Prototypes/Protoframe/DebugSystem.md#try-catch-feature) to provide a unique debugging Experience. This feature uses one public method call to provide the logic to Log Messages, Call Results and Error Data. Along with a planned feature for scrubbing objects to print them for easier debugging of Objects.

This call looks like this (with all paramaters explains after)
```lua
Invade.Debug.LogMessage( "Info", "Hello World", false, "ProtoTest", "Debug", "Tutorial" );
```

The Paramaters are as follows (In order)
|Name|Expected Data|Type|Desc|
|:---:|:---:|:---:|:---|
|Error Type|String|Required|This is used to identify what type of message we are logging|
|Object|String, CallResult, ErrorData|Required|This is the value that we wish to log|
|Deep Trace|Bool or Nil|Required|This is used when logging errors to generate a deep trace to know what caused what|
|Project Name|string|Optinal|This is used to show in the log what project is logging the message|
|System|string|Optinal|This is used to show the message as coming from a given system in a project|
|Feature|string|Optinal|This is used to show the message as coming from a given feature in the given system|

#### **Call Result Feature**

This system uses what it calls 'CallResult' object to know if a given call is successful or not. This comes in three parts:
- Success
- Value
- Error

So lets go over each part, Up first is the Success value of the CallResult. This value is used to know if the call was successful or if there was an error. Next is Value, This is filled if the given successful call returned an object. If the call was not successful "Error" will be filled with a "ErrorData" object that is used to be able to narrow down errors more easily.

To generate a successful value you will do the following
```lua
function successfulCall()
	return Invade.Debug.CreateSuccess();
end
-- Or you can pass a value
function successfulCall()
	return Invade.Debug.CreateSuccess( { Message = "Hello World"})
end
```

To generate a error message you will do the following
```lua
function IE.Math.Devide( num1, num2 )
	if not num1 then return Invade.Debug.CreateFail("Num1 Can not be a nil value", nil, nil, "ProtoTest", "Math", "Devision") end;
	if not num2 then return Invade.Debug.CreateFail("Num2 Can not be a nil value", nil, nil, "ProtoTest", "Math", "Devision") end;
	if type(num1) ~= "number" then Invade.Debug.CreateFail("Num1 is not a number", nil, nil, "ProtoTest", "Math", "Devision") end;
	if type(num2) ~= "number" then return Invade.Debug.CreateFail("Num2 is not a number", nil, nil, "ProtoTest", "Math", "Devision") end;
	if num2 == 0 then return Invade.Debug.CreateFail("Can not devide by 0", nil, nil, "ProtoTest", "Math", "Devision") end;
	return Invade.Debug.CreateSuccess( num1/num2 );
end
```

The CreateFail function accepts the following Paramaters
|Name|Expected Data|Type|Desc|
|:---:|:---:|:---:|:---|
|Message|string (optinal check for registered Error Checks)|Required|The message or "ID" of a registered error Definition|
|Inner Error|string or ErrorData|Optinal|This is the error that caused your error to happen if any|
|CreateData|Table|Optinal|This is a table that is used to create error from the provided ID|
|Project|string|Optinal|This is a the name of the project throwing the error|
|System|string|Optinal|This is the name of the system throwing the error in the given project|
|Feature|string|Optinal|This is the name of the feature throwing the error in the given system|

#### **Try Catch Feature**

The try-catch feature is used to run code which uses both the [Call Result Feature](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Tutorials/Prototypes/Protoframe/DebugSystem.md#call-result-feature) along with a number of other feature to allow users to know if the call was successful or if there was some type of error. While many will feel this system is overkill. But to work with Invade 'Protoframe' you will need a understanding of this feature. It will be the most used feature.

Now to call a feature using this feature we do the following (the following will throw error to allow you to put code together yourself and test)
```lua
local health = 850;
local maxHealth = 0
-- Attempt to devide
local result = Invade.Debug.TryCatch( 
	IE.Math.Devide, 
	"Example showing features and how to uses errors and try catch",
	{
		Project = "Prototest",
		System = "Player",
		Feature = "Health Error Test"
	},
	health,
	maxHealth
);
-- On failure log the error message
if not result.Success then
	Invade.Debug.LogMessage( "Error", result.Error, true, "ProtoTest", "Player", "Health Error Test" );
	return;
end
```

**Invade.Debug.TryCatch: Paramaters**
|Name|Expected Data|Type|Desc|
|:---:|:---:|:---:|:---|
|Function|Function|Required|The function you want to call|
|Message|string|Required|The message or ID to be used for the error generation|
|CreateData|table or nil|Required|The data to be passed to error generation|
|Params|Param List|Required|The paramaters you want to pass to the function seperated by ,|

#### **Basic Errors**

This system provides some basic error definitions that are provided to give users some Common errors that can be used to simplify the process of development as well as keeping the number of errors down.

|**Knowledge**|**Level**|**Desc**|
|:---:|:---:|:---|
|Protoframe - Error System - Error Defs|Basic|A basic understanding of what a error definition is|
|Protoframe - Error System - Error Data|Basic|A basic understanding of what a error object is|
|[Protoframe - Debug System - Try Catch](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Tutorials/Prototypes/Protoframe/DebugSystem.md#try-catch-feature)|Basic|A basic understanding of how to use the try catch feature|
|[Protoframe - Debug System - CallResult](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Tutorials/Prototypes/Protoframe/DebugSystem.md#call-result-feature)|Basic|A basic understanding of the call result feature|

**Nil Arg**

This error is used to allow us to throw a unique message unique to nil values that shouldnt be. For this tutorial I will be updating the example math function to use the error definition.
**ErrorID: Invade.Debug.NilArg**
```lua
function IE.Math.Devide( num1, num2 )
	if not num1 then 
		return Invade.Debug.CreateFail(
			"Invade.Debug.NilArg", 
			nil,
			{ 
				ID = "num1", 
				Project = "ProtoTest", 
				System = "Math", 
				Feature = "Division"
			}
		);
	end;
	if not num2 then 
		return Invade.Debug.CreateFail(
			"Invade.Debug.NilArg", 
			nil, 
			{ 
				ID = "num2", 
				Project = "ProtoTest", 
				System = "Math", 
				Feature = "Division" 
			}
		); 
	end;
	if type(num1) ~= "number" then Invade.Debug.CreateFail("Num1 is not a number", nil, nil, "ProtoTest", "Math", "Devision") end;
	if type(num2) ~= "number" then return Invade.Debug.CreateFail("Num2 is not a number", nil, nil, "ProtoTest", "Math", "Devision") end;
	if num2 == 0 then return Invade.Debug.CreateFail("Can not devide by 0", nil, nil, "ProtoTest", "Math", "Devision") end;
	return Invade.Debug.CreateSuccess( num1/num2 );
end
```

You will notice this time we used the createData paramater of the create fail, and dropped the project, system and features from the func. moving those last 3 to the create data. This allows the system to customize the ErrorData filling the infomation based on the create data.

**NilArg - Create Data Params**
|FieldName|Desc|
|:---|:---|
|Param|This is the value name that should not be nil|
|Project|This customizes the error as to coming from given project|
|System|This customizes the error as to coming from system from given project|
|Feature|This customizes the error as coming from a given feature inside given system|


**Wrong Type**

This error is used to identify that a given paramater is not the correct type.
**ErrorID: Invade.Debug.WrongType**
To show this error I will be again updating the math example to use this error
```lua
function IE.Math.Devide( num1, num2 )
	if not num1 then return Invade.Debug.CreateFail("Invade.Debug.NilArg", nil, { Param = "num1", Project = "ProtoTest", System = "Math", Feature = "Division" }) end;
	if not num2 then return Invade.Debug.CreateFail(Invade.Debug.CreateFail("Invade.Debug.NilArg", nil, { Param = "num2", Project = "ProtoTest", System = "Math", Feature = "Division" }) end;
	if type(num1) ~= "number" then 
		Invade.Debug.CreateFail(
			"Invade.Debug.WrongType", 
			nil, 
			{
				Param = "num1",
				Expect = "number",
				Current = num1,
				Project = "ProtoTest", 
				System = "Math", 
				Feature = "Division"
			}
		)
	end;
	if type(num2) ~= "number" then 
		return Invade.Debug.CreateFail(
			"Invade.Debug.WrongType", 
			nil, 
			{
				Param = "num2",
				Expect = "number",
				Current = num1,
				Project = "ProtoTest",
				System = "Math",
				Feature = "Division"
			}
		);
	end;
	if num2 == 0 then return Invade.Debug.CreateFail("Can not devide by 0", nil, nil, "ProtoTest", "Math", "Devision") end;
	return Invade.Debug.CreateSuccess( num1/num2 );
end
```

**WrongType - Create Data Params**
|FieldName|Desc|
|:---|:---|
|Param|This is the value name that is the wrong type|
|Current|This is the obj for error to get the type (using frame)|
|Expect|This is the string value of the type that is to be expected|
|Project|This customizes the error as to coming from given project|
|System|This customizes the error as to coming from system from given project|
|Feature|This customizes the error as coming from a given feature inside given system|

### **Related Tutorials**

- [**Protoframe - Errors System**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Tutorials/Prototypes/Protoframe/ErrorsSystem.md)
- [**Protoframe - Frame System**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Tutorials/Prototypes/Protoframe/FrameSystem.md)
- [**Protoframe - GameLink System**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Tutorials/Prototypes/Protoframe/GameLinkSystem.md)