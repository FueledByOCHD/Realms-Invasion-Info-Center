# **Realms Invasion: Framework Home**

Realms Invasion: Framework is a core framework for working with PZ and provides all other Realms Invasion Mods with systems and features for interaction with PZ as well as some core features for interaction with the Framework itself as simple and as smooth as possible.

## **Contents**

- [**Required Knowledge**](https://github.com/Ancient-Majik-Tech/PZ-Realms-Info-Center/blob/master/Mods/Framework/RI_Frame.md#required-knowledge)
- [**Indepth About**](https://github.com/Ancient-Majik-Tech/PZ-Realms-Info-Center/blob/master/Mods/Framework/RI_Frame.md#indepth-about)
- [**Systems**](https://github.com/Ancient-Majik-Tech/PZ-Realms-Info-Center/blob/master/Mods/Framework/RI_Frame.md#systems)
    - [**Basic Logic**](https://github.com/Ancient-Majik-Tech/PZ-Realms-Info-Center/blob/master/Mods/Framework/RI_Frame.md#basic-logic)
    - [**Namespace**](https://github.com/Ancient-Majik-Tech/PZ-Realms-Info-Center/blob/master/Mods/Framework/RI_Frame.md#namespace)
    - [**Types**](https://github.com/Ancient-Majik-Tech/PZ-Realms-Info-Center/blob/master/Mods/Framework/RI_Frame.md#types)
    - [**Components**](https://github.com/Ancient-Majik-Tech/PZ-Realms-Info-Center/blob/master/Mods/Framework/RI_Frame.md#components)
    - [**Mods**](https://github.com/Ancient-Majik-Tech/PZ-Realms-Info-Center/blob/master/Mods/Framework/RI_Frame.md#mods)
    - [**Core**](https://github.com/Ancient-Majik-Tech/PZ-Realms-Info-Center/blob/master/Mods/Framework/RI_Frame.md#core)
- [**Tutorials**](https://github.com/Ancient-Majik-Tech/PZ-Realms-Info-Center/blob/master/Mods/Framework/RI_Frame.md#tutorials)

### **Required Knowledge**

**All Users**

- How to Install PZ Mods [Steam]
- [How to Install PZ Mods <NonSteam>](https://pzwiki.net/wiki/Installing_mods)
- [Realms Invasion: Framework mod]()

**Modders**

If this is your first time here please we ask that you get familuar with the Realms Invasion project as well as the framework before trying to use Realms Invasion: Framework, We recomend this because working with Realms Invasion Framework and the Realms Invasion mods function very differently then you would think

### **Indepth About**

Realms Invasion: Framework (RI_Frame) is the core mod to give all Realms Invasion Mods features that other modders can benifit from. RI_Frame is a active work in progress which means that much of the mod is currently in a rough and unpolished state, This means for users and modders alike each version of RI_Frame might break active mods and should be used with caution. 

### **Systems**

A rundown of the current systems inside of the RI_Frame which available for use with your own custom mods.

#### **Namespace**

Realms Invasion is maintained by Fueled By OCHD, who comes from a long background in c#. Part of the RI_Frame's goal is to provide some features which are used to allow all RI Mods to function more like c#. One of these features is Namespaces, to be more spesific, RI Mods are designed to run and function from a single namespace object. 

#### **Main Logic**

The Realms Namespace Object provides some useful features from the base node of the object

- *Debug Logging*: This feature set is used to log different types of actions to the console log to allow for easier debugging of mods.

- *Type Assembly*: This feature set is used to allow mods to register now object "Types" in a c#-Lua hybrid style.

- *Object Assembly*: This feature set is used to allow mods to assembly c# style objects which have thier own "Private" access to fields/functions. Along with a [in the works] Event System along with a c# like [Base] feature.

- *Component Assembly*: This feature set is used to add new logic as well as allow mods to override logic in a "Patch" style manner.

#### **Types**

Realms Framework has a few "Internal" use types, along with some nice custom types which are meant to make modders lives easier.

- *RList*: RI_Frame provides a c# like list of object which as called the RList. This provides functionality for knowing if object is already added (which should be Value not reference based). along with adding and removing a value. Along with a Ordering feature.

- *RDict*: RI_Frame provides a c# like Dictinary of objects which allows you to register a value to a key.

#### **Components**

Components are chuncks of logic and data which are applied on top of existing logic.

RI_Frame provides functionality to apply the new logic as new logic or an override to existing logic

#### **Mods**

Mods are Collections of Components, Types and Data which help provide functionality to Realms Invasion and(or) Project Zomboid.

#### **Core**

RI_Frame provides components which are used to allow mods that use the framework to have a common place to work with things to make peoples lives much easier to work with.

### **Tutorials**
- **Realms**
    - [Basic Logging]()
    - [Realms Object Basics]()
    - [Register New Type]()
    - [Create New Objects]()
    - [Object Events]()
    - [Working with "RLua"]()
    - [Debugging Basics]()
    - [Math]()
    - [Tables]()
    - [Missing Logic]()
    - [Data Files]()
- **Realms.Core**
    - [Testing]()
    - [Items]()
    - [Player]()
    - [Recipes]()
- **Realms.Objects**
    - **Realms.Objects.Collect**
        - [Realms.Objects.Collect.RList]()
        - [Realms.Objects.Collect.RDict]()
    

    