## Static vd Dynamic typed languages

__Static typed__<br>
Compiler throws an error when types are used incorrectly.Ex.C++, Java <br>

main.cpp<br>

`void add (int a, int b) {`<br>
  `count<<a+b` <br>
`}<br>`

`add(1,2)->3` <br>
`add(1,"two")->ERROR` <br>

__Dynamic typed__<br>
Compiler does not enforce the type system Ex. Python, Javascript <br>

main.js <br>

`function add (a,b)`<br>
`return a+b;`<br>
`}`<br>
`add(1,2)->3`<br>
`add(1,"two")->1two`<br>

Such languages are called weakly typed,loosely typed or dynamic typed.<br>

__Static typed advantages__<br>
1. Better Performances<br>
2. Bugs can often be caught by a compiler<br>
3. Better ata integrity<br>

_Dynamic Typed advantages__<br>

1. Fatser to write code.<br>
2. Generally, less rigid.<br>
3. Shorter learning curve.<br>

__Golang__<br>

1. Go has a concept of types that is either explicitly declared by a programmer or is inferred by the compiler.<br>
2. It's fast, statically typed, compiled language that feels like a dynamically typed, interpreted lanaguage.<br>

Example.<br>

main.go <br>

`package main`<br>
`import ("fmt")`<br>
`func main() {` <br>
`name:="Lisa"`<br>
`fmt.Println(name)`<br>
`}`<br>
`...go run main.go`<br>
`Lisa`




