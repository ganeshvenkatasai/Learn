```
1️⃣ Core Java (Must-Know Basics)
✅ Data Types & Variables
✅ Operators (Arithmetic, Logical, Bitwise, etc.)
✅ Control Statements (if-else, switch, loops)
✅ Arrays & Strings
✅ Methods & Recursion
✅ OOPs Concepts (Encapsulation, Inheritance, Polymorphism, Abstraction)
✅ Interfaces & Abstract Classes
✅ Exception Handling (try-catch-finally, throws, throw)
✅ Java Memory Management (Heap, Stack, Garbage Collection)

2️⃣ Java Collections Framework (JCF)
✅ List, Set, Map Interfaces
✅ ArrayList vs LinkedList
✅ HashMap vs TreeMap vs LinkedHashMap
✅ HashSet vs TreeSet vs LinkedHashSet
✅ PriorityQueue & Deque
✅ Sorting & Comparators

3️⃣ Multithreading & Concurrency
✅ Threads & Runnable Interface
✅ Thread Lifecycle
✅ Synchronization & Locks
✅ Executors & Thread Pools
✅ Fork-Join Framework
✅ Atomic Variables
✅ Volatile & ReentrantLock

4️⃣ Java 8+ Features
✅ Lambda Expressions
✅ Functional Interfaces
✅ Streams API (map, filter, reduce)
✅ Method References
✅ Default & Static Methods in Interfaces
✅ Optional Class

5️⃣ File Handling & Serialization
✅ FileReader & FileWriter
✅ BufferedReader & BufferedWriter
✅ Object Serialization (Serializable Interface)

6️⃣ JDBC (Java Database Connectivity)
✅ Connecting to MySQL/PostgreSQL
✅ PreparedStatement vs Statement
✅ Connection Pooling

7️⃣ Java Networking
✅ Sockets & ServerSocket
✅ HTTP Clients

8️⃣ Spring Framework & Spring Boot
✅ Spring Core (Dependency Injection, Beans, AOP)
✅ Spring MVC (Controllers, ViewResolver, REST APIs)
✅ Spring Boot (AutoConfiguration, Annotations)
✅ Spring Data JPA & Hibernate
✅ Spring Security (JWT, OAuth2)
✅ Spring Cloud (Microservices, Eureka, Feign, Resilience4j)

9️⃣ Microservices & Cloud
✅ Building REST APIs
✅ gRPC Communication
✅ Docker & Kubernetes
✅ Kafka & RabbitMQ (Event-Driven Architecture)
✅ Istio & Service Mesh
✅ Cloud Platforms (AWS, GCP, Azure)

🔟 Testing in Java
✅ JUnit & TestNG
✅ Mockito (Mocking & Stubbing)
✅ Integration Testing with Spring Boot

1️⃣1️⃣ Design Patterns
✅ Singleton, Factory, Prototype, Builder
✅ Adapter, Decorator, Observer, Strategy
✅ Microservices Design Patterns (Circuit Breaker, API Gateway)

1️⃣2️⃣ Advanced Java Topics
✅ JVM Internals (ClassLoader, JIT Compiler, Garbage Collectors)
✅ Reactive Programming (Project Reactor, WebFlux)
✅ GraphQL in Java
✅ Performance Optimization & Profiling (JProfiler, VisualVM)




Java Collections Framework

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
subList(int fromIndex, int toIndex): Returns a sublist between the specified indices.

2. Set (Interface) - Implementations: HashSet, LinkedHashSet, TreeSet
add(E e): Adds an element to the set.
remove(Object o): Removes the specified element from the set.
contains(Object o): Checks if the set contains the specified element.
toArray(): Converts the set to an array.
iterator(): Returns an iterator over the set.

3. Queue (Interface) - Implementations: PriorityQueue, LinkedList, ArrayDeque
add(E e): Adds an element to the queue (throws exception if full).
offer(E e): Adds an element to the queue (returns false if full).
remove(): Removes and returns the front element (throws exception if empty).
poll(): Removes and returns the front element (returns null if empty).
element(): Retrieves the front element (throws exception if empty).
peek(): Retrieves the front element (returns null if empty).

4. Deque (Interface) - Implementations: ArrayDeque, LinkedList
addFirst(E e): Adds an element at the front of the deque.
addLast(E e): Adds an element at the end of the deque.
offerFirst(E e): Adds an element at the front of the deque (returns false if full).
offerLast(E e): Adds an element at the end of the deque (returns false if full).
removeFirst(): Removes and returns the front element.
removeLast(): Removes and returns the last element.
pollFirst(): Removes and returns the front element (returns null if empty).
pollLast(): Removes and returns the last element (returns null if empty).
getFirst(): Retrieves the front element (throws exception if empty).
getLast(): Retrieves the last element (throws exception if empty).
peekFirst(): Retrieves the front element (returns null if empty).
peekLast(): Retrieves the last element (returns null if empty).

5. Map (Interface) - Implementations: HashMap, LinkedHashMap, TreeMap, Hashtable
put(K key, V value): Adds or updates a key-value pair in the map.
putAll(Map<? extends K, ? extends V> m): Adds all entries from another map.
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

1. Collection to Array
String[] arr = list.toArray(new String[0]);  
Integer[] arr = set.toArray(new Integer[0]);  
Double[] arr = queue.toArray(new Double[0]);  
Integer[] arr = map.keySet().toArray(new Integer[0]);  

2. Array to Collection
List<String> list = Arrays.asList(array);  
Set<Integer> set = new HashSet<>(Arrays.asList(array));  
Queue<Double> queue = new LinkedList<>(Arrays.asList(array));  

3. Collection to Another Collection
Set<String> set = new HashSet<>(list);  
Queue<Integer> queue = new LinkedList<>(list);  
List<Double> list = new ArrayList<>(set);  
List<String> list = new ArrayList<>(queue);  

4. Collection to Map
Map<Integer, String> map = list.stream().collect(Collectors.toMap(obj -> obj.getId(), obj -> obj.getName()));  
Map<Integer, String> map = IntStream.range(0, keys.size()).boxed().collect(Collectors.toMap(keys::get, values::get));  

5. Map to Collection
List<Integer> keyList = new ArrayList<>(map.keySet());  
Set<String> valueSet = new HashSet<>(map.values());  
List<Map.Entry<Integer, String>> entryList = new ArrayList<>(map.entrySet());  

6. String to Collection
List<String> list = Arrays.asList(str.split(","));  
Set<String> set = new HashSet<>(Arrays.asList(str.split(",")));  

7. Stream-Based Conversions
Stream<String> stream = list.stream();  
List<Integer> list = stream.collect(Collectors.toList());  
String[] arr = stream.toArray(String[]::new);  


String Methods:
length() - Returns the length of the string.
charAt(int index) - Returns the character at the specified index.
substring(int beginIndex) - Returns a substring from the specified start index.
substring(int beginIndex, int endIndex) - Returns a substring from the start index to the end index.
contains(CharSequence sequence) - Returns true if the string contains the specified sequence.
equals(Object anObject) - Compares the string to the specified object for equality.
equalsIgnoreCase(String anotherString) - Compares the string to the specified string, ignoring case.
compareTo(String anotherString) - Compares the string to the specified string lexicographically.
compareToIgnoreCase(String str) - Compares the string to the specified string, ignoring case, lexicographically.
startsWith(String prefix) - Returns true if the string starts with the specified prefix.
endsWith(String suffix) - Returns true if the string ends with the specified suffix.
indexOf(int ch) - Returns the index of the first occurrence of the specified character.
indexOf(String str) - Returns the index of the first occurrence of the specified substring.
lastIndexOf(int ch) - Returns the index of the last occurrence of the specified character.
lastIndexOf(String str) - Returns the index of the last occurrence of the specified substring.
replace(char oldChar, char newChar) - Returns a new string with all occurrences of oldChar replaced by newChar.
replace(CharSequence target, CharSequence replacement) - Replaces each substring of the string that matches the literal target with the specified replacement.
replaceAll(String regex, String replacement) - Replaces each substring of the string that matches the regex with the specified replacement.
replaceFirst(String regex, String replacement) - Replaces the first substring of the string that matches the regex with the specified replacement.
toLowerCase() - Converts all characters in the string to lowercase.
toUpperCase() - Converts all characters in the string to uppercase.
trim() - Removes leading and trailing whitespace from the string.
split(String regex) - Splits the string around matches of the given regular expression.
split(String regex, int limit) - Splits the string around matches of the given regular expression, with a limit on the number of splits.
concat(String str) - Concatenates the specified string to the end of the current string.
join(CharSequence delimiter, CharSequence... elements) - Joins the given elements with the specified delimiter.
valueOf(int i) - Returns the string representation of the specified integer.
toCharArray() - Converts the string into a new character array.
isEmpty() - Returns true if the string is empty (length is 0).
matches(String regex) - Returns true if the string matches the specified regular expression.
regionMatches(int toffset, String other, int ooffset, int len) - Tests if two string regions are equal.
regionMatches(boolean ignoreCase, int toffset, String other, int ooffset, int len) - Tests if two string regions are equal, with an option to ignore case.
contains(CharSequence sequence) - Checks if the string contains the specified sequence of characters.
format(String format, Object... args) - Returns a formatted string using the specified format and arguments.
getBytes() - Encodes the string into a sequence of bytes using the platform's default charset.
getBytes(Charset charset) - Encodes the string into a sequence of bytes using the specified charset.
intern() - Returns a canonical representation of the string.
toString() - Returns the string itself (overridden from Object).
substring(int beginIndex) - Returns a substring from the specified start index to the end of the string.
contentEquals(StringBuffer sb) - Compares the string to the specified StringBuffer for equality.
hashCode() - Returns the hash code for the string.
Common String Operations:
Concatenation: String str3 = str1 + str2;
StringBuilder (mutable strings): StringBuilder sb = new StringBuilder("Hello");
String.format(): String formatted = String.format("Value: %d", 42);
StringBuffer (synchronized mutable strings): StringBuffer sb = new StringBuffer("Hello");
String Comparison: str1.equals(str2), str1.equalsIgnoreCase(str2)



Exception :

// Custom Exception Class
class MyException extends Exception {
    MyException(String message) {
        super(message);
    }
}

public class ExceptionExamples {
    
    // Method using throws
    static void checkAge(int age) throws Exception {
        if (age < 18) {
            throw new Exception("Not eligible to vote");
        }
        System.out.println("You can vote!");
    }
    
    // Method to trigger StackOverflowError
    static void recursiveMethod() {
        recursiveMethod(); // Infinite recursion → StackOverflowError
    }

    public static void main(String[] args) {
        
        // 1. Checked Exception (FileNotFoundException)
        try {
            FileReader file = new FileReader("file.txt"); // Might not exist!
        } catch (FileNotFoundException e) {
            System.out.println("File not found!");
        }

        // 2. Unchecked Exception (ArithmeticException)
        try {
            int num = 10 / 0;
        } catch (ArithmeticException e) {
            System.out.println("Cannot divide by zero!");
        }

        // 3. Multiple Catch Blocks
        try {
            int[] arr = {1, 2, 3};
            System.out.println(arr[5]); // ArrayIndexOutOfBoundsException
        } catch (ArithmeticException e) {
            System.out.println("Math error!");
        } catch (ArrayIndexOutOfBoundsException e) {
            System.out.println("Index out of bounds!");
        }

        // 4. Finally Block
        try {
            System.out.println(10 / 2);
        } catch (Exception e) {
            System.out.println("Error!");
        } finally {
            System.out.println("This will always execute.");
        }

        // 5. Throws Keyword Example
        try {
            checkAge(15);
        } catch (Exception e) {
            System.out.println(e.getMessage());
        }

        // 6. Throw Keyword Example
        try {
            throw new ArithmeticException("Manually thrown exception");
        } catch (ArithmeticException e) {
            System.out.println(e.getMessage());
        }

        // 7. Custom Exception Example
        try {
            throw new MyException("This is a custom exception!");
        } catch (MyException e) {
            System.out.println(e.getMessage());
        }

        // 8. StackOverflowError Example
        recursiveMethod(); 
        
    }
}

------------------------------------------------------------------

Multithresding :
1. Thread Class 2. Runnable Interface
public synchronized void increment() {} // synchronized keyword avoids race condition for method
wait() makes a thread pause execution until another thread calls notify().notify() wakes up the waiting thread.
A deadlock happens when two or more threads wait forever because each is holding a resource the other needs. Solution : 1. Lock Resources in the Same Order 2. tryLock()
Thread Pool is a collection of pre-created reusable threads that execute tasks efficiently without creating new threads each time


Key Takeaways :

Thread Creation: Extend Thread or implement Runnable.
// Method 1: Extend Thread class
class MyThread extends Thread {
    public void run() {
        System.out.println("Thread running: " + Thread.currentThread().getName());
    }
}

// Method 2: Implement Runnable
class MyRunnable implements Runnable {
    public void run() {
        System.out.println("Runnable running: " + Thread.currentThread().getName());
    }
}

public class Main {
    public static void main(String[] args) {
        // Start Thread
        MyThread t1 = new MyThread();
        t1.start();

        // Start Runnable
        Thread t2 = new Thread(new MyRunnable());
        t2.start();
    }
}

Synchronization: Use synchronized methods/blocks or ReentrantLock.
class Counter {
    private int count = 0;
    
    // Synchronized method
    public synchronized void increment() {
        count++;
    }
    
    // Synchronized block
    public void decrement() {
        synchronized(this) {
            count--;
        }
    }
    
    public int getCount() { return count; }
}

public class Main {
    public static void main(String[] args) throws InterruptedException {
        Counter counter = new Counter();
        
        Thread t1 = new Thread(() -> {
            for (int i = 0; i < 1000; i++) counter.increment();
        });
        
        Thread t2 = new Thread(() -> {
            for (int i = 0; i < 1000; i++) counter.decrement();
        });
        
        t1.start();
        t2.start();
        t1.join();
        t2.join();
        
        System.out.println("Final count: " + counter.getCount()); // Should be 0
    }
}

Wait/Notify: For producer-consumer scenarios.
import java.util.LinkedList;
import java.util.Queue;

class Buffer {
    private Queue<Integer> queue = new LinkedList<>();
    private int capacity = 5;
    
    public synchronized void produce(int item) throws InterruptedException {
        while (queue.size() == capacity) {
            wait(); // Wait if full
        }
        queue.add(item);
        System.out.println("Produced: " + item);
        notify(); // Notify consumer
    }
    
    public synchronized void consume() throws InterruptedException {
        while (queue.isEmpty()) {
            wait(); // Wait if empty
        }
        int item = queue.poll();
        System.out.println("Consumed: " + item);
        notify(); // Notify producer
    }
}

public class Main {
    public static void main(String[] args) {
        Buffer buffer = new Buffer();
        
        Thread producer = new Thread(() -> {
            try {
                for (int i = 1; i <= 10; i++) buffer.produce(i);
            } catch (InterruptedException e) { e.printStackTrace(); }
        });
        
        Thread consumer = new Thread(() -> {
            try {
                for (int i = 1; i <= 10; i++) buffer.consume();
            } catch (InterruptedException e) { e.printStackTrace(); }
        });
        
        producer.start();
        consumer.start();
    }
}

Thread Pools: Manage threads efficiently with ExecutorService.
import java.util.concurrent.ExecutorService;
import java.util.concurrent.Executors;

public class Main {
    public static void main(String[] args) {
        ExecutorService executor = Executors.newFixedThreadPool(3);
        
        for (int i = 1; i <= 5; i++) {
            int taskId = i;
            executor.submit(() -> {
                System.out.println("Task " + taskId + " running in " + Thread.currentThread().getName());
            });
        }
        
        executor.shutdown();
    }
}

Atomic Operations: AtomicInteger, AtomicReference for lock-free code.
import java.util.concurrent.atomic.AtomicInteger;

public class Main {
    public static void main(String[] args) throws InterruptedException {
        AtomicInteger counter = new AtomicInteger(0);
        
        Thread t1 = new Thread(() -> {
            for (int i = 0; i < 1000; i++) counter.incrementAndGet();
        });
        
        Thread t2 = new Thread(() -> {
            for (int i = 0; i < 1000; i++) counter.decrementAndGet();
        });
        
        t1.start();
        t2.start();
        t1.join();
        t2.join();
        
        System.out.println("Final count: " + counter.get()); // Should be 0
    }
}

Deadlock Prevention: Always acquire locks in the same order.
public class Main {
    static Object lock1 = new Object();
    static Object lock2 = new Object();
    
    public static void main(String[] args) {
        // Thread 1 (Causes deadlock)
        Thread t1 = new Thread(() -> {
            synchronized(lock1) {
                System.out.println("Thread 1: Holding lock1");
                try { Thread.sleep(100); } catch (Exception e) {}
                synchronized(lock2) {
                    System.out.println("Thread 1: Holding lock1 & lock2");
                }
            }
        });
        
        // Thread 2 (Fixed by acquiring locks in same order)
        Thread t2 = new Thread(() -> {
            synchronized(lock1) {  // Changed to lock1 first
                System.out.println("Thread 2: Holding lock1");
                try { Thread.sleep(100); } catch (Exception e) {}
                synchronized(lock2) {
                    System.out.println("Thread 2: Holding lock1 & lock2");
                }
            }
        });
        
        t1.start();
        t2.start();
    }
}

ReentrantLock (Alternative to Synchronized).
import java.util.concurrent.locks.ReentrantLock;

class Counter {
    private int count = 0;
    private ReentrantLock lock = new ReentrantLock();
    
    public void increment() {
        lock.lock();
        try {
            count++;
        } finally {
            lock.unlock();
        }
    }
}

public class Main {
    public static void main(String[] args) throws InterruptedException {
        Counter counter = new Counter();
        
        Thread t1 = new Thread(() -> {
            for (int i = 0; i < 1000; i++) counter.increment();
        });
        
        Thread t2 = new Thread(() -> {
            for (int i = 0; i < 1000; i++) counter.increment();
        });
        
        t1.start();
        t2.start();
        t1.join();
        t2.join();
        
        System.out.println("Final count: " + counter.getCount()); // Should be 2000
    }
}


-------------------------------------------------------------------

Custom Sorting :

Sorting a List :
import java.util.*;

public class Main {
    public static void main(String[] args) {
        List<Integer> numbers = Arrays.asList(5, 2, 9, 1, 5);
        
        // Ascending order (natural)
        numbers.sort((a, b) -> a - b);
        System.out.println("Ascending: " + numbers); // [1, 2, 5, 5, 9]
        
        // Descending order
        numbers.sort((a, b) -> b - a);
        System.out.println("Descending: " + numbers); // [9, 5, 5, 2, 1]
    }
}

Sorting a List of Objects :
import java.util.*;

class Person {
    String name;
    int age;
    Person(String name, int age) { this.name = name; this.age = age; }
    public String toString() { return name + "(" + age + ")"; }
}

public class Main {
    public static void main(String[] args) {
        List<Person> people = Arrays.asList(
            new Person("Alice", 25),
            new Person("Bob", 20),
            new Person("Charlie", 30)
        );
        
        // Sort by age (ascending)
        people.sort((p1, p2) -> p1.age - p2.age);
        System.out.println("By age: " + people); // [Bob(20), Alice(25), Charlie(30)]
        
        // Sort by name length
        people.sort((p1, p2) -> p1.name.length() - p2.name.length();
        System.out.println("By name length: " + people); // [Bob(20), Alice(25), Charlie(30)]
    }
}

Custom Sorting in a Set :
import java.util.*;

public class Main {
    public static void main(String[] args) {
        // TreeSet with custom sorting (descending)
        Set<Integer> set = new TreeSet<>((a, b) -> b - a);
        set.add(5);
        set.add(2);
        set.add(9);
        System.out.println("Custom Sorted Set: " + set); // [9, 5, 2]
    }
}

Priority Queue with Custom Sorting :
import java.util.*;

public class Main {
    public static void main(String[] args) {
        // Min-heap (default)
        PriorityQueue<Integer> minHeap = new PriorityQueue<>();
        minHeap.add(5);
        minHeap.add(2);
        minHeap.add(9);
        System.out.println("Min-Heap: " + minHeap.poll()); // 2
        
        // Max-heap (custom)
        PriorityQueue<Integer> maxHeap = new PriorityQueue<>((a, b) -> b - a);
        maxHeap.add(5);
        maxHeap.add(2);
        maxHeap.add(9);
        System.out.println("Max-Heap: " + maxHeap.poll()); // 9
        
        // PriorityQueue of arrays (sort by 2nd element)
        PriorityQueue<int[]> pq = new PriorityQueue<>((a, b) -> a[1] - b[1]);
        pq.add(new int[]{1, 5});
        pq.add(new int[]{2, 3});
        pq.add(new int[]{3, 7});
        System.out.println("Array PQ: " + Arrays.toString(pq.poll())); // [2, 3]
    }
}

Sorting a Map by Key/Value :
import java.util.*;
import java.util.stream.*;

public class Main {
    public static void main(String[] args) {
        Map<String, Integer> map = new HashMap<>();
        map.put("Alice", 25);
        map.put("Bob", 20);
        map.put("Charlie", 30);
        
        // Sort by key (name)
        Map<String, Integer> sortedByName = map.entrySet().stream()
            .sorted((e1, e2) -> e1.getKey().compareTo(e2.getKey()))
            .collect(Collectors.toMap(
                Map.Entry::getKey,
                Map.Entry::getValue,
                (a, b) -> a,
                LinkedHashMap::new
            ));
        System.out.println("Sorted by name: " + sortedByName); // {Alice=25, Bob=20, Charlie=30}
        
        // Sort by value (age)
        Map<String, Integer> sortedByAge = map.entrySet().stream()
            .sorted((e1, e2) -> e1.getValue() - e2.getValue())
            .collect(Collectors.toMap(
                Map.Entry::getKey,
                Map.Entry::getValue,
                (a, b) -> a,
                LinkedHashMap::new
            ));
        System.out.println("Sorted by age: " + sortedByAge); // {Bob=20, Alice=25, Charlie=30}
    }
}

Reverse Order Comparator :
import java.util.*;

public class Main {
    public static void main(String[] args) {
        List<Integer> numbers = Arrays.asList(5, 2, 9, 1);
        
        // Using Collections.reverseOrder()
        numbers.sort(Collections.reverseOrder());
        System.out.println("Reverse order: " + numbers); // [9, 5, 2, 1]
        
        // Using lambda
        numbers.sort((a, b) -> b.compareTo(a));
        System.out.println("Reverse lambda: " + numbers); // [9, 5, 2, 1]
    }
}

Sorting a List<int[]> (Multiple Columns) :
import java.util.*;

public class Main {
    public static void main(String[] args) {
        List<int[]> list = new ArrayList<>();
        list.add(new int[]{3, 20});
        list.add(new int[]{1, 30});
        list.add(new int[]{1, 10});
        list.add(new int[]{2, 15});

        // Sort by 1st column (asc), then 2nd column (desc)
        list.sort((a, b) -> {
            if (a[0] != b[0]) {
                return a[0] - b[0]; // 1st column ascending
            } else {
                return b[1] - a[1]; // 2nd column descending
            }
        });

        // Print sorted list
        for (int[] arr : list) {
            System.out.println(Arrays.toString(arr));
        }
        /* Output:
           [1, 30]
           [1, 10]
           [2, 15]
           [3, 20]
        */
    }
}

Sorting a List<String[]> (Multiple Columns) :
import java.util.*;

public class Main {
    public static void main(String[] args) {
        List<String[]> list = new ArrayList<>();
        list.add(new String[]{"Bob", "25"});
        list.add(new String[]{"Alice", "30"});
        list.add(new String[]{"Alice", "20"});

        // Sort by name (asc), then age (desc)
        list.sort((a, b) -> {
            int nameCompare = a[0].compareTo(b[0]);
            if (nameCompare != 0) {
                return nameCompare;
            } else {
                return Integer.compare(Integer.parseInt(b[1]), Integer.parseInt(a[1]));
            }
        });

        // Print sorted list
        for (String[] arr : list) {
            System.out.println(Arrays.toString(arr));
        }
        /* Output:
           [Alice, 30]
           [Alice, 20]
           [Bob, 25]
        */
    }
}

PriorityQueue of Arrays (Custom Multi-Column Order) :
import java.util.*;

public class Main {
    public static void main(String[] args) {
        // Max-Heap by 1st column, Min-Heap by 2nd column
        PriorityQueue<int[]> pq = new PriorityQueue<>((a, b) -> {
            if (a[0] != b[0]) {
                return b[0] - a[0]; // 1st column (descending)
            } else {
                return a[1] - b[1];  // 2nd column (ascending)
            }
        });

        pq.add(new int[]{3, 20});
        pq.add(new int[]{1, 30});
        pq.add(new int[]{1, 10});
        pq.add(new int[]{2, 15});

        while (!pq.isEmpty()) {
            System.out.println(Arrays.toString(pq.poll()));
        }
        /* Output:
           [3, 20]
           [2, 15]
           [1, 10]
           [1, 30]
        */
    }
}


-------------------------------------------------------------------

Access Modifiers (Control Visibility)
public → Accessible from anywhere in the program.
protected → Accessible within the same package and subclasses.
private → Accessible only within the same class.
(default / package-private) → Accessible only within the same package (no keyword needed).

Non-Access Modifiers (Modify Behavior)
static → Belongs to the class rather than an instance.
final → Used for constants, preventing inheritance (class), and preventing method overriding.
abstract → Used in abstract classes and methods without a body.
synchronized → Used in multithreading to allow only one thread at a time.
volatile → Ensures visibility of shared variables in multithreading.
transient → Prevents a field from being serialized.
strictfp → Ensures floating-point calculations follow IEEE precision rules.
native → Used to call platform-specific (C/C++) code.

------------------------------------------------------------------

Indentations :
int age = 25; 
------------------------------------------------------------------
int x = 10, y = 20, z = 30;
------------------------------------------------------------------
public class Example {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
------------------------------------------------------------------
for (int i = 0; i < 10; i++) {  
    System.out.println("Iteration: " + i);
}
------------------------------------------------------------------
if (x > 10) {
    System.out.println("X is greater than 10");
} else {
    System.out.println("X is 10 or less");
}
------------------------------------------------------------------
printDetails("Ganesh", 25, "India");
------------------------------------------------------------------
try {
    int result = 10 / 0;
} catch (ArithmeticException e) {
    System.out.println("Cannot divide by zero");
}
------------------------------------------------------------------
switch (day) {
    case "Monday":
        System.out.println("Start of the week!");
        break;
    case "Friday":
        System.out.println("Weekend is near!");
        break;
    default:
        System.out.println("Just another day!");
}
------------------------------------------------------------------
public class Person {
    private String name;
    
    public Person(String name) {
        this.name = name;
    }
    
    public void display() {
        System.out.println("Name: " + name);
    }
}
------------------------------------------------------------------
public int getValue() {
    return 100;
}
------------------------------------------------------------------
for (int i = 0; i < 5; i++) {
    if (i % 2 == 0) {
        System.out.println(i + " is even");
    }
}
------------------------------------------------------------------
// This is a single-line comment

/*
 * This is a 
 * properly formatted multi-line comment.
 */
------------------------------------------------------------------


Order of Elements in a Java Class :
Package Statement
Import Statements
Class Declaration
Constants (static final)
Instance Variables (private first, then protected, then public)
Constructors
Methods (ordered logically)
Static methods first
Instance methods next
Private helper methods last
Override toString(), equals(), hashCode() (if needed)
Inner Classes (if any)
------------------------------------------------------------------
A class can extend only one parent class (extends). (Single Inheritance)
A class can implement multiple interfaces (implements).
If the class needs to declare exceptions, use throws in method signatures.
public class ClassName extends ParentClass implements Interface1, Interface2 {
    // Class body
}
------------------------------------------------------------------
Order of variables in a class:
Constants (static final)
Static variables (static)
Instance variables (private → protected → public)
------------------------------------------------------------------
Correct Order of Methods:
Static Methods (Public → Private)
Instance Methods (Public → Protected → Private)
Override Methods (toString(), equals(), hashCode() last)
Private helper methods last
------------------------------------------------------------------
extends must come before implements.
Only one class can be extended, but multiple interfaces can be implemented.
If implementing multiple interfaces, separate them with commas.
public class Developer extends Employee implements Coder, Tester {
    // Class body
}
------------------------------------------------------------------
If a method might throw an exception, declare it using throws.
throws must come before the method body.
public void readFile(String fileName) throws IOException {
    // File reading logic
}

------------------------------------------------------------------
Final classes cannot be extended.
Final methods cannot be overridden.
public final class Utility {
    public static void printMessage() {
        System.out.println("Hello!");
    }
}
------------------------------------------------------------------
If your class has an inner class, keep it at the bottom of the outer class.
public class OuterClass {
    private int data = 10;

    // Inner class
    class InnerClass {
        void display() {
            System.out.println("Data: " + data);
        }
    }
}
------------------------------------------------------------------
Only method signatures (no implementation).
All methods are implicitly public abstract.
All variables are implicitly public static final
public interface Vehicle {
    int MAX_SPEED = 120; // Implicitly public static final
    void start(); // Implicitly public abstract
}
------------------------------------------------------------------
Enum constants should be UPPER_CASE.
Keep methods at the bottom.
public enum Color {
    RED, GREEN, BLUE;

    public void display() {
        System.out.println("Color: " + this);
    }
}
------------------------------------------------------------------


Order for Declaring Variables in a Class:
Constants (static final):
All static final constants should be at the top.
They are usually written in UPPER_CASE with underscores (_) separating words.
Example: public static final int MAX_COUNT = 100;
Static Variables (static):
Static variables (class-level variables) should come below constants.
Example: private static int counter = 0;
Instance Variables (Non-static):
These are variables that belong to an object (not shared across instances).
Order (general rule):
Primitive types → Immutable objects (String) → Collections (Lists, Maps, Sets, Arrays, etc.) → Reference types (custom objects).
Access modifiers order:
Private → Protected → Public (Encapsulation principle)
public class Example {

    // Constants (static final)
    public static final int MAX_USERS = 1000;
    private static final String APP_NAME = "MyApp";

    // Static Variables (shared across instances)
    private static int totalUsers;
    protected static double appVersion = 1.0;

    // Instance Variables (Non-static)
    
    // Primitives (organized in size order)
    private boolean isActive;
    private byte status;
    private short shortNumber;
    private int userId;
    private long bigNumber;
    private float piValue;
    private double balance;

    // Immutable objects (`String`, `UUID`, etc.)
    private String name;
    private UUID userUUID;

    // Collections (ordered by usage frequency)
    private List<String> messages;
    private Set<Integer> uniqueIds;
    private Map<String, Integer> scores;

    // Custom objects (Reference types)
    private Address address;
    private User friend;

    // Constructor(s)
    public Example(String name, int userId) {
        this.name = name;
        this.userId = userId;
    }

    // Methods...
}
------------------------------------------------------------------
If multiple variables are logically related, group them together inside their category.
public class Account {
    private int accountId;
    private double balance;

    private String accountHolder;
    private String bankName;
}
------------------------------------------------------------------
private int age;
private int salary;
private double balance;

Good Practice: Declare each variable on a separate line for clarity.
Avoid: Declaring multiple variables of different types on the same line.
------------------------------------------------------------------
Local variables inside methods should follow a similar order
public void process() {
    int count = 0;   // Primitive first
    String name = "Ganesh";
    List<Integer> ids = new ArrayList<>();
    Address address = new Address();
}
------------------------------------------------------------------


observations :
add(int index, E element) // it can add elements upto size of collection
indexOf(Object o) lastIndexOf(Object o) // returns -1 if not found
Vector and Stack are similar to ArrayList but are synchronized, making them slower for concurrent access.
HashSet are unordered, meaning the iteration order is not guaranteed. However, LinkedHashSet maintains the insertion order, and TreeSet orders elements based on their natural ordering or a provided comparator.
ArrayDeque is typically faster than LinkedList for most operations because of its underlying array-based structure.
Insertion/removal operations are O(1) for both ends, but resizing an array (for ArrayDeque) can be costly.
A map does not allow duplicate keys. If you try to insert a duplicate key, the value associated with the key is updated instead.
HashMap allows one null key and multiple null values.
TreeMap does not allow null keys but can have null values, depending on the comparator used.
Hashtable does not allow null keys or values.
Most collection implementations are not thread-safe. For thread-safe operations, you need to use Collections.synchronizedList(), Collections.synchronizedSet(), or use thread-safe implementations like ConcurrentHashMap.
Modifying a collection while iterating over it (except via Iterator.remove()) can lead to ConcurrentModificationException.
iterator() : if the list is modified while iterating (except through the iterator itself), it will throw a ConcurrentModificationException and Can only iterate in one direction (forward).
You can use previous() to move backward and next() to move forward.
It supports add(), remove(), and set() methods while iterating
Default Values of Generic Data Types: Reference types (Objects, Classes):default value is null.

Primitive wrapper types (Integer, Double, Boolean, etc.):Default value is also null because they are objects.
Primitive types (int, double, boolean, etc.):Generics do not directly support primitives, but when using wrappers (Integer, Double), they default to null.

Integer.MAX_VALUE
Integer.MIN_VALUE


```


