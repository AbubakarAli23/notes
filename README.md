# **DATABASE SYSTEMS.**

## **DATABASE SYSTEM CONCEPTS**

Shared integrated computer structure that stores a collection of end-user data and meta-data.

### DBMS

- a collection of programs that manages the database structure and controls access

### ABSTRACTION AND DATA INTEGRATION

#### ABSTRACTION

- it is a simplification mechanism that hides unnecessary details and shows only what is relevant to the user or the application.
- there are three levels of transaction which corresponds to the three views. ![diagram for views](https://www.relationaldbdesign.com/relational-database-design/module3/images/three_schema_architecture.jpg)
  - External view
    - it is the highest level, it is what users or applications see.
    - each user can have a different view.
  - Conceptual view
    - it represents the entire database
    - it contains all entities, attributes and relationships.
    - it is independent of the physical storage
    - it managed by the VBA
  - internal level(physical view)
    - it is the lowest level.
    - it describes how data is actually stored.
    - it includes file structures, record formats, access methods and storage locations.

##### MAPPING BETWEEN VIEWS

- two mappings are provided by the DBMS
  - External conceptual mapping
    - it converts the user views into Conceptual records.
  - Conceptual/ internal mapping.
    - it converts conceptual records into physical storage formats.
- these mappings provide data independence
  - data independence is the immunity of an application program in data storage or structure.
  - there are categories of data independence
    - logical data independence
      - changes at the conceptual level does affect external views.
      - the external views remain unchanged.
      - it helps to protect application programs.
    - physical data independence.
      - changes at the internal level do not affect conceptual or external levels.
      - for example opening file organisation or moving data to new storage devices.

##### components of a database management SYSTEM

- the Data definition language(DDL)
  - it is used to define and modify the database structure.
  - example is CREATE, ALTER.
- The data manipulation language(DML)
  - it is used to retrieve and manipulate data.
  - example is INSERT, DELETE, UPDATE,
- Data control language(DCL)
  - it controls security and access.
  - example is REVOKE
- Form generator
  - it creates screen-based forms
  - it is used for data input or output
- menu generator
  - it creates menus for user interaction
- report generator
  - it creates formatted reports which has headers and footers.
- business graphics
  - it is used to produce charts and graphs.
- the data dictionary
  - it stores meta-data which is data about data.

##### data models

- A model
  - it is an abstraction of a real world or event.
- data models are simple representation of real world complex data structures
- Data modelling
  - is the progressive model of creating a specific data model for a determined problem domain.

###### importance of data models

- they are a communication tools.
- they give an overall views of the database.
- they organise data for various users.
- they are an abstraction for the creation of a good database

###### basic building blocks of a data model

  1. entity
      - it is a unique and distinct object that is used to collect and store data.
  2. attributes  
     - it is a characteristic of an entity
  3. relationship
     - it describes association among entities.
  4. constraint
      - this is a set of rules to ensure data integrity.

## **HIERARCHICAL RELATIONSHIP MODEL**

They manage large amounts of data for complex projects
it represented by an upside down tree which contains segments(nodes)
the segments are equivalents of a file system's record
it is depicted by a set of one to many relationships
![diagram for hierarchy](https://media.geeksforgeeks.org/wp-content/uploads/20200727111632/hierarchical.png)
### advantages
1. it promotes data sharing
2. the parent child relationship promotes conceptual simplicity and data integrity
3. it is efficient with one to many types of relationships 
### disadvantages
1. it requires knowledge of physical data storage characteristics 
2. navigation system requires knowledge on hierarchical path 
3. changes in structure requires changes in all application programs

## **NETWORK DATA MODEL**
![diagram for network model](https://upload.wikimedia.org/wikipedia/commons/thumb/3/3e/Network_Model.svg/1280px-Network_Model.svg.png)
they represent complex data relationships
they impose database standards
they depict both one to many and many to many relationships
### advantages
1. it handles more types of relationships 
2. data access is flexible
3. it conforms to standards
### disadvantages
1. system complexity limits efficiency
2. navigational system yields to complex implementation application development and management

## **ENTITY RELATIONSHIP MODEL**
it represents the real world and the relationship between those entities
an entity is a real world object that is distinguishable from other objects 
these entities can be concrete or abstract
examples of concrete entities are books, cars etc 
examples of abstract entities are loans, holiday etc

### basic components of the ER model
it has three main components
  1. entity set
      - it is a group of similar entities
      - for example all bank customers form the customer entity set
  2. relationship set
      - a relationship is a association between two or more entities
      - a relationship set is a collection of similar entities
  3. attributes
