## Slices

1. A slice is defined as a continuous segment of an underlying array and it provides access to a numbered sequence of elements from that array.
2. Slices provide access to parts of an array in sequential order.
3. Slices are more fexible and more powerful than arrays since arrays had limitations of being fixed size.
4. Unlike array they are variable type (elements can be added or removed)
5. Due to this they offer more flexibility as compared to arrays.

**Components of a slice**

1.  Slice has 3 major component Pointer ,length ,capacity.
2.  Pointer are just varibales that hold memory addresses.
3.  The Length is number of elements it contains.
4.  The length and capacity can be obtain by len() cap()

**declaring and initializing a slice**

<pre>
  slice_name := []data_type{values}
</pre>

<pre>
  grades := []int{10, 20, 30}
</pre>

main.go
<pre>
  package main
  import "fmt"

  func main() {
       slice := []int{10, 20, 30}
       fmt.Println(slice)
  }
  >>> go run main.go
  [10 20 30]
</pre>

main.go
<pre>
  package main
  import "fmt"

  func main() {
       arr := [10]int{10, 20, 30, 40, 50, 60, 70, 80, 90, 100}
       slice := arr[1:8]
       fmt.Println(slice_1)
  }
  >>> go run main.go
  [20, 30, 40, 50, 60, 70, 80]
</pre>

main.go
<pre>
  package main
  import "fmt"

  func main() {
       arr := [10]int{10, 20, 30, 40, 50, 60, 70, 80, 90, 100}
       slice := arr[1:8]
       fmt.Println(slice)
       sub_slice := slice[0:3]
       fmt.Println(sub_slice)
  }
  >>> go run main.go
  [20, 30, 40, 50, 60, 70, 80]
  [20 30 40]
</pre>

**make function**

main.go
<pre>
  package main
  import "fmt"

  func main() {
       arr := [10]int{10, 20, 30, 40, 50, 60, 70, 80, 90, 100}
       slice := make([]int, 5, 8)
       fmt.Println(slice)
       fmt.Println(len(slice))
       fmt.Println(cap(slice))
  }
  >>> go run main.go
  [20, 30, 40, 50, 60, 70, 80]
  [20 30 40]
</pre>

**capacity function**

main.go
<pre>
  package main
  import "fmt"

  func main() {
       arr := [10]int{10, 20, 30, 40, 50, 60, 70, 80, 90, 100}
       slice := arr[1:8]
       fmt.Println(cap(arr))
       fmt.Println(cap(slice))
  }
  >>> go run main.go
  10
  9
</pre>

**slice and index numbers**

main.go
<pre>
  package main
  import "fmt"

  func main() {
       arr := [5]int{10, 20, 30, 40, 50}
       slice := arr[:3]
       fmt.Println(arr)
       fmt.Println(slice)

       slice[1] = 9000
  
       fmt.Println("after modification")
       fmt.Println(arr)
       fmt.Println(slice)
  }
  >>> go run main.go
  [10 20 30 40 50]
  [10 20 30]
  after modification
  [10 9000 30 40 50]
  [10 9000 30]
</pre>

**appending to a slice**

<pre>
  func append(s []T, vs ...T) []T
</pre>
<pre>
  slice = append(slice, element-1, element-2)
</pre>
<pre>
  slice = append(slice, 10, 20, 30)
</pre>

main.go
<pre>
  package main
  import "fmt"

  func main() {
       arr := [4]int{10, 20, 30, 40}
       slice := arr[1:3]
       fmt.Println(slice)
       fmt.Println(len(slice))
       fmt.Println(cap(slice))

       slice = append(slice, 900, -90, 50)
       fmt.Println(slice)
       fmt.Println(len(slice))
       fmt.Println(cap(slice))
  }
  >>> go run main.go
  [20 30]
  2
  3
  [20 30 900 -90 50]
  5
  6
</pre>

**deleting from a slice**

main.go
<pre>
  package main
  import "fmt"

  func main() {
       arr := [10]int{10, 20, 30, 40, 50}
       i := 2
       fmt.Println(arr)
       slice_1 := arr[:i]
       slice_2 := arr[i+1:]
       new_slice := append(slice_1, slice_2...)
       fmt.Println(new_slide)
  }
  >>> go run main.go
  [10 20 30 40 50]
  [10 20 40 50]
</pre>

**copying from a slice**

<pre>
  func copy(dst, src [] Type) int
</pre>
<pre>
  num := copy(dest_slice, src_slice)
</pre>

main.go
<pre>
  package main
  import "fmt"

  func main() {
       src_slice := []int{10, 20, 30, 40, 50}
       dest_slice := make([]int, 3)
       num := copy(dest_slice, src_slice)
       fmt.Println(dest_slice)
       fmt.Println("Number of elements copied: ", num)
  }
  >>> go run main.go
  [10 20 30]
  Number of elements copied: 3
</pre>

**looping through a slice**

main.go
<pre>
  package main
  import "fmt"

  func main() {
       arr := [10]int{10, 20, 30, 40, 50}
       for index, value := range arr {
           fmt.Println(index, "=>", value)
  }
  }
  >>> go run main.go
  0 => 10
  1 => 20
  2 => 30
  3 => 40
  4 => 50
</pre>

main.go
<pre>
  package main
  import "fmt"

  func main() {
       arr := [10]int{10, 20, 30, 40, 50}
       for _, value := range arr {
           fmt.Println(value)
  }
  }
  >>> go run main.go
  10
  20
  30
  40
  50
</pre>
