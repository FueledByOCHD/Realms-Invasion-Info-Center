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