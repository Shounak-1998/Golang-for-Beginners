## Switch Statement

**switch-case**

syntax

<pre>
  switch expression {

  case value_1:
      // execute when expression equals to value_1
  case value_2:
      // execute when expression equals to value_2
  default:
      // execute when no match is found
  }
</pre>

main.go
<pre>
   package main
   import "fmt"

    func main() {
         var i int = 100
         switch i {
              case 10:
                fmt.Println("i is 10")
              case 100, 200:
                fmt.Println("i is either 100 or 200")
              default:
                fmt.Println("i is neither 0, 100 or 200")
          }
  
   }
   >>> go run main.go
   i is either 100  or 200
</pre>

**fallthrough**

1.  The fallthrough keyword is used in switch-case to force the executiom flow to fall through the successive case block.

<pre>
   package main
   import "fmt"

    func main() {
         var i int = 100
         switch i {
              case 10:
                fmt.Println("i is 10")
              case 100, 200:
                fmt.Println("i is either 100 or 200")
              default:
                fmt.Println("i is neither 0, 100 or 200")
          }
  
   }
   >>> go run main.go
   i is either 100  or 200
</pre>

<pre>
   package main
   import "fmt"

    func main() {
         var i int = 10
         switch i {
              case -5:
                fmt.Println("-5")
              case 10:
                fmt.Println("10")
                fallthrough
              case 20:
                fmt.Println("20")
                fallthrough
              default:
                fmt.Println("default")
          }
  
   }
   >>> go run main.go
   i is either 100  or 200
</pre>

**switch with condition**

<pre>
   package main
   import "fmt"

    func main() {
         var a, b int = 10, 20
         switch {
              case a+b == 30:
                fmt.Println("equal to 30")
              case a+b <= 30:
                fmt.Println("less than or equal to 30")
              default:
                fmt.Println("greater than 30")
          }
   }
   >>> go run main.go
   equal to 30
</pre>
