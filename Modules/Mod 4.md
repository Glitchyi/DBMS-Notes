## Anomalies in Designing a DB

### Insertion Anomalies 
Certain information cannot be stored unless other information is already present.
e.g. When adding an employee we must be able to assign a department to him if there is no department table we have to use NULL values, similarly we end up using NULL values for creating departments without employees.

### Deletion Anomalies
Certain information cannot be deleted without loosing on other information. e.g. When we delete the last record of a department from the dept table we end up loosing info about that department ever existing.

### Modification Anomalies
Updating information for similar information is not all updated consistently we end up with having different values for different parts of the database.

## Informal Design Guidelines for Relation Schema
[[Topics/DB Design Guidelines|DB Design Guidelines]]

Four informal guidelines that may be used as measures to determine the quality of relation schema design:
- Making sure that the semantics of the attribute is clear in the schema
- Reducing the redundant information in tuples - Design a schema that does not suffer from the insertion, deletion and update anomalies
- Reducing the NULL values in tuples
- Disallowing the possibility of generating spurious tuples

## Armstrong’s Axioms in Functional Dependency
The term Armstrong axioms refer to the sound and complete set of inference rules or axioms, introduced by William W Armstrong. Axioms that is used to test the logical implication of functional dependencies. If F is a set of functional dependencies then the closure of F, denoted as F+, is the set of all functional dependencies logically implied by F. Armstrong’s Axioms are a set of rules, that when applied repeatedly, generates a closure of functional dependencies.

## AXIOMS
#Important 
IR1: Reflexivity rule
- If A is a set of attributes and B is subset of A (B⊆A), then A holds B (A→B).
- This property is trivial property.
IR2: Augmentation rule
- If A→B holds and Y is attribute set, then AY→BY also holds.
- That is adding attributes in dependencies, does not change the basic dependencies.
- If A→B , then AC→BC for any C.
IR3: Transitivity rule
- Same as the transitive rule in algebra, if A→B holds and B→C holds, then A→C also holds.

## Secondary Rules
IR4: Union/Additive rule
- If A→B holds and A→C holds, then A→BC holds.
IR5: Decomposition/Projective rule
- If A→BC holds then A→B and A→C holds.
IR6: Composition rule
- If A→B and X→Y holds, then AX→BY holds.
IR7: Pseudo Transitivity rule
- If A→B holds and BC→D holds, then AC→D holds.


[[Topics/Normalization]]
[[Topics/Minimal Covers]]
