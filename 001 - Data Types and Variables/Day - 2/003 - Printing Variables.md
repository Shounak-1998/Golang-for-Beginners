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