# Java Interview Cheat Sheet

## 📌 Core Java

### OOP Concepts
1. **Class**: Blueprint for creating objects
2. **Object**: Instance of a class
3. **Inheritance**: "is-a" relationship between classes
4. **Polymorphism**: Same method name with different implementations
5. **Encapsulation**: Data hiding using access modifiers
6. **Abstraction**: Showing essential features only
7. **Coupling**: Degree of dependency between classes
8. **Cohesion**: How well a class does a single task
9. **Association**: Relationship between objects
10. **Aggregation**: "Has-a" relationship (weak ownership)
11. **Composition**: "Has-a" relationship (strong ownership)

### Keywords
12. **this**: Refers to current object
13. **super**: Refers to parent class
14. **static**: Belongs to class rather than instance
15. **final**: Prevents modification/extension/override
16. **abstract**: Cannot be instantiated
17. **transient**: Excludes field from serialization
18. **volatile**: Ensures visibility across threads
19. **synchronized**: Thread-safe access
20. **native**: Platform-dependent implementation
21. **strictfp**: Consistent floating-point across platforms

### Methods
22. **Method Overloading**: Same name, different parameters
23. **Method Overriding**: Redefining parent class method
24. **Constructor**: Special method for object initialization
25. **Default Constructor**: Added by compiler if none exists
26. **Parameterized Constructor**: Takes arguments
27. **Copy Constructor**: Creates object from another object
28. **Getter/Setter**: Access/modify private fields
29. **Varargs**: Variable-length arguments (String...)
30. **Recursion**: Method calling itself

