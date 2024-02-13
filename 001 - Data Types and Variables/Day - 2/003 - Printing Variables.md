## Printing Variables

__Printing a String__

main.go <br>

<pre>
package main
import "fmt"
func main() {
  fmt.Print("Hello World")
}

>>>go run main.go
Hello World
</pre>

<pre>
package main
import "fmt"
func main() {
  var city string = "Kolkata"
  fmt.Print(city)
}

>>>go run main.go
Kolkata
</pre>

<pre>
package main
import "fmt"
func main() {
  var name string = "Shounak"
  var user string = "Khulape"
  fmt.Print("Welcome to", name, ", ",user)
}

>>>go run main.go
Welcome to Shounak, Khualpe
</pre>

> Now, the only problem with using print method is that does not introduce new line after the printing. So if we declare two variables and print one after the other on running the program both of them is printed next to each other the solution is new line character

<pre>
package main
import "fmt"
func main() {
  var name string = "Shounak"
  var user string = "Khulape"
  fmt.Print(name)
  fmt.Print(user)
}

>>>go run main.go
ShounakKhualpe
</pre>

__newline character__

1. \n is called the Newline character.<br>
2. It is used to create a new line.<br>
3. Place with string expressions.<br>
4. When inserted in a string, all the characters after \n are added to a new line.<br>

<pre>
package main
import "fmt"
func main() {
  var name string = "Shounak"
  var user string = "Khulape"
  fmt.Print(name, "\n")
  fmt.Print(user)
}

  
>>>go run main.go
Shounak
Khualpe
</pre>

> We see the string Shounak was printed on new line

**println**

We have another printing packages that makes the printing of Newline process even more easier for us its called println

<pre>
package main
import "fmt"
func main() {
  var name string = "Shounak"
  var user string = "Khulape"
  fmt.Println(name)
  fmt.Println(user)
}

  
>>>go run main.go
Shounak
Khualpe
</pre>

> Notice we didnt use a new line character but the second print statement got printed on new line.

Now you have notice that putting commas making more difficult to rescue it has printf function that implements formateed input-output

**Printf**

<pre>
  fmt.Printf("Template string %s", Object args(s))
</pre>

It is the process of inserting a custom string or variable in predefined text in golang printf function we can use from fmt package +, The function takes a template string that contains the text that needs to be formated.

**Printf-format specifier**

Format specifiers tell Golang how to format different type of data types

:point_right: %v formats the value in a default format.

<pre>
  var name string = "KodeKloud"
  fmt.Printf("Nice to see you here, at %v", name)

  >>> Nice to see you here, at Kodekloud
</pre>

:point_right: %d formats decimal integer.

<pre>
  var grades int = 42
  fmt.Printf("Marks: %d", grades)

  >>> Marks: 42
</pre>

Now let us use these format specifiers together.

main.go
<pre>
  package main
  import ("fmt")

  func main() {
        var name string = "Joe"
        var i int = 78
        fmt.Printf("Hey, %v! You have scored %d/100 in Physics", name, i)
  }

  >>> go run main.go
      Hey, Joe! You have scored 78/100 in Physics
</pre>

Here are few format specifiers we used in Golang

|Verb |Description                              |
| --- | ----------------------------------------|
| %v  | defualt format                          |
| %T  | type of the value                       |
| %d  | integers                                |
| %c  | character                               |
| %q  | quoted characters/string                |
| %s  | plain string                            |
| %t  | true or false                           |
| %f  | floating numbers                        |
| %2f | floating numbers upto 2 decimal places  |


