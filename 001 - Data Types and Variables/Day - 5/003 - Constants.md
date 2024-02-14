## Constants

Constants as the name state, they are varaiables whos values ones initialized cannot be modified.

Syntax:

<pre>
  const  <const name>  <data type>  =  <value>
</pre>

**Untyped constant**

1.  constants are untyped unless they are explicitly given a type at declaration.
2.  allow for flexibility

<pre>
  const age = 12

  const h_name, h_age = "Shounak", 12
</pre>

**Typed constant**

1.  constants are typed when you explicitly specify the type in the declaration.
2.  flexibility that comes with untyped constsnts is lost

<pre>
  const name string = "Shounak Khulape"

  const age int = 12
</pre>

**Understanding constant**

main.go

<pre>
  package main
  import "fmt"

  func main() {
        const name = "Shounak Khualpe"
        const is_muggle = false
        const age =  12

        fmt.Printf("%v: %T \n", name, name)
        fmt.Printf("%v: %T \n", is_muggle, is_muggle)
        fmt.Printf("%v: %T", age, age)
  }
  >>> go run main.go
  Shounak Khulape: string
  false: bool
  12: int
</pre>

> Core concept of constant once initialize cannot change once change cause runtime error

<pre>
  package main
  import "fmt"

  func main() {
        const name = "Shounak Khualpe"
        name = "Abc Def"

        fmt.Printf("%v: %T \n", name, name)
  }
  >>> go run main.go
  Error: cannot assign to name (declared const)
</pre>

> You cannot declare constant and not initialize it a value and will try to assign a value later on

<pre>
  package main
  import "fmt"

  func main() {
        const name
        name = "Shounak Khualpe"
        fmt.Printf("%v: %T \n", name, name)
  }
  >>> go run main.go
  missing value in const declaration, undefined: name
</pre>

> Short hand variablee assignment operator

<pre>
  package main
  import "fmt"

  func main() {
        const name := "Shounak Khualpe"
        fmt.Printf("%v: %T \n", name, name)
  }
  >>> go run main.go
  Error: syntax error: unexpected :=, expecting = 
</pre>

