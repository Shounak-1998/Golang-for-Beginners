## Function Syntax

<pre>
 func <function_name>(<params>)<return type> {
  // body of the function
  }
</pre>

Example:-

<pre>
 func addNumbers(a int, b int) int {
 // body of the function
 }
</pre>

**return keyword**

return from method when it execution is complete

<pre>
 func addNumbers(a int, b int) int {
 sum := a + b
 return sum
 }
</pre>

**calling a function**

<pre>
 function_name(<arguments(s)>)
  add Numbers(2, 3)
  sumOfNumbers := addNumbers(2, 3)
</pre>

 **naming convention for functions**

 1. must begin with a letter
 2. can have any number of additional letters
 3. cannot contain spaces.
 4. case-sensitive.

**parametera vs arguments**

Function Paramter are the names listed in the function definition.
Function arguments are the real values passed into the function.

<pre>
 func addNumbers(a int, b int) int {
 sum := a + b
 return sum
 }
</pre>

<pre>
 func main() {
 sumOfNumbers := addNumbers(2, 3)
 fmt.Print(sumOfNumbers)
 }
</pre>

main.go
<pre>
 package main
 import "fmt"

 func printGreeting(str string) {
      fmt.Println("Hey there,", str)
 }
 func main() {
      printGreeting("Shounak")
 }

 >>> go run main.go
 Hey there, Shounak
</pre>
