## Variables

Last lecture we learn about data types in this will see how to store data in varaible <br>

It is named unit of data and has assigned value, refernece of values<br>

name-->"Peter"<br>
pincode-->900900<br>
grades-->99.08<br>

If you change the values of variables, name remain same.<br>

name-->"Peter"<br>
pincode-->900900<br>
grades-->99.08<br>

__Syntax__

var
`<variable name> <data type> = <value>`<br>
var
`s string = "hello World"`<br>
var
`i int = 100`<br>
var
`b bool = false`<br>
var
`f float64 = 77.90` <br>

__Example__

main.go <br>
<pre>
package main 
import ("fmt") 
func main () { 
   var greeting string = "Hello World"
   fmt.Println(greeting)
}
>>> go run main.go
Hello World
</pre>