## 📌 Data Types

### Primitive Types
31. **byte**: 8-bit integer (-128 to 127)
32. **short**: 16-bit integer (-32,768 to 32,767)
33. **int**: 32-bit integer (-2^31 to 2^31-1)
34. **long**: 64-bit integer (-2^63 to 2^63-1)
35. **float**: 32-bit floating point
36. **double**: 64-bit floating point
37. **char**: 16-bit Unicode character
38. **boolean**: true/false values

### Wrapper Classes
39. **Byte**: Wrapper for byte
40. **Short**: Wrapper for short
41. **Integer**: Wrapper for int
42. **Long**: Wrapper for long
43. **Float**: Wrapper for float
44. **Double**: Wrapper for double
45. **Character**: Wrapper for char
46. **Boolean**: Wrapper for boolean
47. **Autoboxing**: Primitive → Wrapper conversion
48. **Unboxing**: Wrapper → Primitive conversion

### Type Conversion
49. **Widening**: Automatic (byte → short → int → long)
50. **Narrowing**: Manual casting required (long → int)
51. **Type Casting**: (int) 3.14 → 3

## 📌 Strings
52. **String**: Immutable sequence of chars
53. **String Pool**: Heap memory for string literals
54. **StringBuffer**: Mutable, thread-safe
55. **StringBuilder**: Mutable, not thread-safe
56. **charAt()**: Get character at index
57. **concat()**: Concatenate strings
58. **equals()**: Compare content
59. **==**: Compare references
60. **compareTo()**: Lexicographical comparison
61. **substring()**: Extract portion of string
62. **toUpperCase()/toLowerCase()**: Case conversion
63. **trim()**: Remove leading/trailing spaces
64. **replace()**: Replace characters
65. **split()**: Split string by regex
66. **intern()**: Add to string pool
67. **format()**: Format string
68. **valueOf()**: Convert to string

