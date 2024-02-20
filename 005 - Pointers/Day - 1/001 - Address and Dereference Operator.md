## Address and Dereference Operator

1.  & operator - The address of a variable can be obtained by preceding the name of a variable with an ampersand sign (&), known as address-of operator.
2.  * operator - It is known as the dereference operator. when placed before an address, it returns the value at that address.
  
main.go

<pre>
  package main
  import "fmt"
  func main() {
    i := 10
    fmt.Printf("%T %v \n", &i, &i)
    fmt.Printf("%T %v \n", *(&i), *(&i))
  }

  >>> go run main.go
      *int 0xc00018c008
      int 10
</pre>
