# Realms Invasion 'Info Center': **Libraries - Fueled.Core - Changes and Tasks**

Welcome to the **Libraries - Fueled.Core - Changes and Tasks** page of the Realms Invasion Info Center. 
This 'Info Center' is the public knowledge database for the Realms Invasion Mods for Project Zomboid

A few things to note, 
Realms Invasion is a new and WIP project which means that things are subject to change alot between releases so please I ask you keep coming back from time to time

This page covers the current tasks planned for fueled core and the changes log.

## **Index**
- [**Home**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/README.md)
- [**About the Repo**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/README.md#about-the-repo)
- [**About Project 'Realms'**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/AboutProjectRealms.md)
- [**What is Realms Invasion**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/README.md#what-is-realms-invasion)
    - [**What is Realms of Reality**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/AboutRealmsOfReality.md)
    - [**Realms Invasion Features**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/README.md#realms-invasion-features)
- [**Index**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Libraries/Fueled%20Core/FueledCore_Todo.md#index)
    - [**Todo**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Libraries/Fueled%20Core/FueledCore_Todo.md#tasks)
    - [**Changes**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Libraries/Fueled%20Core/FueledCore_Todo.md#changes)
        - [**V: 1.0.0.0**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Libraries/Fueled%20Core/FueledCore_Todo.md#1.0.0.0)

### **Tasks**

- Impliment basics of ability to change settings with a UI
- Update user system with User ID Check feature
- Update pathing system with virtual folder feature
- Add basic design feature attributes

### **Changes**

#### **1.0.0.0**

- Inital Release
- Moved Systems from Fueled.Core.LuaScript to Fueled.Core
- Updated Logging System to process unhandled messages on initalization
- Updated Settings system to fix bug where it would use wrong folder path
- Updated to a systems collection system to allow more flexability
- Added new Fueled App System
- Updated whole library to use new Fueled App and Systems collection systems
- Updated 'Runtime Settings System' with a feature to solve issue with newtonsoft.json