## 📌 Exception Handling
69. **Throwable**: Superclass of all errors/exceptions
70. **Error**: Unrecoverable (OutOfMemoryError)
71. **Exception**: Recoverable (IOException)
72. **Checked Exception**: Compile-time check
73. **Unchecked Exception**: RuntimeException
74. **try-catch-finally**: Exception handling
75. **throw**: Explicitly throw exception
76. **throws**: Declare possible exceptions
77. **Custom Exception**: User-defined exception
78. **try-with-resources**: Auto-close resources
79. **Multi-catch**: Catch multiple exceptions
80. **Suppressed Exceptions**: In try-with-resources

## 📌 Collections Framework
### Core Interfaces
81. **Collection**: Root interface
82. **List**: Ordered collection (duplicates allowed)
83. **Set**: Unique elements
84. **Queue**: FIFO ordering
85. **Deque**: Double-ended queue
86. **Map**: Key-value pairs
87. **SortedSet**: Ordered set
88. **SortedMap**: Ordered map

### List Implementations
89. **ArrayList**: Resizable array
90. **LinkedList**: Doubly-linked list
91. **Vector**: Thread-safe array
92. **Stack**: LIFO structure

### Set Implementations
93. **HashSet**: Hash table implementation
94. **LinkedHashSet**: Maintains insertion order
95. **TreeSet**: Red-Black tree implementation
96. **EnumSet**: For enum types

