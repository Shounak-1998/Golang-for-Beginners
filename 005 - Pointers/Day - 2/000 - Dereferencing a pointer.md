## Dereferencing a Pointer
<pre>
  *<pointer_name>
</pre>

main.go
<pre>
  package main
  import "fmt"
  func main() {
    s := "hello"
    fmt.Printf("%T %v \n", s, s)
    ps := &s
    *ps = "world"
    fmt.Printf("%T %v \n", s, s)
  }

  >>> go run main.go
      string hello
      string world
</pre>
