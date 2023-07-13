## Relational Data Model
[[Relational Algebra]]

### Components of a relational database
1) Domain
2) Tuple (Rows/Values)
3) Attributes (Columns)
4) Keys
5) Relations (Tables)

### Domain
The set of possible atomic values. eg. The domain of phone numbers should contain 10 digits and should preferably start with the country code, dates follow a format.

### Tuples
Ordered set of values, each tuple contains data described in an entity relation or object.

### Attributes
They are the fields of the data, The attribute determines the type and format of the data in a tuple.

### Keys
They refer to a value of data that can be used to uniquely identify rows

### Relations
A relation is a table of values which are formed by making of a set of tuples which follow attributes.
>Degree is the number of attributes in a relation

#### Relation State
It is the subset of Cartesian products of the domains of its attributes
i.e. the set of all possible tuples

## Relational Model Notations
Different was a relational model can be denoted
- Schema Notation R(A1, A2, A3...)
- Relational State Notation:
	- r(R) = {t1,t2,.. , tn}
	- r(R) ⊂ dom(A1) ⅹ dom(A2) ⅹ dom(A3) ⅹ ...
- Tuple in a relation is denoted by ti = <v1,v2,v3...>

### Characteristics of Relation
1) Ordering of tuples in a relation r(R) -  The tuples are not considered to be ordered, even though they appear to be in the tabular form. (there is no row order)
2) Ordering of attributes in a relation - The values in a tuple will always be ordered according to the schema
3) All values in a tuple are assumed to be atomic, NULL used to specify unknown and not applicable values
4) Meaning of a relation - basically what meaning the tuple represents 

## Relational Model Constrains
These are conditions that must hold valid for all relation states.

Three main types of constraints: 
- Inherent model-based constraints/ Implicit
- Schema-based constraints/ Explicit
- Application based constraints/ Semantic

### Inherent model-based Constraints
- Constraints that are inherent/ inbuilt in the data model.
- Eg: A relation cannot have duplicate tuples.

### Application based Constraints
- Cannot be expressed in a schema.
- Defined in application programs.

### Schema-based Constraints
- Domain constraint
- Key constraint
- Constraints on NULLs – whether permitted or not
- Entity Integrity constrains
- Referential Integrity constraints

## Key Constraints
- Primary Key - The main key that is being used for tuples
- Candidate Key - Possible keys that can be used as Primary Keys
- Secondary Key  - 
- Alternate Key
- Composite Key
- Foreign Key
- Super Key