### Map Implementations
97. **HashMap**: Hash table implementation
98. **LinkedHashMap**: Maintains insertion order
99. **TreeMap**: Red-Black tree implementation
100. **Hashtable**: Legacy thread-safe map
101. **IdentityHashMap**: Uses == for comparison
102. **WeakHashMap**: Weak references for keys
103. **EnumMap**: Optimized for enum keys

### Queue Implementations
104. **PriorityQueue**: Priority-based ordering
105. **ArrayDeque**: Resizable array deque
106. **BlockingQueue**: Thread-safe queue
107. **ArrayBlockingQueue**: Bounded blocking queue
108. **LinkedBlockingQueue**: Optionally-bounded queue
109. **PriorityBlockingQueue**: Unbounded priority queue
110. **DelayQueue**: Time-based scheduling
111. **SynchronousQueue**: Handoff mechanism

### Utility Classes
112. **Collections**: Utility methods
113. **Arrays**: Array utilities
114. **Comparator**: Custom ordering
115. **Comparable**: Natural ordering
116. **Iterator**: Traverse collections
117. **ListIterator**: Bidirectional iterator
118. **Spliterator**: Parallel traversal

## 📌 Generics
119. **Type Parameter**: <T> in class/method
120. **Generic Class**: Class<T> { ... }
121. **Generic Method**: <T> void method(T t) { ... }
122. **Bounded Type**: <T extends Number>
123. **Wildcard**: <?>
124. **Upper Bounded**: <? extends Number>
125. **Lower Bounded**: <? super Integer>
126. **Type Erasure**: Compile-time type safety
127. **Reifiable Types**: Retain type at runtime
128. **Heap Pollution**: Mixing raw and generic types

