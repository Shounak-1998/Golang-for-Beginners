## Declaring and Initializing a Pointer

**declare a pointer**

<pre>
  var <pointer_name> *<data_type>
</pre>
<pre>
  var ptr_i *int
</pre>
<pre>
  var ptr_s *string
</pre>

main.go
<pre>
  package main
  import "fmt"
  func main() {
      var i *int
      var s *string
      fmt.Println(s)
  }
  >>> go run main.go
      <nil>
      <nil>  
</pre>

**initializing a pointer**

<pre>
  var <pointer_name> *<data_type> = &<variable_name>

    i := 10
    var ptr_i *int = &i
</pre>
