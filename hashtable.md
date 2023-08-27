What is a Hashtable?
   Hashtables are a data structure that utilize key value pairs. This means every Node or Bucket has both a key, and a value.

   The basic idea of a hashtable is the ability to store the key into this data structure, and quickly retrieve the value. This is done through what we call a hash. A hash is the ability to encode the key that will eventually map to a specific location in the data structure that we can look at directly to retrieve the value.

   Since we are able to hash our key and determine the exact location where our value is stored, we can do a lookup in an O(1) time complexity. This is ideal when quick lookups are required.

how to Creat a Hash?
 -  Add or multiply all the ASCII values together.
 - Multiply it by a prime number such as 599.
 - Use modulo to get the remainder of the result, when divided by the total size of the array.
 - Insert into the array at that index.

example:

Key = "Cat"
Value = "Josie"
67 + 97 + 116 = 280
280 * 599 = 69648
69648 % 1024 = 16
Key gets placed in index of 16. 

what is Collisions?
   A collision occurs when more than one key hashes to the same index in an array. As mentioned earlier, a “perfect hash” will never have any collisions.
this can solved by using linkedlist inside the array each time we create a linkedlist we cheked if there is a linked list allreadey created or not, if there is a linked list we create a new node inside the same linked list.