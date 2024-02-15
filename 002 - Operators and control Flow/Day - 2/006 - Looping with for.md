## looping with for loop

A loop is a sequence of instructions that is continually repeated until a certain condition is reached.

**loop**

<pre>
  fmt.Println("Hello World!")
  fmt.Println("Hello World!")
  fmt.Println("Hello World!")
</pre>

**for loop syntax:**

<pre>
  for initialization; condition; post {
      // statement
  }
</pre>

**for loop**

<pre>
  for i := 1; i <=3; i++ {
      fmt.Println("Hello World")
    }
</pre>

main.go

<pre>
  package main
  import "fmt"

  func main() {
        i := 1
        for i<= 5 {
          fmt.Println(i * i)
          i +=c1
        }
   }
    >>> go run main.go
        1
        4
        9
        16
        25
</pre>

main.go

<pre>
  package main
  import "fmt"

  func main() {
        sum := 0
        for {
            sum++ // repeated forever
         }
         fmt.Println(sum)  // never reached
  }
  
    >>> go run main.go
       the infinite loop
</pre>

**Break statement**

1. the break statement end the loop immediately when it is encountered.

<pre>
  package main
  import "fmt"

  func main() {
        for i := 1; i <= 5; i++ {
          if i == 3 {
            break
          }
          fmt.Println(i)
  }
  }
    >>> go run main.go
       1
       2
        </pre>

**continue statement**

1. the continue statement skips the current iteration of loop and continues with the next iteration.

<pre>
  package main
  import "fmt"

  func main() {
        for i := 1; i <= 5; i++ {
          if i == 3 {
            continue
          }
          fmt.Println(i)
    }
  }
    >>> go run main.go
       1
       2
       3
       4
       5
        </pre>
