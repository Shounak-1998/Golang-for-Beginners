## find type of variable

1. %T format specifier
2. reflect.TypeOf function from the reflect package

**using %T**

main.go
<pre>
  package main
  import "fmt"

  func main() {
       var grades int = 42
       var message string = "hello world"
       var isCheck bool = true
       var amount float32 = 5466.54

       fmt.Printf("variable grades = %v is of type %T \n", grades, grades)
       fmt.Printf("variable message = '%v' is of type %T \n", message, message)
       fmt.Printf("variable isCheck = '%v' is of type %T \n", isCheck, isCheck)
       fmt.Printf("variable amount = %v is of type %T \n", amount, amount)
  }

  >>> go run main.go
  variable grades = 42 is of type int
  variable message = 'hello world' is of type string
  variable isCheck = 'true' is of type bool
  variable amount = 5466.54 is of type float32
</pre>

**using reflect.TypeOf()**

main.go
<pre>
  package main
  import (
  "fmt"
  "reflect"
  )

  func main () {
        fmt.printf("Type: %v \n", reflect.TypeOf(1000))
        fmt.printf("Type: %v \n", reflect.TypeOf("Shounak"))
        fmt.printf("Type: %v \n", reflect.TypeOf(46.0))
        fmt.printf("Type: %v \n", reflect.TypeOf(true))
        
  }

  >>> go run main.go
      Type: int
      Type: string
      Type: float64
      Type: bool
</pre>

> Declare with variables

main.go
<pre>
  package main
  import (
  "fmt"
  "reflect"
  )

  func main () {
        var grades int = 42
        var message string = "hello world"
        fmt.Printf("variable grades=%v is of type %v \n", grades, reflect.TypeOf(grades))
        fmt.Printf("variable message='%v' is of type %v \n", message, reflect.TypeOf(message))
        
  }

  >>> go run main.go
      variable grades = 42 is of type int
      variable message = 'hello world' is of type string
</pre>
