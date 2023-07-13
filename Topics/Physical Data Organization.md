## Primary file organizations
Determines how the files records are stored physically

### Heap file (or unordered file) 
Places the records on disk in no particular order by appending new records at the end of the file

### Sorted file (or sequential file) 
Keeps the records ordered by the value of a particular field (called the sort key).

### Hashed file 
It uses a hash function applied to a particular field (called the hash key) to determine a record’s placement on disk.

## Spanned and Unspanned Organization
When records are kept in a block (Block is the unit of data that can be transferred in one request)

#### Spanned organization 
This type of organization allows for cross block boundaries i.e. it allows records to span between two blocks

#### Unspanned Organization 
The organization does not allow for records to span across block all the records should be confined in blocks

## Blocking Factor 
#Important 

| Value | Notation |
|-|-|
| Block Size | B |
| Record Size | R |
| Blocking Factor | BFR = B/R |
|Number of records | r |

```
Total number of blocks, b = r/BFR
```

# Index Structures
Indexing structures are used to speed up retrieval of records, there are different types of structures Single Level and Multi Level, they can also be characterized as:
- Dense - Each record has its own index entry
- Sparse - Each block has its entry

## Single Level
Single level indexing makes use of one index file.

### Primary Index
When we make use of the primary index of the table.  primary index is an ordered file whose records are of fixed length with two fields.

![[Images/Pasted image 20230713214330.png]]

### Clustering index
Non Key fields are used in the index file to store the indexes, these keys are need not be distinct for each record

The field is called the clustering field 
The data file is called a clustered file

![[Images/Pasted image 20230713214726.png]]


### Secondary Index
A secondary index provides a secondary means of accessing a file for which some primary access already exists. This may be based on any candidate key which has unique values for tuples

## Multi Level
Multi level indexing deals with indexing with more than one index file, there will be an index file for the index file which further reduces the number of access we need to make to the database
Idea behind a multilevel index is to reduce part of the index that we continue to search by BFRI , blocking factor for index, which is larger than 2.

For multilevel indexing, each level has  CHECK PDF !!!


## B Trees & B + Trees
How to build a B tree we push the middle value to the top ez.


