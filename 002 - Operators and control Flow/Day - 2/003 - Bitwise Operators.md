## Bitwise Operators

Bitwise operators work at bit level or perform bit by bit operation.

**bitwise AND (&)**

1. takes two numbers as operands and does AND on every bit of two numbers.

main.go
<pre>
   package main
   import "fmt"

    func main() {
         var x, y int = 12, 25
         z := x & y
         fmt.Println(z)
   }
   >>> go run main.go
   8
</pre>

**bitwise OR (|)**

1. takes two numbers as operands and does OR on every bit of two numbers.

main.go
<pre>
   package main
   import "fmt"

    func main() {
         var x, y int = 12, 25
         z := x | y
         fmt.Println(z)
   }
   >>> go run main.go
   29
</pre>

**bitwise XOR (^)**

1. takes two numbers as operands and does XOR on every bit of two numbers.
2. The result of XOR is 1 if the two bits are opposite

main.go
<pre>
   package main
   import "fmt"

    func main() {
         var x, y int = 12, 25
         z := x ^ y
         fmt.Println(z)
   }
   >>> go run main.go
   21
</pre>

**right shift (>>)**

1. Shifts all bits towards left by a certain number of specified bits.
2. The bits positions that have been vacated by the left shift operator are filled with 0.

main.go
<pre>
   package main
   import "fmt"

    func main() {
         var x int = 212
         z := x << 1
         fmt.Println(z)
   }
   >>> go run main.go
   424
</pre>

**left shift (<<)**

1. Shifts all bits towards right  by a certain number of specified bits.
2. excess bits shifted off to the right are discarded.

main.go
<pre>
   package main
   import "fmt"

    func main() {
         var x int = 212
         z := x >> 2
         fmt.Println(z)
   }
   >>> go run main.go
   53
</pre>
