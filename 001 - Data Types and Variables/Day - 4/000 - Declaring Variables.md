# Declaring Variables

We can declare a variables in many ways, that is declaring and assiging it a value on the same line.

main.go
<pre>
  package main
  import("fmt")

  func main() {
      var user string
      user = "Shounak"
      fmt.Pintln(user)
}

>>> go run main.go
    Shounak
</pre>

> Note data types of variables is also important as it defines what values may be assigned to it.

> [!CAUTION]
> A variables with the type of string for example cannot be assigned a integer value so compiler throw error

**Incorrect Value**

<pre>
  package main
  import ("fmt")

  func main () {
       var s string
       s = 123
       fmt.Println(s)
  }

  >>> go run main.go
  Error:cannot use 123 (type untyped int) as type string in assignment
</pre>

**shorthand way**

main.go
<pre>
  package main
  import ("fmt")

  func main() {
       var s,t string = "Shounak", "Khulape"
       fmt.Println(s)
       fmt.Println(t)
  }

  >>> go run main.go
      Shounak Khulape
</pre>

> The variables here are wrapped inside parenthesis after the var keyword but they are at different line

main.go
<pre>
  package main
  import ("fmt")

  func main() {
       var (
       s string = "Shounak"
       i int = "Khulape"
       fmt.Println(s)
       fmt.Println(t)
  }

  >>> go run main.go
      Shounak Khulape
</pr

  **Short Variable Declaration**

  <pre>
    s:="Hello Shounak"
  </pre>

  </pre>
  
main.go
<pre>
  package main
  import ("fmt")

  func main() {
       name:= "Shounak"
       name = "Khulape"
       fmt.Println(name)
  }

  >>> go run main.go
      Khulape
</pre>
  </pre>

> If we try to modify its value to an integer and we run we will going to get error we cannot use which is an integer data type as type string in assignment

<pre>
  package main
  import ("fmt")

  func main() {
       name:= "Shounak"
       name = 12
       fmt.Println(name)
  }

  >>> go run main.go
      Error: cannot use 12 (type untyped int) as type string in assignment
</pre>

