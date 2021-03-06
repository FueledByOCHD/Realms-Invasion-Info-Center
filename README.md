# Realms Invasion 'Info Center': **Home**

Welcome to the **home page** of the Realms Invasion Info Center. 
This 'Info Center' is the public knowledge database for the Realms Invasion Mods for Project Zomboid

A few things to note, 
Realms Invasion is a new and WIP project which means that things are subject to a lot of changes between releases so make sure to occasionally return for the most recent and up-to-date version release.

## **Index**
- [**Home**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/README.md)
- [**About the Repo**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/README.md#about-the-repo)
- [**About Project 'Realms'**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/AboutProjectRealms.md)
- [**What is Realms Invasion**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/README.md#what-is-realms-invasion)
	- [**Realms Invasion Status**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/README.md#realms-invasion-status)
	- [**What is Realms of Reality**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/AboutRealmsOfReality.md)
    - [**Realms Invasion Features**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/README.md#realms-invasion-features)
- [**What is Invade 'Prototypes'**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/README.md#what-is-invade-prototypes)
	- [**Invade 'Prototypes' Status**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/README.md#invade-prototypes-status)  
- [**What are Types**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/README.md#what-are-types)  
- [**Index**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/README.md#index)
    - **General**
        - [**Tutorials Home**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Tutorials/TutorialsHome.md)
        - [**Want To Donate?**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/DonateToRI.md)
        - [**About Me**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/AboutMe.md)
        - [**Follow On Discord**](https://discord.gg/8P2kvwm)
        - [**Changes and Todo**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Changes/RI_Todos.md)
        - [**Credits and Shoutouts**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Credits/RI_FullCredits.md)
    - **Mods**
		- **Invade Prototypes**
			- [**Prototype**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Mods/Prototypes/Prototype/InvadeProto.md)
			- [**Protoframe**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Mods/Prototypes/Protoframe/InvadeFrame.md)
    - **Tools**
        - [**Projects**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Tools/Projects/RI_Projects.md)
    - **Libraries**
        - [**Fueled.Core**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Libraries/Fueled%20Core/FueledCore.md)



## **About the Repo**

This Repo is used to help with getting familuar and a knowledge data base for all my works.

## **What are Types**

"Types" are a name for the "Type" of object that your working with. Lua includes basic types and allows for types, but the issue is that the Lua system makes you remember the following

```lua
obj:CallFunc()
-- Or
obj.CallFunc()
```

If your trying to call data. With the Hard Typed version "Realms Invasion Modset" there will be one
to remember which is the normal . call. And will eventuall allow for different "Security" levels on object fields, properties and function (Logic) calls.

**Hard Type** refers to a full access level type system which is mimics C# in Lua.
**Simi-Type** refers to a value based type system which "Loosely" enforces data types.
**Basic-Type** refers to systems like that of lua and JS which have a few "Basic" data types.

**Security Levels**

|Name|Access Info|
|:---:|:---|
|Public|This level is used to refer to calls made outside the object its self|
|Private|This level is used to refer to calls made inside the exact "Type"|
|Protected|This level is used to refer to calls made inside the exact "Type" and "Subtypes"|

## **What is Invade Prototypes**

Invade 'Prototypes' is the reference for Invade 'Prototype' and Invade 'Protoframe' which are the [simi-typed](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/README.md#what-are-types) version of the eventual [Hard Typed](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/README.md#what-are-types) Realms Invasion Modset. 

### **Invade Prototypes Status**

Invade 'Prototype' and 'Protoframe' are currently in active development to be used as the base for the Realms Invasion Modset. These two projects are the "Prototype" of the Realms Invasion Mods.

## **What is Realms Invasion**

Realms Invasion is a collection of mods with the long term goal of overhauling Project Zomboid with more of a Sci-Fi Fantasy theme based off [**Realms of Reality Lore**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/AboutRealmsOfReality.md). The end goal is to eventually transform this into a game of its own.

### **Realms Invasion Status**

Realms Invasion Mods are on hole while I focus my attention on [**Invade 'Prototypes'**]() which will be the [simi-typed](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/README.md#what-are-types) version of the complete Invasion Modset, as well as while I develop out [**Realms Invasion 'Projects'**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Tools/Projects/RI_Projects.md) out to allow me to more effectivly develop and maintain all my projects.
