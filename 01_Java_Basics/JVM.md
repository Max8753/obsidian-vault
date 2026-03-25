2026-03-24 19:38
# Conception
Die JVM (Java Virtual Machine) ist eine virtuelle Maschine, die Java-Bytecode ausführt. Java-Code wird zuerst vom Compiler in Bytecode (.class) übersetzt, und dieser Bytecode wird dann von der JVM ausgeführt.
Concept:
The JVM (Java Virtual Machine) is a virtual machine that runs Java bytecode. Java code is first compiled into bytecode (.class), and then the JVM executes this bytecode.

# Why it matters
- Plattformunabhängigkeit → „Write once, run anywhere“
- Speicherverwaltung (Garbage Collector)
- Sicherheit (kein direkter Speicherzugriff)
- Optimierung zur Laufzeit (JIT-Compiler)
- 
- Platform independence → “Write once, run anywhere”
- Memory management (Garbage Collector)
- Security (no direct memory access)
- Runtime optimization (JIT compiler)

# Example
Process: .java → Compiler (javac) → .class (Bytecode) → JVM → Operating System