## 📌 Multithreading
### Thread Basics
129. **Thread**: Lightweight process
130. **Runnable**: Functional interface for threads
131. **Thread Class**: Extend to create thread
132. **Thread States**: NEW, RUNNABLE, BLOCKED, WAITING, TIMED_WAITING, TERMINATED
133. **Daemon Thread**: Background thread
134. **Thread Priority**: 1 (MIN) to 10 (MAX)
135. **Thread Group**: Group of threads

### Thread Operations
136. **start()**: Begin execution
137. **run()**: Contains thread logic
138. **sleep()**: Pause execution
139. **yield()**: Hint to scheduler
140. **join()**: Wait for thread completion
141. **interrupt()**: Request termination
142. **isInterrupted()**: Check interrupt status
143. **interrupted()**: Check & clear interrupt

### Synchronization
144. **Race Condition**: Unpredictable behavior
145. **Critical Section**: Code needing protection
146. **Monitor**: Synchronization mechanism
147. **synchronized**: Method/block level locking
148. **Intrinsic Lock**: Monitor lock
149. **ReentrantLock**: Explicit lock
150. **ReadWriteLock**: Separate read/write locks
151. **StampedLock**: Optimistic locking
152. **Deadlock**: Circular wait condition
153. **Livelock**: Threads keep changing state
154. **Starvation**: Thread gets no CPU time

### Concurrent Utilities
155. **Executor**: Executes tasks
156. **ExecutorService**: Manages thread pool
157. **ThreadPoolExecutor**: Configurable pool
158. **ScheduledExecutorService**: Delayed/periodic tasks
159. **Future**: Result of async computation
160. **Callable**: Returns result
161. **CompletableFuture**: Asynchronous programming
162. **ForkJoinPool**: Work-stealing pool
163. **CountDownLatch**: One-time synchronization
164. **CyclicBarrier**: Reusable synchronization
165. **Phaser**: Flexible synchronization
166. **Semaphore**: Controls resource access
167. **Exchanger**: Thread data exchange
168. **BlockingQueue**: Thread-safe queue

### Atomic Operations
169. **AtomicInteger**: Thread-safe int
170. **AtomicLong**: Thread-safe long
171. **AtomicBoolean**: Thread-safe boolean
172. **AtomicReference**: Thread-safe reference
173. **AtomicArray**: Thread-safe array
174. **AtomicFieldUpdater**: Atomic field updates
175. **CAS**: Compare-And-Swap operation
176. **ABA Problem**: CAS limitation

## 📌 Java 8 Features
### Lambda Expressions
177. **Lambda**: Anonymous function
178. **Functional Interface**: Single abstract method
179. **Predicate**: boolean test(T t)
180. **Function**: R apply(T t)
181. **Consumer**: void accept(T t)
182. **Supplier**: T get()
183. **UnaryOperator**: T apply(T t)
184. **BinaryOperator**: T apply(T t1, T t2)

