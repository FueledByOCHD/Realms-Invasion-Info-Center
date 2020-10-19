# Realms Invasion 'Info Center': **Libraries - Fueled Core**

Welcome to the **Libraries - Fueled Core** page of the Realms Invasion Info Center. 
This 'Info Center' is the public knowledge database for the Realms Invasion Mods for Project Zomboid

A few things to note, 
Realms Invasion is a new and WIP project which means that things are subject to change alot between releases so please I ask you keep coming back from time to time

This page covers all the basic infomation about my custom Application Core C#(Sharp) Library. 

## **Index**
- [**Home**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/README.md)
- [**About the Repo**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/README.md#about-the-repo)
- [**About Project 'Realms'**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/AboutProjectRealms.md)
- [**What is Realms Invasion**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/README.md#what-is-realms-invasion)
    - [**What is Realms of Reality**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/AboutRealmsOfReality.md)
    - [**Realms Invasion Features**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/README.md#realms-invasion-features)
- [**Index**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Fueled%20Core/FueledCore.md#index)
    - [**What is Fueled Core**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Fueled%20Core/FueledCore.md#what-is-fueled-core)
    - [**Systems and Features**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Fueled%20Core/FueledCore.md#systems-and-features)
        - [**Design System**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Fueled%20Core/FueledCore.md#design-system)
        - [**Data System**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Fueled%20Core/FueledCore.md#data-system)
        - [**Debug Logging System**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Fueled%20Core/FueledCore.md#debug-logging-system)
        - [**Aliased File Paths System**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Fueled%20Core/FueledCore.md#aliased-file-paths-system)
        - [**Users System**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Fueled%20Core/FueledCore.md#users-system)
        - [**Runtime Settings System**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Fueled%20Core/FueledCore.md#runtime-settings-system)
    - [**Changes and Tasks**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Fueled%20Core/FueledCore_Todo.md)
    - [**Tutorials**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Fueled%20Core/FueledCore.md#tutorials)
        

### **What is Fueled Core**

Fueled Core is my custom systems which are meant to help users and myself in the process of making applications and libraries. Many of these system are ones if have used in alot of my applications and now I'm building one base Library which is the culmination of the different evolutions of these systems.

### **Systems and Features**

Fueled Core is designed around the Systems and Features. Using Fueled Core as the base library for your applicaions is based around an application is a collection of Systems which is a collection of fields and logic which are grouped together into a Feature. A feature is a group of Logic, Fields and data to perform a given Task.

#### **Design System**

Fueled Core's Design system is build with the idea of letting an other applications to read the active data given in applications built using Fueled Core. To be more percice Fueled Core is designed to allow my Realms Invasion 'Projects' application to read the current infomation in a given library to allow it to be used to better design applications and libraries by giving access to a task and changlog systems which are used to help developers with the task of making thier own works much easier.

#### **Data System**

Fueled Core's Data System is build to allow users and myself the ability to save and load c# objects to json data. 

#### **Debug Logging System**

Fueled Core's Debug Logging System is used to allow our applications and libraries to much easier to debug by giving our works a set of features which allow us to log details about the running of our features. This system is made to allow 'Projects' to be able to read these logs to allow us to easy search and visualize the issues to make problems much easier to debug.

#### **Aliased File Paths System**

Fueled Core's Aliased File Paths system is used to allow our works to have a way to make dealing with pathing while in c# much easier. It allows for creation of FilePaths and FolderPaths to allow our works to use more of a Object oriented pathing, instead of functioning like C with a bunch of static functions. It allows for creation of paths like

```cs
FilePath pathOfSave = new FilePath( savesFolder, "save.json");
```

Which gives the code a little better flow and it provides more features which should make it easier to for things like mods to be much easier to allow by simplifing the system to allow for loading from apps and event mods because paths can also be created using an alias.

```cs
FilePath pathOfSave = $"<Saves>/{Player.Name}/Save.json";
if (!pathOfSave.ParentFolder.Exists)
    pathOfSave.ParentFolder.Create();
if (pathOfSave.Exists)
    pathOfSave.Delete();
pathOfSave.SaveObj(GetSaveObject());
```

#### **Users System**

Fueled Core's Users System is designed to allow the editor to function independantly of the current user of the Operating system. That way systems that use a **Shared** account each user can do work on thier projects without requiring a long workaround.

#### **Runtime Settings System**

Fueled Core's Runtime Settings System is designed to allow our code to designate settings that control how things function. This system allows the settings to be controlled by the Active User which allows the whole system to react to when users are changed because the whole system can adjust for the active user.


### **Tutorials**

- [**Tutorials Home**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Tutorials/TutorialsHome.md)
- [**New App with Fueled Core**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Tutorials/Libraries/FueledCore/NewFueledApp.md#using-with-new-app)
- [**Update App with Fueled Core**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Tutorials/Libraries/FueledCore/FueledAppsTutorial.md#using-with-existing-app)
- [**Using Fueled Design System**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Tutorials/Libraries/FueledCore/Systems/DesignSystem.md)
    - **System Tutorials**
        - [**Aliased Pathing**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Tutorials/Libraries/FueledCore/Systems/AliasedPathing.md)
        - [**Data System**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Tutorials/Libraries/FueledCore/Systems/DataSystem.md)
        - [**Debug Logging**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Tutorials/Libraries/FueledCore/Systems/DebugLogging.md)
        - [**User System**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Tutorials/Libraries/FueledCore/Systems/UserSystem.md)
        - [**Runtime Settings**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Tutorials/Libraries/FueledCore/Systems/RuntimeSettings.md)