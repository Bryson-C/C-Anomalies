### Unknown Languages
#### Here I Will Document Some Strange Laguages I Have Come Across

1. Ceylon
  <br>
  Ceylon Is Very Similar To Java.
  <br>
  Like Java It Is Overly Verbose.
  <br>
  It Appears To Not Have A Main Entry Point, Instead The Entry Function Is Set Via The Command Line.
  <br>
  Say We Have The Code:
  <br>
  ```Java
    shared void HelloWorld() {
      print("Hello World!");
    }
  ```
  <br>
  shared Means That The Function (Supposedly) Will be Able To Be Called From The Command Line
  <br>
  Running The Function:
  <br>
  ```batch
    ceylon-1.3.3/bin/ceylon run --compile=force --run=hello default
  ```
  <br>
  1. `--compilie=force` Forces The Program To Compile Before Ran
  2. `--run=HelloWorld` Runs HelloWorld Function As The Entry Point (Runs The Function "run" If Not Set)
  3. `default` Means The Program Will Ran A Given Module (Since No Module Exists `default` Isnt Too Useful)
  <br>
  ```batch
    ceylon-1.3.3/bin/ceylon compile (Path To File That Will Be Compiled)
    ceylon-1.3.3/bin/ceylon run --run=hello default
  ```
  <br>
  1. The First Line Compiles The Files And Optionally Compiles The Path Given
  2. The Second Line Compiles Runs The Function Given By The `--run` parameter, `default` Again Tells The Compiler To Execute The Given Module
  <br>
  ```Java
  print("Hello, this is Ceylon ``language.version``  
       running on ``runtime.name`` ``runtime.version``!\n
       You ran me at ``system.milliseconds`` ms, 
       with ``process.arguments.size`` arguments.");
  ```
  <br>
  Ceylon Does Some Interesting Things, It Gives Variables.
  <br>
  These Variables Give Information About The Executable And Enviornment Such As:
  <br>
  - The Runtime `runtime`
  - The System `system`
  - And The Process `process`


2. Wyvern



> Note Both Are Using The JVM (I Found This Interesting)