### Stream API
185. **Stream**: Sequence of elements
186. **Intermediate Ops**: filter, map, etc.
187. **Terminal Ops**: collect, forEach, etc.
188. **filter()**: Select elements
189. **map()**: Transform elements
190. **flatMap()**: Flatten streams
191. **distinct()**: Remove duplicates
192. **sorted()**: Order elements
193. **peek()**: Debug stream
194. **limit()**: Truncate stream
195. **skip()**: Skip elements
196. **forEach()**: Iterate elements
197. **toArray()**: Convert to array
198. **reduce()**: Aggregate elements
199. **collect()**: Mutable reduction
200. **min()/max()**: Find extremes
201. **count()**: Count elements
202. **anyMatch()/allMatch()/noneMatch()**: Predicate matching
203. **findFirst()/findAny()**: Find elements
204. **parallelStream()**: Parallel processing

### Date/Time API
205. **LocalDate**: Date without time
206. **LocalTime**: Time without date
207. **LocalDateTime**: Date and time
208. **ZonedDateTime**: With timezone
209. **Instant**: Machine timestamp
210. **Duration**: Time-based amount
211. **Period**: Date-based amount
212. **DateTimeFormatter**: Format dates

### Other Java 8 Features
213. **Optional**: Avoid null checks
214. **Default Methods**: Interface implementations
215. **Static Methods in Interfaces**: Utility methods
216. **Method References**: Shorthand for lambdas
217. **Nashorn**: JavaScript engine
218. **Type Annotations**: More annotation places
219. **Repeatable Annotations**: Multiple same annotations

## 📌 Java I/O
### Byte Streams
220. **InputStream**: Abstract byte input
221. **OutputStream**: Abstract byte output
222. **FileInputStream**: Read from file
223. **FileOutputStream**: Write to file
224. **ByteArrayInputStream**: Read from byte array
225. **ByteArrayOutputStream**: Write to byte array
226. **BufferedInputStream**: Buffered input
227. **BufferedOutputStream**: Buffered output
228. **DataInputStream**: Read primitives
229. **DataOutputStream**: Write primitives
230. **ObjectInputStream**: Read objects
231. **ObjectOutputStream**: Write objects
232. **PrintStream**: Formatted output

### Character Streams
233. **Reader**: Abstract char input
234. **Writer**: Abstract char output
235. **FileReader**: Read from file
236. **FileWriter**: Write to file
237. **CharArrayReader**: Read from char array
238. **CharArrayWriter**: Write to char array
239. **BufferedReader**: Buffered input
240. **BufferedWriter**: Buffered output
241. **InputStreamReader**: Byte to char
242. **OutputStreamWriter**: Char to byte
243. **PrintWriter**: Formatted output

### NIO
244. **Path**: File/directory location
245. **Files**: File operations
246. **FileSystem**: Access to filesystem
247. **FileStore**: Storage device
248. **WatchService**: File change notifications
249. **Channels**: I/O connections
250. **Buffers**: Data containers
251. **Charset**: Character encoding
252. **Selector**: Multiplexed I/O

## 📌 JDBC
253. **DriverManager**: Manages drivers
254. **Connection**: Database session
255. **Statement**: Execute SQL
256. **PreparedStatement**: Parameterized SQL
257. **CallableStatement**: Stored procedures
258. **ResultSet**: Query results
259. **DatabaseMetaData**: Database info
260. **ResultSetMetaData**: ResultSet info
261. **RowSet**: Disconnected ResultSet
262. **JdbcRowSet**: Connected RowSet
263. **CachedRowSet**: Disconnected RowSet
264. **Batch Processing**: Multiple statements
265. **Transaction**: ACID operations
266. **Savepoint**: Partial rollback
267. **DataSource**: Preferred connection method
268. **Connection Pooling**: Reuse connections

## 📌 Memory Management
269. **Heap**: Object storage
270. **Stack**: Method calls/local vars
271. **Method Area**: Class metadata
272. **PC Register**: Thread execution point
273. **Native Method Stack**: Native code
274. **Young Gen**: New objects
275. **Eden Space**: Initial allocation
276. **Survivor Space**: Surviving objects
277. **Old Gen**: Long-lived objects
278. **Perm Gen**: Class metadata (pre-Java 8)
279. **Metaspace**: Class metadata (Java 8+)
280. **Garbage Collection**: Memory reclamation
281. **Minor GC**: Young gen collection
282. **Major GC**: Old gen collection
283. **Full GC**: Entire heap collection
284. **Mark-Sweep**: Basic GC algorithm
285. **Mark-Compact**: Reduce fragmentation
286. **Copying**: Between survivor spaces
287. **Generational**: Different algorithms per gen
288. **Serial GC**: Single-threaded
289. **Parallel GC**: Multi-threaded
290. **CMS**: Concurrent Mark-Sweep
291. **G1**: Garbage-First collector
292. **ZGC**: Scalable low-latency
293. **Shenandoah**: Concurrent GC
294. **Reference Types**: Strong, Soft, Weak, Phantom
295. **Finalization**: Cleanup before GC
296. **Memory Leak**: Unintentional retention

## 📌 Design Patterns
### Creational
297. **Singleton**: Single instance
298. **Factory**: Create objects
299. **Abstract Factory**: Families of objects
300. **Builder**: Complex object construction
301. **Prototype**: Clone objects

### Structural
302. **Adapter**: Convert interface
303. **Bridge**: Decouple abstraction
304. **Composite**: Tree structures
305. **Decorator**: Add responsibilities
306. **Facade**: Simplified interface
307. **Flyweight**: Share objects
308. **Proxy**: Control access

### Behavioral
309. **Chain of Responsibility**: Pass requests
310. **Command**: Encapsulate request
311. **Interpreter**: Language interpretation
312. **Iterator**: Traverse collection
313. **Mediator**: Centralized communication
314. **Memento**: Capture/restore state
315. **Observer**: Publish-subscribe
316. **State**: Change behavior with state
317. **Strategy**: Encapsulate algorithm
318. **Template Method**: Algorithm skeleton
319. **Visitor**: Add operations

## 📌 JVM Internals
320. **Classloader**: Loads classes
321. **Bootstrap**: Loads core classes
322. **Extension**: Loads extension classes
323. **System**: Loads application classes
324. **Bytecode**: JVM instructions
325. **JIT**: Just-In-Time compilation
326. **HotSpot**: Oracle's JVM
327. **Method Area**: Class structures
328. **Heap**: Object storage
329. **Stack**: Thread execution
330. **PC Register**: Thread position
331. **Native Stack**: Native calls
332. **Verifier**: Checks bytecode
333. **Interpreter**: Executes bytecode
334. **Profiler**: Performance analysis
335. **Debugger**: Debug support

## 📌 Java 9-17 Features
### Java 9
336. **Module System**: Jigsaw project
337. **JShell**: REPL tool
338. **Factory Methods**: Collections.of()
339. **Private Methods**: In interfaces
340. **HTTP/2 Client**: New HTTP API
341. **Multi-Release JARs**: Versioned classes

### Java 10
342. **var**: Local variable inference
343. **Garbage-Collector Interface**: Clean GC code

### Java 11
344. **HTTP Client**: Standardized
345. **Local-Variable Syntax**: for lambdas
346. **Epsilon GC**: No-op collector
347. **Flight Recorder**: Production profiling

