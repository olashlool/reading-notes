# Reading 20: Hash Table

## What is a Hashtable?
- Hash - A hash is the result of an algorithm taking an incoming string and converting it into a value that could be used 
for either security or some other purpose. In the case of a hashtable, it is used to determine the index of the array.

- Buckets - A bucket is what is contained in each index of the array of the hashtable. Each index is a bucket that could 
potentially contain multiple key/value pairs if a collision occurs.

- Collisions - A collision is what happens when more than one key gets hashed to the same location of the hashtable.

- Hashtables - A data structure that utilize key value pairs. Every Node or Bucket has both a key, and a value. 
The same key should always produce the same hash code. Hashtables allow us to store the key into this data structure, 
and quickly retrieve the value. This is done through a hash, which is the ability to encode the key that will eventually 
map to a specific location in the data structure that we can look at directly to retrieve the value.

## Time Complexity
- Since we are able to hash our key and determine the exact location where our value is stored, we can do a lookup in an O(1) time complexity.
- Calculating the hash code and reading an array at that index is all constant time, so the hash map has O(1) read access

## Creating a Hash
- Create an array. The size of the array is important for index placement
- Add logic that will turn the “key” into a numeric number value, for example:
    - Add or multiply all the ASCII values together.
    - Multiply it by a prime number such as 599.
    - Use modulo to get the remainder of the result, when divided by the total size of the array.
    - Insert into the array at that index.
    
## Collisions
- A collision occurs when more than one key hashes to the same index in an array.
- A “perfect hash” will never have any collisions.

## Collision Resolution Techniques
- Separate Chaining - Separate chaining is one of the most commonly used collision resolution techniques. It is usually 
implemented using linked lists.

    - Instead of starting all the buckets as null we can initialize a LinkedList in each one.
    - If two keys get the same index in the array their key/value pairs can be stored as a node in a linked list.
    - It is important to store the entire key/value pair in the bucket, not just the value, because different keys can lead 
    to the same bucket.

- Linear probing - In open addressing, instead of in linked lists, all entry records are stored in the array itself. 
When a new entry has to be inserted, the hash index of the hashed value is computed and then the array is examined 
(starting with the hashed index). If the slot at the hashed index is unoccupied, then the entry record is inserted in 
slot at the hashed index else it proceeds in some probe sequence until it finds an unoccupied slot.

- Quadratic probing - Quadratic probing is similar to linear probing and the only difference is the interval between 
successive probes or entry slots. Here, when the slot at a hashed index for an entry record is already occupied, 
you must start traversing until you find an unoccupied slot. The interval between slots is computed by adding the 
successive value of an arbitrary polynomial in the original hashed index.

- Double hashing - Double hashing is similar to linear probing and the only difference is the interval between successive 
probes. Here, the interval between probes is computed by using two hash functions.

## How Hash Maps Store Values:

- Accept a key
- Calculate the hash of the key
- Use modulus to convert the hash into an array index
- Store the key with the value by appending both to the end of a linked list

## How Hash Maps Read A Value:
- Accept a key
- Calculate the hash of the key
- Use modulus to convert the hash into an array index
- Use the array index to access the short LinkedList representing a bucket
- Search through the bucket looking for a node with a key/value pair that matches the key you were given

## Bucket Sizes
- Hash Maps can have any number of buckets.
- More buckets mean fewer collisions, but more unused space.
- Load Factor - tells us how full the hash table is. A hash table can calculate its own load factor and automatically 
grow when needed.