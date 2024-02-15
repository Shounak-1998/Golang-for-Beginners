## Arithmentic Operators

1.  Arithmetic operators are frequently combined with the comparison operator to create a Boolean statement. These operators are used to perform common arithmetic   
operations, such as addition, subtraction and multiplication.
2.  common comparisons -
     1.  Does the sum of two numbers equal a particular value?
     2.  Is the difference between two numbers lesser than a particular value?

**addition(+)**

1. adds the left and right operands.

main.go
<pre>
   package main
   import "fmt"

   func main() {
         var a, b string = "foo", "bar"
         fmt.Println(a + b)
   }

   >>> go run main.go
   foobar
</pre>

**subtraction(-)**

1. subtracts the right operand from the left operand.

main.go
<pre>
   package main
   import "fmt"

   func main() {
         var a, b float64 = 79.02, 75.66
         fmt.Println("%.2f",a - b)
   }

   >>> go run main.go
   3.36  
</pre>

**multiplication (*)**

1. multiples both operands.

main.go
<pre>
   package main
   import "fmt"

   func main() {
         var a, b int = 5,10
         fmt.Println(a * b)
   }

   >>> go run main.go
   50  
</pre>

**division (/)**

1. returns the quotient when left operand is divided by right operand

main.go
<pre>
   package main
   import "fmt"

   func main() {
         var a, b int = 10, 2
         fmt.Println(a / b)
   }

   >>> go run main.go
   5  
</pre>

**modulus (%)** 

1. returns the remainder when left operand is divided by right operand.

main.go
<pre>
   package main
   import "fmt"

   func main() {
         var a, b int = 24, 7
         fmt.Println(a % b)
   }

   >>> go run main.go
   3  
</pre>

**increment(++)**

1. unary operator are operators that act upon a single operand to produce a new value.
2. This operator increments the value of the operands by one.

main.go
<pre>
   package main
   import "fmt"

   func main() {
         var i int = 1
         i++
         fmt.Println(i)
   }

   >>> go run main.go
   2  
</pre>

**decrement (--)**

1. unary operator are operators that act upon a single operand to produce a new value.
2. This operator decrement the value of the operands by one.

main.go
<pre>
   package main
   import "fmt"

   func main() {
         var i int = 1
         i--
         fmt.Println(i)
   }

   >>> go run main.go
   0
</pre>
