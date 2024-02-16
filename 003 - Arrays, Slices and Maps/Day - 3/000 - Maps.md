## Maps

1.  unordered collection of key/value pairs.
2.  implemented by hash tables.
3.  provide efficient add, get and delete operations.

**declaring and initializing a map**
<pre>
  var map_name map[key data type] value data type
</pre>
<pre>
  var my_map map[]string int
</pre>

<pre>
  package main
  import "fmt"

  func main() {
      var codes map[string]string
      codes["en"] = "English"
      fmt.Println(codes)

  >>> go run main.go
  panic: assignment to entry in nil map
</pre>

To create a map in key values pair

map_name := map[key data type]value data type{key value pairs}
<pre>
  codes := map[string]string{"en": "English", "fr": "French"}
</pre>

<pre>
  package main
  import "fmt"

  func main() {
      codes := map[string]string{"en": "English", "fr": "French"}
      fmt.Println(codes)
  }
  >>> go run main.go
  map[en:English fr:French]
</pre>

make() function

main.go
<pre>
  package main
  import "fmt"

  func main() {
      codes := make(map[string]int)
      fmt.Println(codes)
  }
  >>> go run main.go
  map[]
</pre>

**length of map**

1.  len()

**accessing a map**

1.  map[key]

**getting a key**

value, found :=map_name[key]
