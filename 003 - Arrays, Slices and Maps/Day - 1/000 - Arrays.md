## Arrays

1.  An array a collection of similar data elements that are stored at contiguous memory locations.
2.  For example - We can have a collection of integers that represent roll number of student in a class

      | 1             | 2             | 3             | 4             |
      | ------------- | ------------- | ------------- | ------------- |

3.  For example - we have collection of strings that might represent characters of state
   
      | Maharashtra             | Karnataka             | Gujarat             | Orissa             |
      | -------------           | -------------         | -------------       | -------------      |

4.  Elements in array are store in contiguous memory location
5.  Arrays are also known as homogenous data typessince we can store elements of s single data type in one array and not different data types in one single array.

6.  **Array elements**

      | 1             | 2             | 3             | 4             | 5             |
      | ------------- | ------------- | ------------- | ------------- | ------------- |

7.  **memory address**

     | 200             | 204             | 208             | 212             | 216             |
     | -------------   | -------------   | -------------   | -------------   | -------------   |
     | 4 bytes             | 4 bytes             | 4 bytes             | 4 bytes             | 4 bytes             |

**Why we need Array**

In Programming most of the time we need to store large amount of data of similar type

**Arrays in Golang**

1. It is fixed length once declared and the size is mentioned we cannot change the length of the array
2. Elements in the array should be of the same data types
3. Arrays in Golang has the pointer that point to the first element of the array since memory is contiguous we can calculate the memory address that we want to.
4. It also has the property called length which denotes the number of elements in the array and properties of capacity the number of element it can content.

**Array declaration**

syntax

  | var             | array name               | size of the array                 | data type               |
  | -------------   | -------------            | -------------                     | -------------           |
  | var             | grades                   | [5]                               | int                     |
  | var             | fruits                   | [3]                               | string                  |     

main.go

<pre>
  package main
  import "fmt"

  func main() {
        var grades [5] int
        fmt.Println(grades)
        var fruits [3] string
        fmt.Println(fruits)
  }
  >>> go run main.go
  [0 0 0 0 0]
  [  ]
</pre>

**Array initialization**

<pre>
  var grades [3]int = [3]int{10,20,30}
</pre>
<pre>
  grades := [3]int{10,20,30}
</pre>
<pre>
  grades := [...]int{10, 20, 30}
</pre>

main.go
<pre>
  package main
  import "fmt"

  func main() {
       var fruits [2]string = [2]string{"apples","oranges"}
       fmt.Println(fruits)
       marks := [3]int{10,20,30}
       fmt.Println(marks)
       names := [...]string{"Rachel", "Phoebe", "Monica"}
       fmt.Println(names)
  }
  >>> go run main.go
  [apples oranges]
  [10 20 30]
  [Rachel Phoebe Monica]
</pre>

**len()**

1. The length of the array refers to the number of elements stored in the array.

main.go
<pre>
  package main
  import "fmt"

  func main() {
       var fruits [2]string = [2]string{"apples","oranges"}
       fmt.Println(len(fruits))
  }
  >>> go run main.go
  2
</pre>

**indexes in array**

1. Array is also numbered and these numbers are called array index.

      | 90            | 86             | 76             | 42            | 85            |
      | ------------- | -------------  | -------------  | ------------- | ------------- |

grades[1] = > 86
grades[0] = > 90

**array indexing**

main.go
<pre>
  package main
  import "fmt"

  func main() {
       var fruits [5]string = [5]string{"apples","oranges","grapes","mango","papaya"}
       fmt.Println(fruits[2])
  }
  >>> go run main.go
  grapes
</pre>

<pre>
  package main
  import "fmt"

  func main() {
       var fruits [5]string = [5]string{"apples","oranges","grapes","mango","papaya"}
       fmt.Println(fruits[6])
  }
  >>> go run main.go
  invalid array index 6 (out of bounds for 5- element array)
</pre>

<pre>
  package main
  import "fmt"

  func main() {
       var grades [5]int = [5]int{90, 80, 70, 80, 65}
       fmt.Println(grades)
       grades[1] = 100
       fmt.Println(grades)
  }
  >>> go run main.go
  [90 80 70 80 97]
  [90 100 70 80 97]
</pre>

**looping through an array**

<pre>
  for i := 0; i less than len(grades); i++ {
                  fmt.Println(grades[i])
                  }
</pre>

<pre>
  package main
  import "fmt"

  func main() {
       var grades [5]int = [5]int{90, 80, 70, 80, 65}
       for i := 0; i <len(grades); i++ {
                fmt.Println(grades[i])
                  }
  }
  >>> go run main.go
  90
  80
  70
  80
  65
</pre>

**looping through an array using range keyword**

<pre>
  for index, element := range grades {
      fmt.Println(index, "=>", element)
  }
</pre>

main.go
<pre>
  package main
  import "fmt"

  func main() {
       var grades [5]int = [5]int{90, 80, 70, 80, 65}
       for index, element := range grades {
          fmt.Println(index, "=>", element)
  }
  >>> go run main.go
  0 => 90
  1 => 80
  2 => 70
  3 => 80
  4 => 65
</pre>

**multidimensional arrays**

1. A multi-dimensional array is an array that has more than one dimension
2. 2-d array

main.go
<pre>
  package main
  import "fmt"

  func main() {
       arr := [3][2]int{{2, 4}, {4, 16}, {8, 64}
       fmt.Println(arr[2][1])
  }
  >>> go run main.go
  64
</pre>
