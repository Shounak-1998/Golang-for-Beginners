## Anonymous Function

1.  An anonymous function is a function that is declared without any named identifier to refer to it.
2.  They can accept inputs and return outputs, just as standard fucntions do.
3.  They can be used for containing functionality that need not be named and possibly for short-term use.

main.go
<pre>
  package main
  import "fmt"
  func main () {
      x := func (1 int, b int) int {
          return 1 * b
      }
      fmt.Printf("%T \n", x)
      fmt.Println(x(20, 30))
  }

  >>> go run main.go
      func(int, int) int
      600
</pre>
