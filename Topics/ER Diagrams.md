## The model works by defining the relation between data objects. 

### Entity is a real world object. e.g. - Employee, Job
Each entity has attributes the different types of attributes include
1) Composite vs Atomic
2) Single valued vs Multivalued
3) Stored vs Derived
4) NULL attributes
5) Complex Composite Multivalued Attributes

| Composite | Atomic |
|-|-|
| Composite can be subdivided into individual attributes | The smallest Attribute cannot be divided|
|eg: Address usually has House Name, City, State, Country| eg: Age is an atomic cause we cannot split it down to more components |

| Single Values |Multivalued |
|-|-|
| Single valued include just having one value | The value that has multiple values |
|eg: Roll Number is only a single value which may be alphanumeric | eg: Person can have multiple phone numbers |

| Stored  |Derived |
|-|-|
| The values are stored directly in the database | The value is derived from any stored values |
|eg: Employee Number can be stored directly on the database| eg: Age can be calculate by date of base |

#### NULL Value
The value for an attribute can be NULL when there is no applicable value that can be placed there or the value is unknown.

### Entity Type 
It is defines a collection of entities with the same attributes & Collection of all Entities in the database is called an entity set.

### Key Attribute 
They are attributes that have a unique value for each attribute. There could be more than one key attribute.

### Domain 
It is the allowed set of values of an attribute, eg Age should be a number, Phone No should be a 10 digit number

## Relationship
#Important 
It is an association between two or more entities, each relationship has a 
- Name 
- Degree (Number of Attributes) and
- Cardinality (Number of Entities/Tuples)

#### Degree of a Relation ship
- Unary
- Binary
- Ternary

### Constraints 
Constrains are the limit of relations that an entity can participate in.
1) Cardinality Ration - Maximum number of relations an entity can participate in.
2) Participant Constraints - Minimum number of relations an entity can participate in.
	1) Total Participation - Every entity in a type participates in atleast one relation (represented in double lines)
	2) Partial participation - Some entities may not participate in any relationship, (represented in single lines)

### Cardinality 
It refers to the number of Entities in a given relation.
There can be classified into the following: 
1) One to One
2) One to Many
3) Many to One
4) Many to Many

## Types of Entities
There are two type of entities

### Strong entity types 
- Should have one key attribute
- Always will have a primary key
- It will be not dependent of any other entity
- Represented by single rectangle 
- Strong entities make relations represented by single diamond

### Weak entity types
- Does not have any attribute
- Dependent on a strong entity.
- No primary key
- Has a partial discriminator key
- Double rectangle representation 

## ER Diagram Notations
![[Images/Pasted image 20230713015343.png]]

## Example ER Diagram
![[Images/Pasted image 20230713092621.png]]

#### Min Max Notation
The structural notation is specified in the format (min, max), represent the minimum and maximum number of entities participating in the given relation.
In the above example the information that we get will be the number of departments an employee will work in is 1, and the number of employees in a dept is a minimum of 1 and a maximum of N.

