## User Input

> We will see how to read input from a user.

**Scanf**

One ways to take input is through scanner function, which is provided by the FMT package.

<pre>
  fmt.Scanf("%<format specifier> (s)", Object_arguments)
</pre>

Scanner function takes the format string, along with the list of variable number of arguments.The String contains custom specifiers that the scanner function uses to format final output string, The list is the list of all arguments where you want to store your data.

main.go
<pre>
  package main
  import"fmt"

  func main() {
      var name string
      fmt.Print("Enter your name:")
      fmt.println("Hey there, ", name)
  }

  >>> go run main.go
      Enter your name: Shounak
      Hey there, Shounak
</pre>

main.go
<pre>
  package main
  import"fmt"

  func main() {
      var name string
      var is_muggle bool
      fmt.Print("Enter your name & are you a muggle:")
      fmt.Scanf("%s %t", &name, &is_muggle)
      fmt.println(name, is_muggle)
  }

  >>> go run main.go
      Enter your name & are you a muggle: Shounak false
      Shounak false
</pre>

> Scanf function reads from the input source sequentially. Hence we must give list of argument in the order that specifed in format string

count->      the number of arguments that the fucntion writes to

error->        any error thrown during the execution of the function

Multiple Input

main.go
<pre>
  package main
  import"fmt"

  func main() {
      var a string
      var b int
      fmt.Print("Enter a string and a number:")
      count, err := fmt.Scanf("%s %d", &a &b)
      fmt.println("count : ", count)
      fmt.println("a: ", a)
      fmt.println("b: ", b)
  }

  >>> go run main.go
      Enter a sting and a number: Shounak yes
      count : 1
      error: expected integer
      a: Shounak
      b: 0
</pre>
