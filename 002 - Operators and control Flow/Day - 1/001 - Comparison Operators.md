Comparison Operators

1.  compare two operands and yield a Boolean value
2.  allow values of the same data type for comparisons
3.  common comparisons-
   + Does one string match another?
   + Are two number the same?
   + Is one number greater than another?
   + == equal
   + != not equal
   + < less than
   + <= less than or equal to
   + >. greater than
   + >= greater than or qual to
     
**Equal to (==)**

1. return true when the values are equal

main.go
<pre>
   package main
   import "fmt"

   func main() {
         var city string = "Kolkata"
         var city_2 string = "calcutta"
         fmt.Println(city == city_2)
   }

   >>> go run main.go
   false 
</pre>

**not equal to (!=)**

1. return True when the values are not equal.

main.go
<pre>
  package main
   import "fmt"

   func main() {
         var city string = "Kolkata"
         var city_2 string = "calcutta"
         fmt.Println(city != city_2)
   }

   >>> go run main.go
   true  
</pre>

**less than (<)**

1. returns True when the left operand is lesser than the right operand.

main.go
<pre>
   package main
   import "fmt"

   func main() {
         var a, b int = 5,10
         fmt.Println(a < b)
   }

   >>> go run main.go
   true  
</pre>

**less than or equal to (<=)**

1. reutrns True when the left operand is lesser or equal to the right operand

main.go
<pre>
   package main
   import "fmt"

   func main() {
         var a, b int = 10, 10
         fmt.Println(a <= b)
   }

   >>> go run main.go
   true  
</pre>

**greater than (>)**

1. returns true when the left operand is greater than the right operand.

main.go
<pre>
   package main
   import "fmt"

   func main() {
         var a, b int = 20, 10
         fmt.Println(a > b)
   }

   >>> go run main.go
   true  
</pre>

**greater than or equal to (>=)**

1. returns true when the left operand is greater or equal to the right operand.

main.go
<pre>
   package main
   import "fmt"

   func main() {
         var a, b int = 20, 20
         fmt.Println(a >= b)
   }

   >>> go run main.go
   true  
</pre>
