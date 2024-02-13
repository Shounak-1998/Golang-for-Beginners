## Variable scope

The scope of varibale can be defined as a part of the program, where particular variable is accessible or from where it can be referenced.
In Golang scope is defined using block (it is possibily empty sequence of declaration and statement within curly brackets)

<pre>
  {
  // outer block
    {
    //  inner block
    }
  }
</pre>

1. Inner blocks can access variables declared within outer blocks.
2. Outer blocks cannot access variables declared within inner blocks.
   
main.go
<pre>
  func main() {
  city := "London"
  {
      country := "UK"
      fmt.Println(country)
      fmt.Println(city)
  }
  fmt.Println(country)
  fmt.Println(city)

  >>> go run main.go
      Error: ./main.go: Line 10: undefined: country
</pre>

If we remove this line it will work fine

<pre>
  func main() {
  city := "London"
  {
      country := "UK"
      fmt.Println(country)
      fmt.Println(city)
  }
  fmt.Println(city)

  >>> go run main.go
      UK
      London
      London
</pre>

## Local vs Gloabl Variables

**Local Variables**
1. Declared inside a function or a block.
2. not accessible outside the function or the block
3. can also be declared inside looping and conditional statements.

> Let see exmaple of Local Varibales

main.go
<pre>
  package main
  import ("fmt")

  func main() {
       name:= "Shounak"
       fmt.Println(name)
  }

  >>> go run main.go
      Shounak
</pre>

**Global Variables**

1. Declared outside if a function or a block.
2. They are available throughout the lifetime of a program.
3. declared at the top of the program outside all functions or blocks
4. can be accessed from any part of the program.

5. main.go
<pre>
  package main
  import ("fmt")
  var name string:= "Shounak"
  func main() {
       
       fmt.Println(name)
  }

  >>> go run main.go
      Shounak
</pre>
