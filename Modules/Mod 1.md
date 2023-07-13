#About_DBMS #Advantages #Disadvantages 
## Characteristics of the database approach 
1) Self-describing nature of the database system.
2) Insulation between program and data. (Data Abstraction)
3) Support multiple views of the data.
4) Sharing of data & multiuser transaction processing.
	1) DBMS must enforce several transaction properties  [[Acid Compliancy]]
			◦ Atomicity 
			◦ Consistency
			◦ Isolation
			◦ Durability

## Types of people who use the database
[[Actors In DB]]
1) Database Administrators (DBA)
2) Database Designers
3) End Users
	1) Casual end users (Occasional Access)
	2) Naïve/ Parametric end users (Largest grp of users | Rely on Canned Transactions)
	3) Sophisticated end users (Engineers, scientists, business analysts, etc.)
	4) Standalone users
5) System Analysts & Application Programmers/Software Engineers

## Advantages of using a database
1) Controlling Redundancy
2) Restricting unauthorized access
3) Providing storage structures for efficient query processing
4) Providing backup & recovery
5) Providing multiple user interfaces
6) Representing complex relationships among data
7) Enforcing integrity constraints
8) Permitting inferencing & actions using rules
9) Sharing of data, data security, privacy, etc...

## Disadvantage of using DBMS
1) Cost of Hardware & Software
2) Cost of Data Conversion
3) Cost of Staff Training
4) Appointing Technical Staff
5) Database Damage

---
#About_Data
## Types of data
1) Structured (eg RDBMS)
	1) Fully Organized
	2) Strict format maintained
	3) Usually SQL
2) Semi-Structured (eg XML, JSON)
	1) Needs processing
	2) Flexible format
	3) Usually web
3) Unstructured (eg PDF, Markdown, Word)
	1) Just data 
	2) No real format
	3) eg Word, PDF, Text, Manga

## Data Models
#Important #Data_Models
1) High-level (or conceptual) data models
	- Provide concepts that are close to the way many users perceive data.
	- Use concepts such as entities, attributes, and relationships.
	- An entity represents a real-world object. Eg: an employee, student, teacher, etc.
	- An attribute represents some property of interest that further describes an entity. Eg: name, salary, etc.
	- A relationship among two or more entities represents an association among them. Eg: works-on, teaches.
1) Representational (or implementation) data models
	1) Relational - SQL
	2) Network - Record Ownership model basically like a graph ish
	3) Hierarchical - Tree like ownership more or less like classes and sub classes
2) Low-level (or physical) data models
	- Provide concepts that describe the details of how data is stored.
	- Meant for computer specialists, not for end users.
---
![[Images/Pasted image 20230320222236.png]]

---

## Schemas
* Schemas are the representation of the database, they are not expected to change that often.
- The data in the DB at a particular moment in time is called the database state/ snapshot
- Schema changes are often referred to evolution 
### 3 Schema Architecture for a DBMS
![[Images/Pasted image 20230712191637.png]]
[[#Data Models]] again basically
```python
Internal Schema == Low Level (Physical)
Conceptual Schema == Representational
External Schema == High Level
```
1) Internal Schema deals with how the data is physically stored in the database [[Physical Data Organization]]
2) Conceptual Schema deals with Entity and Relationships [[SQL]], [[Relational Algebra]]
3) External View deals with how the end user or people who interact with the data see [[ER Diagrams]]

### DATA INDEPENDENCE
Defined as the capacity to change the schema at one level of a DB system without having to change the schema at the next higher level.
Two types of data independence:
1) Logical data independence - Capacity to change the conceptual schema without having to change the external schema.
2) Physical data independence - Capacity to change the internal schema without having to change the conceptual/ external schema.
### Database Languages
1) Data Definition 
2) Storage Definition
3) View Definition
4) Data Manipulation
5) Data Control
6) Transaction Control
[[SQL]]
## The Database system environment 
![[Images/Pasted image 20230712195746.png]]Top part refers to the users and how they interact with the DB
The bottom part refers to the internal of a DBMS and how it stores and serves the request

## Entity Relation Ship model
High level data model
### [[ER Diagrams]]

## Entities
Each entity has attributes the different types of attributes include
1) Composite vs Atomic
2) Single valued vs Multivalued
3) Stored vs Derived
4) NULL attributes
5) Complex Composite Multivalued Attributes

### Relations
It is an association between two or more entities, each relationship has a 
- Name 
- Degree (Number of Attributes) and
- Cardinality (Number of Entities/Tuples)

### Participation Constraint
Determines the total number of entities that participate in a relation.

### Strong VS Weak Entities

### Cardinality 
It refers to the number of Entities in a given relation.
There can be classified into the following: 
1) One to One
2) One to Many
3) Many to One
4) Many to Many
