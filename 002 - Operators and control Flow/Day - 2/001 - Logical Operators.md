## Logical Operators

1.  Used to determeine the logic between variables or values.
2.  common logical comparisons-
   1.  Are two variables both true?
   2.  Does either of two expressions evaluate to true?

**And (&&)**

1. returns true if both the statements are true.
2. returns false when either of the statement is false.

main.go
<pre>
   package main
   import "fmt"

   func main() {
         var x int = 10
         fmt.Println((x < 100) && (x < 200))
         fmt.Println((x < 300) && (x < 0))
         i++
         fmt.Println(i)
   }

   >>> go run main.go
   true
   false
</pre>

**OR (||)**

1. returns true if one of the statement is true.
2. returns false when both statements are false.

main.go
<pre>
   package main
   import "fmt"

    func main() {
         var x int = 10
         fmt.Println((x < 0) || (x < 200))
         fmt.Println((x < 0) || (x > 200))
         i++
         fmt.Println(i)
   }
   >>> go run main.go
   true
   false
</pre>

**NOT (!)**

1. unary operator.
2. Reverses the result, returns false if the expreseeion evaluates to true and vice versa.

main.go
<pre>
   package main
   import "fmt"

    func main() {
         var x, y int = 10, 20
         fmt.Println(!(x > y))
         fmt.Println(!(true))
         fmt.Println(!(false))
         i++
         fmt.Println(i)
   }
   >>> go run main.go
   true
   false
   true
</pre>

