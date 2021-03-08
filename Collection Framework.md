COLLECTIONS IN JAVA

Collection
* A Collection represents a single unit of objects, i.e., a group.
* The Collection in Java is a framework that provides an architecture to store and manipulate the group of objects.
* Java Collections can achieve all the operations that you perform on a data such as searching, sorting, insertion, manipulation, and deletion. 

Collection framework
* The Collection framework represents a unified architecture for storing and manipulating a group of objects. It has:
  * Interfaces and its implementations, i.e., classes 
  * Algorithm
  
Interfaces in Java
* Set
* List
* Queue
* Deque

Classes in Java
* ArrayList 
* Vector
* LinkedList
* PriorityQueue
* HashSet
* LinkedHashSet
* TreeSet

Iterator interface
* Iterator interface provides the facility of iterating the elements in a forward direction only. 

Iterable Interface
* The Iterable interface is the root interface for all the collection classes.
* The Collection interface extends the Iterable interface and therefore all the subclasses of Collection interface also implement the Iterable interface.

Collection Interface
* The Collection interface is the interface which is implemented by all the classes in the collection framework.
* Collection interface builds the foundation on which the collection framework depends.
* Example:
  * Boolean add ( Object obj), 
  * Boolean addAll ( Collection c), 
  * void clear()

List Interface
* List interface is the child interface of Collection interface.
* It inhibits a list type data structure in which we can store the ordered collection of objects.
* It can have duplicate values.
* Syntax:   
  List <data-type> list1= new ArrayList();  
  List <data-type> list2 = new LinkedList();  
  List <data-type> list3 = new Vector();  
  List <data-type> list4 = new Stack(); 

ArrayList
* The ArrayList class implements the List interface.
* It uses a dynamic array to store the duplicate element of different data types.
* The ArrayList class maintains the insertion order and is non-synchronized.
* The elements stored in the ArrayList class can be randomly accessed. 

LinkedList
* LinkedList implements the Collection interface.
* It uses a doubly linked list internally to store the elements.
* It can store the duplicate elements.
* It maintains the insertion order and is not synchronized.
* In LinkedList, the manipulation is fast because no shifting is required.

Vector
* Vector uses a dynamic array to store the data elements.
* It is similar to ArrayList. 
* It is synchronized.
* It contains many methods that are not the part of Collection framework.

Stack
* The stack is the subclass of Vector.
* It implements the last-in-first-out data structure, i.e., Stack.
* The stack contains all the methods of Vector class.
* It provides its methods which defines its properties like 
  * boolean push(), 
  * boolean peek(),
  * boolean push(object o).

Queue Interface
* Queue interface maintains the first-in-first-out order.
* It can be defined as an ordered list that is used to hold the elements which are about to be processed.
* There are various classes which implements the Queue interface like 
  * PriorityQueue,
  * Deque,
  * ArrayDeque.
* Queue interface can be instantiated as:
    * Queue<String> q1 = new PriorityQueue();  
    * Queue<String> q2 = new ArrayDeque();  

PriorityQueue
* The PriorityQueue class implements the Queue interface.
* It holds the elements or objects which are to be processed by their priorities.
* PriorityQueue doesn't allow null values to be stored in the queue.

Deque Interface
* Deque interface extends the Queue interface.
* In Deque, we can remove and add the elements from both the side.
* Deque stands for a double-ended queue which enables us to perform the operations at both the ends.
* Deque can be instantiated as:
  * Deque d = new ArrayDeque();  

ArrayDeque
* ArrayDeque class implements the Deque interface.
* It facilitates us to use the Deque.
* Unlike queue, we can add or delete the elements from both the ends.
* ArrayDeque is faster than ArrayList and Stack and has no capacity restrictions.

Set Interface
* Set Interface in Java is present in java.util package.
* It extends the Collection interface.
* It represents the unordered set of elements which doesn't allow us to store the duplicate items.
* We can store at most one null value in Set.
* Set is implemented by 
  * HashSet,
  * LinkedHashSet, 
  * TreeSet.

Set can be instantiated as:

    Set<data-type> s1 = new HashSet<data-type>();  
    Set<data-type> s2 = new LinkedHashSet<data-type>();  
    Set<data-type> s3 = new TreeSet<data-type>();  

HashSet
* HashSet class implements Set Interface.
* It represents the collection that uses a hash table for storage.
* Hashing is used to store the elements in the HashSet.
* It contains unique items.

LinkedHashSet
* LinkedHashSet class represents the LinkedList implementation of Set Interface.
* It extends the HashSet class and implements Set interface.
* Like HashSet, It also contains unique elements.
* It maintains the insertion order and permits null elements.

SortedSet Interface
* SortedSet is the alternate of Set interface that provides a total ordering on its elements.
* The elements of the SortedSet are arranged in the increasing order.
* The SortedSet provides the additional methods that inhibit the natural ordering of the elements.

The SortedSet can be instantiated as:

    SortedSet<data-type> set = new TreeSet();  

TreeSet
* Java TreeSet class implements the Set interface that uses a tree for storage.
* Like HashSet, TreeSet also contains unique elements.
* However, the access and retrieval time of TreeSet is quite fast.
* The elements in TreeSet stored in ascending order.


