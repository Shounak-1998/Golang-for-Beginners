## Zero Values

**What is zero values in Golang?**

In Golang if you're declaring a new variable, but are not necessarily initializing it with a value, the variable is given default values is called zero value

1.bool-->false
2.int-->0
3.float64-->0.0
4.string-->""

Pointer, function values is nil

main.go
<pre>
  package main
  import "fmt"

  func main() {
        var i int
        fmt.Printf("%d", i)
  }

  >>> go run main.go
  0
</pre>

main.go
<pre>
  package main
  import "fmt"

  func main() {
        var f1 float64
        fmt.Printf("%.2f", f1)
  }

  >>> go run main.go
  0.00
</pre>

| Verb                                | Description   |
| ----------------------------------- | ------------- |
| int                                 | 0             |
| float64                             | 0.0           |
| string                              | ""            |
| bool                                | false         |
| pointers,functions,interfaces,maps  | nil           |
