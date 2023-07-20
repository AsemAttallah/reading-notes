# Hashtable?
## What is a Hashtable?
* 'A hash table is a data structure that you can use to store data in key-value format with direct access to its items in constant time.

* Hash tables are said to be associative, which means that for each key, data occurs at most once. Hash tables let us implement things like phone books or dictionaries; in them, we store the association between a value (like a dictionary definition of the word "lamp") and its key (the word "lamp" itself).

* We can use hash tables to store, retrieve, and delete data uniquely based on their unique key.'

## Why do we use Hashtable?
* The most valuable aspect of a hash table over other abstract data structures is its speed to perform insertion, deletion, and search operations. Hash tables can do them all in constant time.

* For those unfamiliar with time complexity (big O notation), constant time is the fastest possible time complexity. Hash tables can perform nearly all methods (except list) very fast in O(1) time.

### The Hash table data structure stores elements in key-value pairs where

* Key- unique integer that is used for indexing the values
* Value - data that are associated with keys.

### In a hash table, a new index is processed using the keys. And, the element corresponding to that key is stored in the index. This process is called hashing.

* Let k be a key and h(x) be a hash function.

* Here, h(k) will give us a new index to store the element linked with k.

## When the hash function generates the same index for multiple keys, there will be a conflict (what value to be stored in that index). This is called a hash collision.We can resolve the hash collision using one of the following techniques.

* Collision resolution by chaining
* Open Addressing: Linear/Quadratic Probing and Double Hashing