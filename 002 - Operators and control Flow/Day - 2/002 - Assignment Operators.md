## Assignment Operators.

**assign (=)**

1. assign left operand with the value to the right
2. x = y

main.go
<pre>
   package main
   import "fmt"

    func main() {
         var x int = 10
         var y int
         y = x
         fmt.Println(y)
   }
   >>> go run main.go
   10
</pre>

**add and assign (+=)**

1. assign left operand with the addition result.
2. x+= y means x = x + y

main.go
<pre>
   package main
   import "fmt"

    func main() {
         var x, y int = 10, 20
         x +=y
         fmt.Println(x)
   }
   >>> go run main.go
   30
</pre>

**subtract and assign (-=)**

1. assign left operand with the subtraction result.
2. x-= y means x = x - y

main.go
<pre>
   package main
   import "fmt"

    func main() {
         var x, y int = 10, 20
         x -= y
         fmt.Println(x)
   }
   >>> go run main.go
   -10
</pre>

**multiply and assign (*=)**

1. assign left operand with the multiplication result.
2. x*= y means x = x * y

main.go
<pre>
   package main
   import "fmt"

    func main() {
         var x, y int = 10, 20
         x *= y
         fmt.Println(x)
   }
   >>> go run main.go
   200
</pre>

**divide and assign (/=)**

1. assign left operand with the quotient of the division.
2. x/= y means x = x / y

main.go
<pre>
   package main
   import "fmt"

    func main() {
         var x, y int = 200, 20
         x /= y
         fmt.Println(x)
   }
   >>> go run main.go
   10
</pre>

**divide and assign modulus (%=)**

1. assign left operand with the remainder of the division.
2. x%= y means x = x % y

main.go
<pre>
   package main
   import "fmt"

    func main() {
         var x, y int = 210, 20
         x %= y
         fmt.Println(x)
   }
   >>> go run main.go
   10
</pre>
