# Realms Invasion 'Info Center': **PZ Mods - Prototypes - Protoframe**

Welcome to the **PZ Mods - Prototypes - Protoframe** page of the Realms Invasion Info Center. 
This 'Info Center' is the public knowledge database for the Realms Invasion Mods for Project Zomboid

A few things to note, 
Realms Invasion is a new and WIP project which means that things are subject to change alot between releases so please I ask you keep coming back from time to time

This page covers the active development infomation of all things related to Invade 'Protoframe'.

## **Index**
- [**Home**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/README.md)
- [**About the Repo**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/README.md#about-the-repo)
- [**About Project 'Realms'**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/AboutProjectRealms.md)
- [**What is Realms Invasion**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/README.md#what-is-realms-invasion)
    - [**What is Realms of Reality**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/AboutRealmsOfReality.md)
    - [**Realms Invasion Features**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/README.md#realms-invasion-features)
- [**Index**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Mods/Prototypes/Protoframe/InvadeFrame.md#index)
- [**About**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Mods/Prototypes/Protoframe/InvadeFrame.md#about)
	- [**Project Details**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Mods/Prototypes/Protoframe/InvadeFrame.md#project-details)
	- [**Systems**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Mods/Prototypes/Protoframe/InvadeFrame.md#systems)

### **About**

Some Key Features include
|Name|Desc|
|:---|:---|
|Inline Errors|A feature to allow for custom errors which are not reliant on the game's normal error system.|
|Error Defs|A feature to allow users to define thier own Error Defs that can be used to make debugging easier|
|Error Assembly|A feature to allow the system to build error details from details provided by the user|
|Debug Logging|A feature to make projects easier to develop by giving the logged details look different enough to make it easier Identify your messages|
|Call Results|A feature used to make the system able to know if a call was successful without using the normal Lua error system|

### **Project Details**

|Name|Detail|
|:---:|:---|
|Project ID|Invade.Frame|
|Dev Version|V 1.0.0|
|Public Version|V ---|
|Beta Version|V ---|
|Steam Version|V ---|
|Name|Invade Prototype Framework|
|Desc|This project provides modders with a set collection of features which are meant to make developing PZ mods much easier|

### **Systems**

This section covers the current Systems in the Development Version of this project.

**Systems:**

- [**Debug System**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Mods/Prototypes/Protoframe/InvadeFrame.md#debug-system)
- [**Error System**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Mods/Prototypes/Protoframe/InvadeFrame.md#error-system)
- [**Frame System**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Mods/Prototypes/Protoframe/InvadeFrame.md#frame-system)
- [**Game Link System**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Mods/Prototypes/Protoframe/InvadeFrame.md#game-link-system)

#### **Debug System**

|Detail|Value|
|:---|:---|
|System ID|Frame.Debug|
|Name|Debugging System|
|Dev Version|V 1.0|
|Public Version|V ---|
|Beta Version|V ---|
|Steam Version|V ---|
|Desc|This system is used to help modders with the task of debugging thier projects|

**Features:**
- [**Raw Try Catch Feature**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Mods/Prototypes/Protoframe/InvadeFrame.md#raw-try-catch-feature)
- [**Try Catch Feature**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Mods/Prototypes/Protoframe/InvadeFrame.md#try-catch-feature)
- [**Call Result Feature**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Mods/Prototypes/Protoframe/InvadeFrame.md#call-result-feature)
- [**Debug Logging Feature**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Mods/Prototypes/Protoframe/InvadeFrame.md#debug-logging-feature)

##### **Raw Try Catch Feature**

|Detail|Value|
|:---|:---|
|Feature ID|Debug.RawTry|
|Name|Raw Try Catch Feature|
|Dev Version|V 1.0|
|Public Version|V ---|
|Beta Version|V ---|
|Steam Version|V ---|
|Desc|This feature allows the debug system to call code and if any errors are thrown from either Java or Lua, this feature will catch the error and build a Result and error with the details.|

##### **Try Catch Feature**

|Detail|Value|
|:---|:---|
|Feature ID|Debug.TryCatch|
|Name|Inline Errors Feature|
|Dev Version|V 1.0|
|Public Version|V ---|
|Beta Version|V ---|
|Steam Version|V ---|
|Desc|This feature allows users to try to run logic, catching any errors that are encountered at runtime and building Proper Error Data at runtime.|

##### **Call Result Feature**

|Detail|Value|
|:---|:---|
|Feature ID|Debug.CallResult|
|Name|Call Result Feature|
|Dev Version|V 1.0|
|Public Version|V ---|
|Beta Version|V ---|
|Steam Version|V ---|
|Desc|This feature is used to allow calls to be attempted and allows for knowing if the call was successful along with the returned value as well a error if any were encountered.|

##### **Debug Logging Feature**

|Detail|Value|
|:---|:---|
|Feature ID|Debug.Logging|
|Name|Debug Logging Feature|
|Dev Version|V 1.0|
|Public Version|V ---|
|Beta Version|V ---|
|Steam Version|V ---|
|Desc|This feature is built ontop of the normal logging system of PZ which is used to make the log message custom to make it easier to debug mods based on Realms Lore. This feature also allows for logging for Runtime Errors using a custom format layout|

#### **Error System**

|Detail|Value|
|:---|:---|
|System ID|Frame.Errors|
|Name|Error System|
|Dev Version|V 1.0|
|Public Version|V ---|
|Beta Version|V ---|
|Steam Version|V ---|
|Desc|This system is used to define and build errors to be used for debugging mods|

**Features:**
- [**Error Defs Feature**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Mods/Prototypes/Protoframe/InvadeFrame.md#error-defs-feature)
- [**Error Data Feature**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Mods/Prototypes/Protoframe/InvadeFrame.md#error-data-feature)
- [**Registerable Error Defs Feature**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Mods/Prototypes/Protoframe/InvadeFrame.md#registerable-error-defs-feature)
- [**Error Assembly Feature**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Mods/Prototypes/Protoframe/InvadeFrame.md#error-assembly-feature)
- [**Error Def Assembly Feature**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Mods/Prototypes/Protoframe/InvadeFrame.md#error-def-assembly-feature)
- [**Inline Errors Feature**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Mods/Prototypes/Protoframe/InvadeFrame.md#inline-errors-feature)
- [**Basic Errors Feature**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Mods/Prototypes/Protoframe/InvadeFrame.md#basic-errors-feature)

##### **Error Defs Feature**

|Detail|Value|
|:---|:---|
|Feature ID|Errors.Defs|
|Name|Error Definition Feature|
|Dev Version|V 1.0|
|Public Version|V ---|
|Beta Version|V ---|
|Steam Version|V ---|
|Desc|This feature allows users to define thier own custom Error definition for use with Inline Errors Feature.|

##### **Error Data Feature**

|Detail|Value|
|:---|:---|
|Feature ID|Errors.Data|
|Name|Error Runtime Data Feature|
|Dev Version|V 1.0|
|Public Version|V ---|
|Beta Version|V ---|
|Steam Version|V ---|
|Desc|This feature allows errors to be generated at runtime with using a def as a template for the creation of the error|

##### **Registerable Error Def Feature**

|Detail|Value|
|:---|:---|
|Feature ID|Errors.RegDefs|
|Name|Error Def Register Feature|
|Dev Version|V 1.0|
|Public Version|V ---|
|Beta Version|V ---|
|Steam Version|V ---|
|Desc|This feature allows users to register their custom error definitions for use with Inline Erros Feature.|

##### **Basic Errors Feature**

|Detail|Value|
|:---|:---|
|Feature ID|Errors.Basic|
|Name|Basic Error Defitions Feature|
|Dev Version|V 1.0|
|Public Version|V ---|
|Beta Version|V ---|
|Steam Version|V ---|
|Desc|This feature provides some basic errors that cover some of the most basic 'Errors', from Nil Argument to Wrong Type|

#### **Frame System**

|Detail|Value|
|:---|:---|
|System ID|Frame.Frame|
|Name|Framework Core System|
|Dev Version|V 1.0|
|Public Version|V ---|
|Beta Version|V ---|
|Steam Version|V ---|
|Desc|This system provides some of the most basic feature for working with 'Protoframe'|

**Features:**
- [**Object Type Feature**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Mods/Prototypes/Protoframe/InvadeFrame.md#object-type-feature)
- [**System Install Feature**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Mods/Prototypes/Protoframe/InvadeFrame.md#system-install-feature)

##### **Object Type Feature**

|Detail|Value|
|:---|:---|
|Feature ID|Frame.Type|
|Name|Lua Object Types Feature|
|Dev Version|V 1.0|
|Public Version|V ---|
|Beta Version|V ---|
|Steam Version|V ---|
|Desc|This feature provides the basic logic for knowing some basic infomation about Lua code objects and the "Object" type.|

##### **System Install Feature**

|Detail|Value|
|:---|:---|
|Feature ID|Frame.SysInstall|
|Name|System Install Feature|
|Dev Version|V 1.0|
|Public Version|V ---|
|Beta Version|V ---|
|Steam Version|V ---|
|Desc|This feature is used to allow users to run installer functions which are used to know if there are any issues installing this feature will pass a Call Result if the install was successful, and if not the error that caused it to fail.|

#### **Game Link System**

|Detail|Value|
|:---|:---|
|System ID|Frame.GameLink|
|Name|Zomboid Link System|
|Dev Version|V 1.0|
|Public Version|V ---|
|Beta Version|V ---|
|Steam Version|V ---|
|Desc|This system is used to link to Zomboid while wrapping around to maintain a pure . system|

**Features:**
- [**Player Link Feature**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Mods/Prototypes/Protoframe/InvadeFrame.md#player-link-feature)
- [**Character Link Feature**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Mods/Prototypes/Protoframe/InvadeFrame.md#character-link-feature)
- [**Inventory Link Feature**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Mods/Prototypes/Protoframe/InvadeFrame.md#inventory-link-feature)
- [**Items Link Feature**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Mods/Prototypes/Protoframe/InvadeFrame.md#items-link-feature)
- [**World Link Feature**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Mods/Prototypes/Protoframe/InvadeFrame.md#world-link-feature)
- [**World Cell Link Feature**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Mods/Prototypes/Protoframe/InvadeFrame.md#world-cell-link-feature)
- [**World Square Link Feature**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Mods/Prototypes/Protoframe/InvadeFrame.md#world-square-link-feature)

##### **Player Link Feature**

|Detail|Value|
|:---|:---|
|Feature ID|GameLink.Player|
|Name|Player Linking Feature|
|Dev Version|V 1.0|
|Public Version|V ---|
|Beta Version|V ---|
|Steam Version|V ---|
|Desc|This feature is used for working with Project Zomboid Players.|

##### **Character Link Feature**

|Detail|Value|
|:---|:---|
|Feature ID|GameLink.Character|
|Name|Character Linking Feature|
|Dev Version|V 1.0|
|Public Version|V ---|
|Beta Version|V ---|
|Steam Version|V ---|
|Desc|This feature is provides logic which makes the process of dealing with PZ Game Characters.|

##### **Inventory Link Feature**

|Detail|Value|
|:---|:---|
|Feature ID|GameLink.Inventory|
|Name|Inventory Link Feature|
|Dev Version|V 1.0|
|Public Version|V ---|
|Beta Version|V ---|
|Steam Version|V ---|
|Desc|This feature provides logic which is used to make working with PZ Inventories much eaiser to deal with.|

##### **Items Link Feature**

|Detail|Value|
|:---|:---|
|Feature ID|{}|
|Name|{}|
|Dev Version|V 1.0|
|Public Version|V ---|
|Beta Version|V ---|
|Steam Version|V ---|
|Desc|This feature provides logic that makes working with PZ game Items much easier to work with.|

##### **World Link Feature**

|Detail|Value|
|:---|:---|
|Feature ID|GameLink.World|
|Name|World Link Feature|
|Dev Version|V 1.0|
|Public Version|V ---|
|Beta Version|V ---|
|Steam Version|V ---|
|Desc|This feature provides logic that makes working with the PZ game world much easier to work with.|

##### **World Cell Link Feature**

|Detail|Value|
|:---|:---|
|Feature ID|GameLink.WorldCell|
|Name|World Cell Link Feature|
|Dev Version|V 1.0|
|Public Version|V ---|
|Beta Version|V ---|
|Steam Version|V ---|
|Desc|This feature provides logic that makes working with PZ world Cell's much easier to work with.|

##### **World Square Link Feature**

|Detail|Value|
|:---|:---|
|Feature ID|GameLink.WorldSquare|
|Name|World Square Link Feature|
|Dev Version|V 1.0|
|Public Version|V ---|
|Beta Version|V ---|
|Steam Version|V ---|
|Desc|This feature provides logic simplifing the job of working with PZ World Squares|