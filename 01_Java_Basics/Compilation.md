# Compilation

Created: 2026/03/25 00:04
Tags: #java #concept

# Definition

DE:
Compilation ist der Prozess, bei dem der Java-Quellcode (.java) vom Compiler in Bytecode (.class) übersetzt wird.

EN:
Compilation is the process in which Java source code (.java) is translated by the compiler into bytecode (.class).

## Why it matters

DE:
Der Java-Compiler heißt javac und ist Teil des JDK.

EN:
The Java compiler is called javac and is part of the JDK.


|              | Compilation    | Execution               |
| ------------ | -------------- | ----------------------- |
| Was passiert | .java → .class | .class → Programm läuft |
| Tool         | javac          | java                    |
| Teil von     | JDK            | JRE                     |
| Ergebnis     | Bytecode<br>   | Maschinencode           |


## Example

Main.java → javac → Main.class (Bytecode)

Nach der Compilation entsteht eine .class-Datei mit Bytecode.

After compilation, a .class file with bytecode is created.

`javac Main.java`
`java Main`
