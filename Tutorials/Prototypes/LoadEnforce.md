# Realms Invasion 'Info Center': **Tutorials - {}**

Welcome to the **Tutorials - {}** page of the Realms Invasion Info Center. 
This 'Info Center' is the public knowledge database for the Realms Invasion Mods for Project Zomboid

A few things to note, 
Realms Invasion is a new and WIP project which means that things are subject to change alot between releases so please I ask you keep coming back from time to time

This page covers a concept I Call Load Enforcement.

## **Index**
- [**Home**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/README.md)
- [**About the Repo**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/README.md#about-the-repo)
- [**About Project 'Realms'**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/AboutProjectRealms.md)
- [**What is Realms Invasion**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/README.md#what-is-realms-invasion)
    - [**What is Realms of Reality**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/AboutRealmsOfReality.md)
    - [**Realms Invasion Features**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/README.md#realms-invasion-features)
- [**Tutorials Home**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Tutorials/TutorialsHome.md)
- [**Index**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/{}#index)
    - [**About**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/{}#about)
    - [**Required Apps**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/{}#required-apps)
    - [**Required knowledge**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/{}#required-knowledge)
    - [**Sections**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/{}#sections)

    - [**Related Tutorials**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/{}#related-tutorials)

### **About**

Load enforcement refers to the concept of makeing sure that systems and features are loaded in to the game. This is used to make sure that we dont get errors because some System and or feature is not loaded in. 

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

### **Sections**

There are two main types of Load Enforcement these are covered below

#### **Object Check**

Object check is used to refer to see if a object is exists or not. This is used for systems that do not use the [Protoframe - Frame System - System Install Feature]() to initalize thier systems. Mainly [Protoframe - Debug System](), [Protoframe - Errors System]() and [Protoframe - Frame System]().

Most other systems will use the [Load Enforcement - Value Check]().

An Example of this is the framework
```lua
-- Check to make sure Protoframe - Frame system is initalized
if not Invade or not Invade.Frame then
	require "Invade/Frame"
end
```

#### **Value Check**


### **Related Tutorials**


