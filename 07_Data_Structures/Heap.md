2026-03-24 20:30
**Heap (Java Memory)**
# Was ist Heap?

DE:
Der Heap ist ein Speicherbereich der JVM, in dem Objekte und Instanzen zur Laufzeit gespeichert werden. Der Heap wird vom Garbage Collector verwaltet.
EN:
The Heap is a memory area of the JVM where objects and instances are stored at runtime. The Heap is managed by the Garbage Collector.

# Was wird im Heap gespeichert?

DE:
Im Heap werden gespeichert:
Objekte
Instanzen von Klassen
Arrays
String-Objekte
EN:
Stored in the Heap:
Objects
Instances of classes
Arrays
String objects
# Beispiel / Example:

`String s = new String("Hello");`
`Person p = new Person();`
`int[] arr = new int[10];`

→ Alle Objekte liegen im Heap.

# Eigenschaften des Heap

- Wird von Garbage Collector bereinigt
- Cleaned by Garbage Collector
- Für Objekte
- For objects
- Groß
- Large
- Langsamer als Stack
- Slower than stack
- Gemeinsamer Speicher (Threads)
- Shared memory (threads)
- Heap Struktur (vereinfacht)
- 
# Structor
Heap
 ├── Young Generation
 │     ├── Eden
 │     └── Survivor
 └── Old Generation
Neue Objekte → Young Generation → Wenn sie lange leben → Old Generation