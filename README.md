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
      - they describe properties of an entity
      - for example registration number, ID number etc 
      - simple attribute
          - it is an attribute that cannot be divided 
          - for example registration number
      - composite attribute 
          - this is an attribute that can be divided into smaller parts
          - for example names
      - single value attributes
          - it has a single a value
      - multi value attributes
          - it can have multiple values
          - for example dependents
      - null attributes
          - it is where no value exists
      - calculated attributes
          - these are attributes whose value is calculated from other attributes
          - for example age and net income
#### ER diagram

##### chen notation

  1. rectangles
      - they represent entity sets
  2. ellipsis
      - they represent attributes
  3. diamonds
      - they represent relationship sets
  4. lines
      - they link attributes to entities and entity sets to relationship sets
  5. double ellipsis
      - they represent multi valued attributes
  6. dashed ellipsis
      - they represent derived attributes
  7. double lines
      - indicate total participation of an entity in relationship set

![diagram for chen notation](https://www.researchgate.net/publication/316047916/figure/fig1/AS:745519605379073@1554757133243/An-entity-relationship-diagram-of-data-quality-issues-Chens-notation.png)

##### crow's foot notation

![diagram for crow's foot](https://i.sstatic.net/ICEy2.png)
![diagram for crow's foot](https://edrawcloudpublicus.s3.amazonaws.com/work/864984/2021-12-24/1640313342/main.png)

##### Unified modelling language

![diagram for UML](https://cdn-images.visual-paradigm.com/guide/uml/uml-class-diagram-tutorial/17-class-diagram-example-order-system.png)
![diagram for UML 2](https://www.ionos.co.uk/digitalguide/fileadmin/_processed_/b/5/csm_EN-class-diagram11_d5a6119e38.webp)

## characteristics of relational table

  1. it is a two dimensional structure that is composed of rows and columns
  2. each intersection of a row and a column represents a single data value
  3. each row represents a single entity occurence within the entity set
  4. all values in a column must conform to the same data format
  5. each column represents an attribute and each column has a distinct name
  6. each column has a specific range of values that is referred to as attribute domain
  7. the order of rows and columns is immaterial to the DBMS
  8. each table must have an attribute or a combination of attributes that uniquely identifies each row

## KEY

A key consists of one or more attribute that determine other attributes
a key is used to ensure that each row in a table is uniquely identifiable
it is also used to establish relationships among tables and to ensure there is integrity of the data
a primary key is an attribute or combination of attributes that uniquely identifies any given row

## determination

it is the state in which knowing the value of one attribute makes it possible to determine the value of another
it is the basis for establishing the role of a key
it is based on the relationship among the attributes
the statement A determines indicates that if you the value of attribute A you can determine(lookup) the value of attribute B
for example knowing the registration number in the student table you can the value of the first name
[REGno -> Fname]

### functional dependency

it is where the value of one or more determines the value of one or more other attributes

| Regno | fname | lname | courseID | coursetitle |
| --------------- | --------------- | --------------- | --------------- | --------------- |
| Item1.1 | Item2.1 | Item3.1 | Item4.1 | Item5.1 |
| Item1.2 | Item2.2 | Item3.2 | Item4.2 | Item5.2 |
| Item1.3 | Item2.3 | Item3.3 | Item4.3 | Item5.3 |
| Item1.4 | Item2.4 | Item3.4 | Item4.4 | Item5.4 |

[(REGno,courseID) -> fname, lname , coursetitle]

#### full functional dependency
>
> [!TIP]
> this is where the entire collection of attributes in the determinant is necessary for relationship
>determinant - this is an attribute whose value determines another
>dependent - it is an attribute whose value is determined by another attribute

## types of relational database
1. super key
    - it is an attribute or combination of attributes that uniquely identifies each row in a table
2. candidate key 
    - these are minimal or irreducible super key
3. primary key 
    - this is a candidate key that is selected to uniquely identify all other attributes in any given row
    - it cannot contain null values 
4. foreign key 
    - it is an attribute or collection of attributes of a table must either match the primary key of a another table or be null 

## integrity rules
  1. all primary keys entries are unique and no part of the primary key may be null
  2. a foreign key may have a null entry or an entry that matches the primary key value in a table to which it is related 
  3. it is possible for an attribute not to have a corresponding value but it is impossible to have an invalid entry 
  4. it is impossible to delete a row in a table whose primary key has mandatory matching foreign key values in another table

## ways to handle values
  1. flags
      - these are special codes used to indicate the absence of some value
  2. NOT null constraint
      - placed on a column to ensure that every row has a value for that column
  3. unique constraint
      - it is a restriction placed on a column to ensure that every row has no duplicate values exists for that column

## relational Algebra 
this is a theoretical way of manipulating the table contents using relational operators
relational operators have the property of closure
closure is the use of relational Algebraic operators on existing relations to produce new relations
### types of relational set operators
  1. SELECT(Restrict)
      - it is a unary operator that yields sub-set of a table 
      - for example SELECT ALL yields all values of the table, SELECT ALL WHERE REGno= Item1.4 will yield 1 record
 2. PROJECT
      - it is a unary operator that yields a vertical sub-set of a table
      - for example PROJECT fname will yield the fname attribute values
  3. UNION 
      - it combines all rows from two tables excluding duplicate rows
      - tables should be UNION compatible for example they should the same number of columns and their corresponding columns share compatible domains
  4. INTERSECT
      - it yields only the rows that appear in both tables
      - the tables must be UNION compatible
      - 

