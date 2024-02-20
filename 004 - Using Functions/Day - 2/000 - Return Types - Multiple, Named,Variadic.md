## Retrun Types

**returning single value**

**variadic functions**

1.  function that accepts variables number of arguments.
2.  it is possible to pass a varying number of arguments of the same type as referenced in the function signature.
3.  to declare a variadic function, the type of the final parameter is preceded by an ellipsis "..."
4.  Example - fmt.Println method

<pre>
  func <func_name> (param-1 type, param-2 type, para-3 ...type) <return_type>
</pre>
<pre>
  func sumNumbers(numbers ...int) int
</pre>
<pre>
  func sumNumbers(str string, numbers ...int)
</pre>

main.go
<pre>
  package main
  import "fmt"
  func sumNumbers(numbers ...int) int{
        sum := 0
        for _, value := range numbers {
            sum += value
        }
        return sum
  }
  func main() {
        fmt.Println(sumNumbers())
        fmt.Println(sumNumbers(10))
        fmt.Println(sumNumbers(10, 20))
        fmt.Println(sumNumbers(10, 20, 30, 40, 50))
  }
  >>> go run main.go
      0
      10
      30
      150
</pre>

**blank identifier '_'**

main.go
<pre>
  package main
  import "fmt"
  func f() (int, int) {
        return 42, 53
  }
  func main() {
        v , _ := f()
        fmt.Println(v)
  }

  >>> go run main.go
      42
</pre>

