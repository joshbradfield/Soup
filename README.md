Soup
====

This project is a CONCEPT. NOTHING has been implemented.

**Table Of Contents**  
1. [Rough Explanation](#1)  
2. [Major Components](#2)  
3. [Things To Add](#3)  

<a name='1' \>
1. Rough Explanation
--------------------

An "Associative Data Structure" (Pseudo File System), that allows data to be searched both hierarchically as well as associatively. Data sits in a **Soup** as there is no *"Top of Tree"*.

Any "Relation" or link between pieces of data in the system has very little meaning on its own. It is up to the user to interpret the relationships as something meaningful.

Ideally this would be done using a model that explains how two pieces of data interact. A view would would then display this information in a useful fashion.

To simplify the process of identifying information, all data must be typed. Soup uses an Object Oriented approach to help classify "unknown" data. (Specifically a Data Type may implement several Interfaces(which can in inherit other interfaces))

Soup is about functionality not implementation.

<a name='2' \>
2. Major Components
-------------------
The Soup system consists of several key elements:

- [Data Soup](#DataSoup)
- [Possessive (Hierachical) Links](#PossessiveLinks)
- [Associative Links](#AssociativeLinks)
- [Hashtags](#TagLinks) 
- [List of Data Types](#DataTypes)
- [List of Interfaces](#Interfaces)
- [Views](#Views)

<a name="DataSoup" />
### Data Soup ###

Data exists as "Blobs" with very little meta data attached, as such the data is natively unorganised, *floating in a soup*.

Data natively has the following meta attached to it:

- ID (Unique)
- Human Readable Name
- Type

Any extra metadata has to be "attached" via a link.

<a name="PossessiveLinks" />
### Possessive Links ###

Set of Links joining Data in the Soup, providing one method of Hierachical organisation. Links are Parent to Child (And vice versa). A child can have multiple parents.

The type of relationship between parent and child is defined by the data type. This extra information is stored on the link.

<a name="AssociatveLinks" />
### Associative Links ###
Set of Links joining Data in the soup by association. Think "Uses" and "Used by". 

This type of Link is defined by the way two data types interact. This data is stored on the Link.

<a name="TagLinks" />
### Hashtags ###
Data can be tagged with "Free Format" ideas. (Like hashtags)

This type of link has no extra data.

<a name="DataTypes" />
### List of Data Types ###
Because Possessive and Associative links are defined by the **types** of data, the system has to know how to process them. 

Data types have the following meta data
- ID *Database Specific*
- Global Identifier *The same for all systems* (To tell the model what this data type is)
- Human Readable Name
- Supported Interfaces

<a name="Interfaces" />
### List of Interfaces ###
Interfaces help describe how the data can be interpreted.

Interfaces have the following data:
- ID *Database Specific*
- Global Identifier *The same for all systems* (To tell the model what this interface type is)
- Human Readable Name
- Supported Interfaces

<a name='3' \>
3. Things To Add
--------------------
- Support for versioning (Straight copies or a more complex versioning system like GIT)
  + Versioning for Data, DataTypes and Links.
  + Ability to mark an item as "Deleted"
- Hierachical Hashtags (A->B->C) (Like "folders")
  + Different from Possessive Links because its an idea of association, not determined by the data. The meaning of a possessive link is determined by the parent Data-Type.
- Synchronizing multiple systems (Sharing)
- Permission Layer.
