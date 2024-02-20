## defer statement

1.  A defer statement delays the execution of a function until the surrounding function returns.
2.  The deferred call's argument are evaluated immediately but the function is not executed until the surrounding function returns.

main.go

<pre>
  package main
  import "fmt"
  func printName(str string) {
        fmt.Println(str)
  }
  func printRollNo(rno int) {
        fmt.Println(rno)
  }
  func printAddress(adr string) {
        fmt.Println(adr)
  }
  func main() {
        printName("Shounak")
        defer printRollNo(23)
        printAddress("street-32")
  }

  >>> go run main.go
      Shounak
</pre>
