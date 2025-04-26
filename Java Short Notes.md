
## Java Collections Framework :
```
1. List (Interface) - Implementations: ArrayList, LinkedList, Vector, Stack
add(E e): Adds an element to the end of the list.
add(int index, E element): Inserts an element at the specified index.
get(int index): Retrieves an element at the specified index.
remove(int index): Removes the element at the specified index.
remove(Object o): Removes the first occurrence of the specified object.
set(int index, E element): Replaces the element at the specified index.
contains(Object o): Return true if found.
indexOf(Object o): Returns the index of the first occurrence of the specified element.
lastIndexOf(Object o): Returns the index of the last occurrence of the specified element. If not found returns -1


2. Set (Interface) - Implementations: HashSet, LinkedHashSet, TreeSet
add(E e): Adds an element to the set.
remove(Object o): Removes the specified element from the set.
contains(Object o): Checks if the set contains the specified element.
toArray(): Converts the set to an array.

3. Queue (Interface) - Implementations: PriorityQueue, LinkedList, ArrayDeque
offer(E e): Adds an element to the queue (returns false if full).
poll(): Removes and returns the front element (returns null if empty).
peek(): Retrieves the front element (returns null if empty).

4. Deque (Interface) - Implementations: ArrayDeque, LinkedList
offerFirst(E e): Adds an element at the front of the deque (returns false if full).
offerLast(E e): Adds an element at the end of the deque (returns false if full).
pollFirst(): Removes and returns the front element (returns null if empty).
pollLast(): Removes and returns the last element (returns null if empty).
peekFirst(): Retrieves the front element (returns null if empty).
peekLast(): Retrieves the last element (returns null if empty).

5. Map (Interface) - Implementations: HashMap, LinkedHashMap, TreeMap, Hashtable
put(K key, V value): Adds or updates a key-value pair in the map.
get(Object key): Retrieves the value associated with the key.
remove(Object key): Removes the key-value pair for the specified key.
containsKey(Object key): Checks if the map contains the specified key.
containsValue(Object value): Checks if the map contains the specified value.
keySet(): Returns a set of all keys in the map.
values(): Returns a collection of all values in the map.
entrySet(): Returns a set of all key-value pairs in the map.

Common methods :
size(): Returns the number of entries.
clear(): Removes all entries.
isEmpty(): Return true if no entries present.

```

## Iterators :
### List
```
for (int i = 0; i < fruits.size(); i++) System.out.println(fruits.get(i));
for (String fruit : fruits) System.out.println(fruit);
```
###  Set
```
for (String city : cities) System.out.println(city);
```
### Queue
```
while (!queue.isEmpty()) System.out.println(queue.poll());
for (String item : queue) System.out.println(item);
```
### Map
```
for (Map.Entry<Integer, String> entry : map.entrySet()) System.out.println(entry.getKey() + " : " + entry.getValue());
```

## Exceptions :

```
class CustomException extends Exception{
    public CustomException(String message) {
        super(message);
    }
}


// Exceptions
class Main {
    
    public void getException() throws CustomException{
        throw new CustomException("Divide by zero");
    }
    
    public static void main(String[] args) {
        
        Main m = new Main();
        
        try {
            int x = 10 / 0;
        } catch (ArithmeticException e) {
            System.out.println("Exception Occured : " + e.getMessage());
        } 
        
        try {
            m.getException();
        } catch (CustomException e) {
            System.out.println("Custom Exception Occured : " + e.getMessage());
        } finally {
            System.out.println("Finally will execute anyway");
        }
        
    }
}

```
