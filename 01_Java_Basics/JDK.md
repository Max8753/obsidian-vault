2026-03-24 20:24
# Conception

**JDK – Java Development Kit**
DE:
Das JDK (Java Development Kit) ist ein Softwarepaket für die Java-Entwicklung. Es enthält alle Werkzeuge, um Java-Programme zu schreiben, zu kompilieren und auszuführen.
EN:
The JDK (Java Development Kit) is a software package for Java development. It contains all tools needed to write, compile, and run Java programs.
# Struktur des JDK

JDK
 ├── [[JRE]]
 │    ├── [[JVM]]
 │    └── Standard Libraries
 └── Development Tools (javac, java, javadoc, jar ...)
 
JDK = JRE + Tools
DE:
Das JDK besteht aus der JRE und Entwicklerwerkzeugen wie Compiler und Debugger.
EN:
The JDK consists of the JRE and development tools such as the compiler and debugger.
# Komponenten

1. JVM (Java Virtual Machine)
DE: Führt Bytecode aus.
EN: Executes bytecode.
2. JRE (Java Runtime Environment)
DE: Enthält JVM + Standardbibliotheken, um Java-Programme auszuführen.
EN: Contains JVM + standard libraries to run Java programs.
3. Development Tools
# Wichtige Tools:

| javac   | Compiler (.java → .class)                         |
| ------- | ------------------------------------------------- |
| java    | Startet Programm                                  |
| jar     | Erstellt JAR-Dateien                              |
| javadoc | Erstellt Dokumentation<br>Generates documentation |
| jdb     | Debugger                                          |

# Beispiel – Ablauf

Main.java → javac → Main.class → JVM → Programm läuft