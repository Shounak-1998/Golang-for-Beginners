## Control Flow

**if-else**
**if**

<pre>
  if condition {
  // executes when condition is true
  }
</pre>

main.go
<pre>
   package main
   import "fmt"

    func main() {
         var a string = "happy"
         if a == "happy" {
           fmt.Println(z)
          }
   }
   >>> go run main.go
   happy
</pre>

**if-else**

<pre>
  if condition {
        // executes when condition is true
  }  else  {
        // executes when condition is false
  }
</pre>

main.go
<pre>
   package main
   import "fmt"

    func main() {
         var fruit string = "grapes"
         if fruit == "apples" {
              fmt.Println("Fruit is apple")
          } else {
                  fmt.Println("Fruit is not apple")
   }
   >>> go run main.go
   Fruit is not apple
</pre>

**if-else-if else**

<pre>
  if condition_1 {
    // execute when condition_1 is true
  }  else if condition_2  {
    /* execute when condition_1 is false, and condition_2 is true */
  }  else if condition_3  {
    /* execute when condition_1 and 2 are false, and condition_3 is true */
  }  else  {
    // when none of the above conditions are true
  }
</pre>

main.go
<pre>
   package main
   import "fmt"

    func main() {
         fruit := "grapes"
         if fruit == "apple"
            fmt.Println("I love apples")
         }  else if fruit == "orange" {
            fmt.Println("Oranges are not apples")
         }  else  {
              fmt.Println("no appetite")
          }
  }
   >>> go run main.go
   no appetite
</pre>

