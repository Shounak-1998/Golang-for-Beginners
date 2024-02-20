## Recursive Functions

1.  recursion is a concept where a function calls itself by direct or indirect means.
2.  the function keeps calling itself until it reaches a base case.
3.  used to solve a problem where the solution is dependednt on the smaller instance of the same problem.

Example to calculate factorial of number factorial(5) = 5*4*3*2*1

main.go
<pre>
  package main
  import "fmt"
  func factorial(n int )int{
      if n == 1 {
          return 1
  }
    return n * factorial(n-1)
  }
  func main() {
    n := 5
    result := factorial(n)
    fmt.Println("Factorial of", n, "is :", result)

  >>> go run main.go
      Factorial of 5 is : 120
</pre>