### Java 12-17
348. **Switch Expressions**: Simplified switch
349. **Text Blocks**: Multiline strings
350. **Records**: Data carriers
351. **Sealed Classes**: Restricted inheritance
352. **Pattern Matching**: instanceof + cast
353. **Foreign Function API**: Native interop

## 📌 Advanced Topics
354. **Reflection**: Runtime class inspection
355. **Annotations**: Metadata
356. **Dynamic Proxy**: Runtime proxy
357. **Bytecode Manipulation**: ASM, Javassist
358. **Class Loading**: Custom loaders
359. **Instrumentation**: Modify classes
360. **Serialization**: Object persistence
361. **Externalization**: Custom serialization
362. **JMX**: Management extensions
363. **JNI**: Native interface
364. **Java Agents**: Runtime modification
365. **ServiceLoader**: Plugin mechanism
366. **Compiler API**: Programmatic compilation
367. **Process API**: Process control
368. **Nashorn**: JavaScript engine
369. **GraalVM**: Polyglot VM
370. **Value Types**: Experimental (Valhalla)

## 📌 Testing
371. **JUnit**: Unit testing
372. **TestNG**: Advanced testing
373. **Mockito**: Mocking framework
374. **PowerMock**: Extended mocking
375. **Hamcrest**: Matchers
376. **AssertJ**: Fluent assertions
377. **JUnit 5**: Modern testing
378. **Parameterized Tests**: Multiple inputs
379. **TDD**: Test-Driven Development
380. **BDD**: Behavior-Driven Development

## 📌 Build Tools
381. **Maven**: Build/dependency mgmt
382. **Gradle**: Flexible builds
383. **Ant**: Legacy build tool
384. **POM**: Maven config
385. **Build Lifecycle**: Maven phases
386. **Dependencies**: Artifact management
387. **Plugins**: Build extensions
388. **Repositories**: Artifact storage

## 📌 Frameworks
### Spring
389. **IoC**: Inversion of Control
390. **DI**: Dependency Injection
391. **AOP**: Aspect-Oriented
392. **Spring MVC**: Web framework
393. **Spring Boot**: Auto-configuration
394. **Spring Data**: Data access
395. **Spring Security**: Auth/authz
396. **Spring Cloud**: Microservices
397. **Bean**: Managed object
398. **ApplicationContext**: Bean factory
399. **Annotation Config**: @Configuration
400. **Component Scan**: Auto-detection

### Hibernate
401. **ORM**: Object-Relational Mapping
402. **Session**: Persistence context
403. **SessionFactory**: Creates sessions
404. **Transaction**: DB transaction
405. **Entity**: Persistent class
406. **HQL**: Hibernate Query Language
407. **Criteria API**: Type-safe queries
408. **Lazy Loading**: On-demand loading
409. **Eager Loading**: Immediate loading
410. **Cache**: First/second level
411. **Dialect**: DB-specific SQL

### Microservices
412. **Service Discovery**: Find services
413. **API Gateway**: Single entry point
414. **Circuit Breaker**: Fault tolerance
415. **Config Server**: Centralized config
416. **Distributed Tracing**: Request tracking
417. **Load Balancing**: Distribute traffic
418. **Feign**: Declarative REST client
419. **Hystrix**: Fault tolerance
420. **Zuul**: API gateway
421. **Eureka**: Service discovery
422. **Ribbon**: Client-side LB
423. **Sleuth**: Distributed tracing
424. **Zipkin**: Trace visualization

## 📌 Web Technologies
425. **Servlet**: Java web component
426. **JSP**: JavaServer Pages
427. **JSF**: JavaServer Faces
428. **JSTL**: JSP tag library
429. **WebSocket**: Full-duplex comm
430. **REST**: Representational State Transfer
431. **SOAP**: Simple Object Access Protocol
432. **JAX-RS**: REST API (Jersey)
433. **JAX-WS**: SOAP API
434. **JSON**: Data interchange
435. **Jackson**: JSON processing
436. **Gson**: Google JSON
437. **JWT**: JSON Web Tokens
438. **OAuth2**: Authorization
439. **OpenID Connect**: Authentication

## 📌 Concurrency Patterns
440. **Thread Pool**: Reusable threads
441. **Executor**: Task execution
442. **Future**: Async result
443. **CompletableFuture**: Async pipeline
444. **Fork-Join**: Divide & conquer
445. **Producer-Consumer**: Work queue
446. **Read-Write Lock**: Concurrent access
447. **Barrier**: Thread synchronization
448. **Double-Checked Locking**: Singleton
449. **Thread Local**: Per-thread storage
450. **Balking**: Skip if busy
451. **Guarded Suspension**: Wait for condition
452. **Scheduler**: Timed execution
453. **Work Stealing**: Balanced load

## 📌 Performance Tuning
454. **Profiling**: Performance analysis
455. **Benchmarking**: Measure performance
456. **JIT Optimizations**: Inlining, etc.
457. **Escape Analysis**: Stack allocation
458. **Memory Leaks**: Unintended retention
459. **GC Tuning**: Heap sizing, etc.
460. **CPU Profiling**: Hot methods
461. **Memory Profiling**: Allocation tracking
462. **Thread Dump**: Thread states
463. **Heap Dump**: Memory snapshot
464. **JVM Flags**: Tuning parameters
465. **Cache**: Reduce computation
466. **Pooling**: Reuse objects
467. **Lazy Init**: Defer creation
468. **Immutable Objects**: Thread-safe
469. **Primitives vs Objects**: Performance
470. **String Concatenation**: Builder better than +

## 📌 Security
471. **JAAS**: Authentication/authorization
472. **JCE**: Crypto operations
473. **JSSE**: SSL/TLS
474. **SASL**: Authentication framework
475. **OAuth**: Delegated auth
476. **JWT**: Secure tokens
477. **CORS**: Cross-origin resource sharing
478. **CSRF**: Cross-site request forgery
479. **XSS**: Cross-site scripting
480. **SQL Injection**: Malicious SQL
481. **Secure Coding**: Best practices
482. **Security Manager**: Access control
483. **Policy Files**: Permissions
484. **KeyStore**: Crypto keys
485. **TrustStore**: Certificates
486. **HTTPS**: Secure HTTP
487. **Certificate Pinning**: Trust specific certs
488. **Password Hashing**: Secure storage
489. **Salt**: Random hash input
490. **PBKDF2**: Password-based key derivation

## 📌 Best Practices
491. **SOLID Principles**: OOP guidelines
492. **DRY**: Don't Repeat Yourself
493. **KISS**: Keep It Simple
494. **YAGNI**: You Ain't Gonna Need It
495. **Clean Code**: Readable/maintainable
496. **Code Smells**: Bad patterns
497. **Refactoring**: Improve design
498. **Unit Testing**: Verify components
499. **Integration Testing**: Verify interactions
500. **CI/CD**: Continuous workflows
501. **Code Reviews**: Quality control
502. **Documentation**: Essential explanations
503. **Logging**: Runtime visibility
504. **Monitoring**: Production visibility
505. **Error Handling**: Graceful failures
506. **Null Checks**: Avoid NPEs
507. **Immutable Objects**: Thread safety
508. **Defensive Copying**: Prevent modification
509. **Fail Fast**: Early validation
510. **Design First**: Plan before coding
