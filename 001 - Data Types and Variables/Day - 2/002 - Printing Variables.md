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
  fmt.Print("Welcome", name, ", ",user)
}

>>>go run main.go
Welcome to Shounak, Khualpe
</pre>

> Now the only problem with print method is that it does not introduce a new line after printing. if we declare two variables and print them one after the other,on runnigna program we see that both of them are printed just next to each other anf doe solution to this is new line character
