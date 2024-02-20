## Declaring and Initializing a Struct

**struct-decalration**

<pre>
  type<struct_name> struct {
    // list of fields
    }

    type Circle struct {
      x float64
      y float64
      r float64
    }
</pre>

<pre>
  type Student struct {
    name string
    rollNo int
    marks []int
    grades map[string] int
</pre>

**struct-initialize**

<pre>
  var <variable_name><struct_name>
    var s Student
</pre>

main.go
<pre>
  package main
  import "fmt"
  type Student struct {
    name string
    rollNo int
    marks []int
    grades map[string] int
  }
  func main() {
    var s Student
    fmt.Printf("%+v", s)
  }
  >>> go run main.go
  {name: rollNo:0 marks:[] grades:map[]}
</pre>
