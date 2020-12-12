# Realms Invasion 'Info Center': **Tutorials - Libraries - Fueled.Core - Fueled CS Pattern**

Welcome to the **Tutorials - Libraries - Fueled.Core - Fueled CS Pattern** page of the Realms Invasion Info Center. 
This 'Info Center' is the public knowledge database for the Realms Invasion Mods for Project Zomboid

A few things to note, 
Realms Invasion is a new and WIP project which means that things are subject to change alot between releases so please I ask you keep coming back from time to time

This page covers the custom design pattern used by all my projects and works.

## **Index**
- [**Home**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/README.md)
- [**About the Repo**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/README.md#about-the-repo)
- [**About Project 'Realms'**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/AboutProjectRealms.md)
- [**What is Realms Invasion**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/README.md#what-is-realms-invasion)
    - [**What is Realms of Reality**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/AboutRealmsOfReality.md)
    - [**Realms Invasion Features**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/README.md#realms-invasion-features)
- [**Tutorials Home**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Tutorials/TutorialsHome.md)
- [**Index**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Tutorials/FueledCSDesignPattern.md#index)
    - [**About**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Tutorials/FueledCSDesignPattern.md#about)
    - [**Required Apps**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Tutorials/FueledCSDesignPattern.md#required-apps)
    - [**Required knowledge**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Tutorials/FueledCSDesignPattern.md#required-knowledge)
    - [**Sections**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Tutorials/FueledCSDesignPattern.md#sections)
        - [**Identification Objects**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Tutorials/FueledCSDesignPattern.md#identification-objects)
            - [**ID Layout**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Tutorials/FueledCSDesignPattern.md#id-layout)
            - [**ID Pieces**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Tutorials/FueledCSDesignPattern.md#id-pieces)
            - [**Project ID Objects**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Tutorials/FueledCSDesignPattern.md#project-id-objects)
                - [**Optinal Project IDs**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Tutorials/FueledCSDesignPattern.md#optinal-project-ids)
                    - [**Log Package**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Tutorials/FueledCSDesignPattern.md#log-package)
                    - [**Setting Package**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Tutorials/FueledCSDesignPattern.md#setting-package)
            - [**System ID Objects**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Tutorials/FueledCSDesignPattern.md#system-id-objects)
            - [**Feature IDs**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Tutorials/FueledCSDesignPattern.md#feature-ids)
        - [**Library Tracking**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Tutorials/FueledCSDesignPattern.md#library-tracking)
        - [**Systems Tracking**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Tutorials/FueledCSDesignPattern.md#systems-tracking)
        - [**Feature Tracking**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Tutorials/FueledCSDesignPattern.md#feature-tracking)
        - [**Data Orgonization**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Tutorials/FueledCSDesignPattern.md#data-orgonization)
            - [**Construct**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Tutorials/FueledCSDesignPattern.md#construct)
            - [**Convert**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Tutorials/FueledCSDesignPattern.md#convert)
            - [**Debug**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Tutorials/FueledCSDesignPattern.md#debug)
            - [**Equality**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Tutorials/FueledCSDesignPattern.md#equality)
            - [**Math**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Tutorials/FueledCSDesignPattern.md#math)
    - [**Related Tutorials**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Tutorials/FueledCSDesignPattern.md#related-tutorials)

### **About**

This tutorial will cover how to use and how to impliment my custom design pattern for use with designing your own apps and systems.

### **Required Apps**

The following apps are required to complete this tutorial.

|**AppName**|**Req Type**|**Desc**|
|:---:|:---:|:---|
|Visual Studio 2019|Required|This is the basic IDE which Fueled Core is designed and built with|

There are plans to allow the system to be developed using Monodevelop but this is a future plan and may take some time to impliment.

### **Required knowledge**

The following knowledge or the will to learn are required before attempting

|**Knowledge**|**Level**|**Desc**|
|:---:|:---:|:---|
|C# (CSharp)|Basic|The ability to code using the cSharp language is required|
|C# - .Net Framework 4.7.2|Basic|Neet to know the basics of using .Net Framework Version 4.7.2|
|C# - Attributes|Basic|Need to know the basics of applying attributes to c# objects|
|C# - Constants|Basic|Need to know how to create constant fields|
|C# - Strings|Basic|The basic knowledge of string values in c#|


### **Sections**

The following sections cover different aspects of applying CS pattern to your libraries and applications.

#### **Identification Objects**

Fueled Core is designed around keeping the object data down by using "ID" objects. These object(s) are serve a few purpases, among these are, Making it easier to change ID's without spending forever and a half changing and finding all strings, central Object for use with the Fueled Core's Design system.

##### **ID Layout**

The ID's for objects are developed using a very spesific format.
- Project ID = BasePiece + Project Piece
- System ID = Project Piece + System Piece;
- Feature ID = System Piece + Feature ID

##### **ID Pieces**

ID pieces are small pieces of ID's that are combined with another piece to form the complete ID. There are two different types of ID Pieces, Project and System ID pieces. For more infomation on why please check [ID Layout](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Tutorials/FueledCSDesignPattern.md#id-layout)

##### **Project ID Object**

Project ID Object are for identifing the main ID's for all things relating the the general project. Can also include system ID's although this is only recomended with small projects. With larger projects it is recomended to use A small Project ID Object then Seperate ID Objects for each system to keep things from overlapping.

To design a core Object you add a new class, We recomend a short name to identify the project plus ID at the end. After that you will want to include the Project Design Namespace Like so.

```cs
using Fueled.Core.Design;
```

Next I recomend sealing your class because our ID objects are not meant to be able to subclassed. This looks like
```cs
namespace Fueled.Core {
    public sealed class FueledID {

    }
}
```

Next we will add a region chunk with the title of 'Identify: Project' which looks like

```cs
namespace Fueled.Core {
    public sealed class FueledID {
        #region Identify: Project

        #endregion
    }
}
```

Next you will want to add a internal constant string (although for small projects you can keep it private) that has the name of _projectIDPiece and a public constant string with name of ProjectID. this looks like so.


```cs
namespace Fueled.Core {
    public sealed class FueledID {
        #region Identify: Project
        internal const string _projectIDPiece = "Fueled";

        public const string ProjectID = _projectIDPiece;
        #endregion
    }
}
```

Now that we have our basic ID's in place we can start to add the given attributes. There are three attributes that apply to ID's. They are ProjectIDObject, ProjectID, ProjectIDPiece. You can also use more then one Project ID Piece, although only the one that is used with System IDs gets marked with ProjectIDPiece, the other ones use ProjectIDBase. To Apply these attributes it looks like so.

```cs
namespace Fueled.Core {
    [ProjectIDObject(FueledID.ProjectID)]
    public sealed class FueledID {
        #region Identify: Project
        [ProjectIDPiece(FueledID.ProjectID)]
        internal const string _projectIDPiece ="Core"
        
        [ProjectIDBase(FueledID.ProjectID)]
        private const string _projectBase = "Fueled";

        [ProjectID(FueledID.ProjectID)]
        public const string ProjectID = _projectBase + "." + _projectIDPiece;
        #endregion
    }
}
```

Tada, now you are done with creating your first Project ID Object.

###### **Optinal Project ID's**

There are a few custom Optinal IDs that can be added to our Project ID Objects which are used to make working with some extra features. These are:
- [**Log Package**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Tutorials/FueledCSDesignPattern.md#log-package): Used to identify the logging package used by the given project.
- [**Setting Package**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Tutorials/FueledCSDesignPattern.md#setting-package): Used to identify the custom settings package used by the project.

###### **Log Package**

Fueled Core design system has built in features which allows you to designate the project's Log Package ID using the same attribute system. To do this you first add the following Using.

```cs
using Fueled.Core.Design.Logging;
```

Next you will go to your project ID Object and add a the following region block then add a public constant with the ID you want to use for your Project

```cs
#region Identity: Logging
public const string LogPackage = FueledID.ProjectID;
#endregion
```

Next you will add the given Attribute to the ID.

```cs
#region Identity: Logging
[LogPackageID(Fueled.ProjectID)]
public const string LogPackage = FueledID.ProjectID;
#endregion
```

You are now done adding your logging package for your project.

###### **Setting Package**

- **Not yet implimented**

##### **System ID Objects**

For System ID objects much of the same applies as a project ID object, although you will be adding a region block called Identify: System, and then you will put all, System ID Piece, System ID and all the different feature ID's in that given region block. Which will look like so

```cs
namespace Fueled.Core.Apps {
    public sealed class FueledAppID {
        #region Identify: System
        private const string _systemIDPiece = "FueledApp";

        public const string SystemID = FueledID._projectIDPiece + "." + _systemIDPiece;

		public const string LogicHostFeature = _appPiece + ".LogicHost";
		public const string InitalizeFeature = _appPiece + ".Initalize";
		public const string FolderFeature = _appPiece + ".Folder";
		public const string InstanceFeature = _appPiece + ".Instance";
		public const string SingleInstanceFeature = _appPiece + ".SingleInstance";
        
        #endregion
    }
}
```

Next is to add the following using statements to your System ID Class.

```cs
using Fueled.Core.Design.Systems;
```

Next we will be applying the system equivalant of the Project ID attributes, but this time making sure that to use the system version. This looks like 

```cs
namespace Fueled.Core.Apps {
	[SystemIDObject( FueledID.ProjectID, FueledAppID.AppSystem )]
	public sealed class FueledAppID {
		#region Identify: System
		[SystemIDPiece( FueledID.ProjectID, FueledAppID.AppSystem )]
		internal const string _systemIDPiece = "FueledApp";

		[SystemID( FueledID.ProjectID, FueledAppID.AppSystem )]
		public const string AppSystem = FueledID._projectIDPiece + "." + _systemIDPiece;
		#endregion
	}
}
```

As you can See there are System equivalant attributes for ProjectIDObject, ProjectIDPiece and ProjectID. 

##### **Feature IDs**

On to the last part that is contained within our System ID Object. This is the features of a given system. First thing to do if you havent already is add the features namespace

```cs
using Fueled.Core.Design.Systems.Features;
```

This will allow us to add attributes to our features to get things where they can be identified by the system. Next is to add the features to your system Object.

```cs
namespace Fueled.Core.Apps {
    [SystemIDObject( FueledID.ProjectID, FueledAppID.AppSystem )]
    public sealed class FueledAppID {
        #region Identify: System
       [SystemIDPiece( FueledID.ProjectID, FueledAppID.AppSystem )]
		internal const string _systemIDPiece = "FueledApp";

		[SystemID( FueledID.ProjectID, FueledAppID.AppSystem )]
		public const string AppSystem = FueledID._projectIDPiece + "." + _systemIDPiece;

		public const string LogicHostFeature = _appPiece + ".LogicHost";
		public const string InitalizeFeature = _appPiece + ".Initalize";
		public const string FolderFeature = _appPiece + ".Folder";
		public const string InstanceFeature = _appPiece + ".Instance";
		public const string SingleInstanceFeature = _appPiece + ".SingleInstance";
        
        #endregion
    }
}
```

Next we will be applying the Attributes to our feature ids which will end up looking like so.

```cs
namespace Fueled.Core.Apps {
	[SystemIDObject( FueledID.ProjectID, FueledAppID.AppSystem )]
	public sealed class FueledAppID {
		#region Identify: System
		[SystemIDPiece( FueledID.ProjectID, FueledAppID.AppSystem )]
		internal const string _systemIDPiece = "FueledApp";

		[SystemID( FueledID.ProjectID, FueledAppID.AppSystem )]
		public const string AppSystem = FueledID._projectIDPiece + "." + _systemIDPiece;

		[FeatureID(FueledID.ProjectID, FueledAppID.AppSystem,FueledAppID.LogicHostFeature)]
		public const string LogicHostFeature = _systemIDPiece + ".LogicHost";
		[FeatureID( FueledID.ProjectID, FueledAppID.AppSystem, FueledAppID.InitalizeFeature )]
		public const string InitalizeFeature = _systemIDPiece + ".Initalize";
		[FeatureID( FueledID.ProjectID, FueledAppID.AppSystem, FueledAppID.FolderFeature )]
		public const string FolderFeature = _systemIDPiece + ".Folder";
		[FeatureID( FueledID.ProjectID, FueledAppID.AppSystem, FueledAppID.InstanceFeature )]
		public const string InstanceFeature = _systemIDPiece + ".Instance";
		[FeatureID( FueledID.ProjectID, FueledAppID.AppSystem, FueledAppID.SingleInstanceFeature )]
		public const string SingleInstanceFeature = _systemIDPiece + ".SingleInstance";
		#endregion
	}
}
```

You have now successfully applied all the given attributes that are used to Identify your Project, System and the system's features. These will be used by other attributes to allow the system to read the given Systems and features inside a given project.

#### **Library Tracking**

Fueled Core is designed to allow us to mark our libraries and applications as belonging to a given project. First thing we need to do is find our library/app's AssemblyInfo.cs file. Next we open this file using the IDE. at the top you need to add two using statements, the first is to the namespace holding the design attributes, the second is the namespace of our project id object. For Fueled Core this looks like.

```cs
using Fueled.Core.Design;
using Fueled.Core;
```

Next we will add the following to the bottom of the page.

```cs
[assembly: ProjectLibrary(FueledID.ProjectID)]
```

Replace the "FueledID.ProjectID" with the your libraries "ProjectIDObject" class and your Project ID. Now you have applied it so that your library(ies) will now be analized by Realms Invasion 'Projects' to allow for extra new features.

#### **System Tracking**

#### **Feature Tracking**

#### **Data Orgonization**

##### **Construct**

##### **Convert**

##### **Debug**

##### **Equality**

##### **Math**





### **Related Tutorials**

- **Fueled.Core**
    - [**Apps System**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Tutorials/Libraries/FueledCore/Apps/FueledAppsTutorial.md)
    - [**Design System**](https://github.com/FueledByOCHD/Realms-Invasion-Info-Center/blob/develop/Tutorials/Libraries/FueledCore/Systems/DesignSystem.md)