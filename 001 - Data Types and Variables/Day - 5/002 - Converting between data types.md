## Converting betwwen data types

**Type Casting**

1.  The process of converting one dats type to another is known as Type Casting.
2.  Data Types can be converted to other data types, but this does bot not gurantee that the value of the varibale will remian intact.

**integer to float**

main.go
<pre>
  package main
  import "fmt"

  fucn main() {
        vat i int = 90
        var f floatb64 = float64(i)
        fmt.Printf("%.2f\n",f)
  }

  >>> go run main.go
  90.00

</pre>

**float to integer**

main.go
<pre>
  package main
  import "fmt"

  fucn main() {
        var f float64 = 45.89
        var i int = int(f)
        fmt.Printf("%v\n",i)
  }

  >>> go run main.go
  45
</pre>

**strconv package**

1.  Itoa()
   1.  converts integer to string
   2.  return one value-string froma with the given integer

main.go
<pre>
  package main
  import (
  "fmt"
  "strconv"

  fucn main() {
        var i itn = 42
        var s string = strconv.Itoa(i) //convert int to string
        fmt.Printf("%q",s)
  }

  >>> go run main.go
  "42"
</pre>

2.  Atoi()
   1.  converts string to integer
   2.  returns two values-the corresponding integer, error(if any).

**string to integer**

main.go
<pre>
  package main
  import (
  "fmt"
  "strconv"

  fucn main() {
        var s string = "200"
        i, err := strconv.Atoi(s)
        fmt.Printf("%v, %T \n", i, i)
        fmt.Printf("%v, %T", err, err)
  }

  >>> go run main.go
  200, int
  <nil>, </nil>
</pre>

main.go
<pre>
  package main
  import (
  "fmt"
  "strconv"

  fucn main() {
        var s string = "200abc"
        i, err := strconv.Atoi(s)
        fmt.Printf("%v, %T \n", i, i)
        fmt.Printf("%v, %T", err, err)
  }

  >>> go run main.go
  0, int
  strconv.Atoi: parsing "200a": invalid syntax, *strconv.Numerror
</pre>



