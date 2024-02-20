## Passing by Value in Functions

1.  Function is called by directly passing the value of the variable as an argument.
2.  the paramter is copied into another location of your memory.
3.  So, when accessing or modifying the variable within your function, only the copy is accessed or modified, and the original value is never modified.
4.  All basic types (int, float, bool, string, array) are passed by value.

main.go
<pre>
  package main
  import "fmt"

  func modify(s string) {
      s = "world"
  }
  
  func main() {
    a := "hello"
    fmt.Println(a)
    modify(a)
    fmt.Println(a)
  }
  >>> go run main.go
      hello
      hello
  
</pre>
