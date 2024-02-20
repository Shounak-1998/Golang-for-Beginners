## Accessing Fields

<pre>
  <variable_name>.<field_name>
</pre>

main.go

<pre>
  package main
  import "fmt"
  type Circle struct {
    x int
    y int
    radius int
  }

  func main () {
    var c Circle
    c.x = 5
    c.y = 5
    c.radius = 5
    fmt.Printf("%+v \n", c)
    fmt.Printf("&+v \n", c.area)
  }
  >>> go run main.go
      c.area undefined (type Circle has no field or method area)
</pre>
