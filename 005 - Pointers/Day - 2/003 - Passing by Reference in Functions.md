## Passing by Reference in Functions

1.  Go supports pointer, allowing you to pass references to values within your program.
2.  In call by reference/pointer, the address of the variable is passed into the function call as the actual paramter.
3.  All the operations in the function are performed in the value stored at the address of the actual parameters.

<pre>
  package main
  import "fmt"

  func modify(s string) {
      *s = "world"
  }
  
  func main() {
    a := "hello"
    fmt.Println(a)
    modify(&a)
    fmt.Println(a)
  }
  >>> go run main.go
      hello
      world
</pre>

1. slices are passed by reference by default

<pre>
  package main
  import "fmt"

  func modify(s []int) {
      s[0] = 100
  }
  
  func main() {
    slice := []int{10, 20, 30}
    fmt.Println(slice)
    modify(slice)
    fmt.Println(slice)
  }
  >>> go run main.go
      [10 20 30]
      [100 20 30]
</pre>

2. Maps as well are passed by refernece by default

<pre>
  package main
  import "fmt"

  func modify(s []int) {
      m["K"] = 75
  }
  
  func main() {
    ascii_codes := make(map[string]int)
    ascii_codes["A"] = 65
    ascii_codes["F"] = 70
    fmt.Println(ascii_codes)
    modify(ascii_codes)
    fmt.Println(ascii_codes)
  }
  >>> go run main.go
      map[A:65 F:70]
      map[A:65 F:70 K:75]
</pre>

