# Implementation: Hash Tables

## Hash Tables in JavaScript Quiz

Test your knowledge about Hash Tables and their implementation in JavaScript by answering the following questions. Choose the best answer for each question.

**Question 1:** What is a Hash Table in JavaScript?

a) A built-in data structure for managing asynchronous operations.

b) A collection of ordered key-value pairs.

c) A data structure that stores key-value pairs and uses a hash function to index and retrieve values efficiently.

d) A method for converting arrays into strings.

**Question 2:** What is the purpose of a hash function in a Hash Table?

a) To sort the key-value pairs.

b) To convert values into keys.

c) To generate a unique index for each key.

d) To determine the length of the Hash Table.

**Question 3:** In JavaScript, which built-in object can be used to implement Hash Tables?

a) `Set`

b) `Object`

c) `Map`

d) `Array`

**Question 4:** What is a collision in the context of Hash Tables?

a) A situation where a key is missing from the Hash Table.

b) A situation where two different keys produce the same hash value and collide in the same bucket.

c) A situation where the Hash Table becomes too large to handle.

d) A situation where the hash function fails to generate an index.

**Question 5:** How can you handle collisions in Hash Tables?

a) By ignoring collisions and moving to the next bucket.

b) By increasing the size of the Hash Table.

c) By using a linked list or another data structure to store multiple values in the same bucket.

d) By removing the collided key from the Hash Table.

**Question 6:** Which of the following is a common method to create a hash function?

a) Returning the length of the key.

b) Converting characters of the key to ASCII values and summing them up.

c) Ignoring the key and using a random number as the index.

d) Using the `Math.random()` function to generate a hash value.

**Question 7:** What is the average time complexity for inserting, searching, and deleting elements in a well-implemented Hash Table?

a) O(1)

b) O(log n)

c) O(n)

d) O(n log n)

**Question 8:** In JavaScript, how can you check if a specific key exists in a Hash Table?

a) Using the `hasKey()` method.

b) By directly accessing the key as a property and checking for `undefined`.

c) Hash Tables don't support key existence checks.

d) By using the `containsKey()` function.

**Question 9:** Why are Hash Tables considered efficient for data retrieval?

a) They use linked lists for all their operations.

b) They have a fixed size, which guarantees constant time operations.

c) The hash function allows for direct indexing of values based on their keys.

d) They automatically sort the data to improve retrieval times.

**Question 10:** What is one potential drawback of using Hash Tables?

a) They are memory-intensive and can lead to high memory usage.

b) They only support string keys, limiting their usability.

c) Hash Tables cannot store complex data structures like arrays.

d) Hash Tables have slow average time complexity for most operations.

**Question 11:** Which Hash Table implementation in JavaScript provides a predictable order of keys?

a) The native `Object` type.

b) The `Map` type.

c) The `Set` type.

d) The `HashTable` class.

**Question 12:** When might using a Hash Table be preferable over using an Array?

a) When you need to maintain an ordered collection of elements.

b) When memory usage needs to be minimized.

c) When you need constant-time access to elements using keys.

d) When you only have a small number of elements to store.

**Question 13:** What happens if two different keys consistently produce the same hash value in a Hash Table?

a) The Hash Table crashes and becomes unusable.

b) A new bucket is created to accommodate the collision.

c) The hash function is automatically adjusted to prevent collisions.

d) A chain of linked list nodes is created in the same bucket to handle the collision.

**Question 14:** Which operation on Hash Tables is most affected by a poor hash function?

a) Insertion

b) Deletion

c) Retrieval

d) Resizing

**Question 15:** In open addressing collision resolution, what does linear probing refer to?

a) Using a linked list to store collided elements.

b) Hashing the key value repeatedly until a unique index is found.

c) Skipping a fixed number of indexes to find the next available slot.

d) Rehashing the entire table when a collision occurs.

**Bonus Question:** What is a potential security risk related to hash collisions in Hash Tables?

a) Collisions can lead to loss of data integrity.

b) Collisions can be exploited to slow down the Hash Table operations.

c) Hash collisions can cause memory leaks.

d) Hash collisions might expose sensitive data stored in the Hash Table.

---

## [Read Intro to Hash Tables](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-30/resources/Hashtables.html)

## [Watch what is a hash table?](https://www.youtube.com/watch?v=MfhjkfocRR0)

## [Read basics of hash tables](https://www.hackerearth.com/practice/data-structures/hash-tables/basics-of-hash-tables/tutorial/)

## [Skim hash table wiki](https://en.wikipedia.org/wiki/Hash_table)

## [Answers](./HashTablesAnswers.md)

## [Main Page](../README.md)
