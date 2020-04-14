Print Format

      package main
      import "fmt"
      func main() {
            fmt.Print("hello world")
      }

Print line format 

      package main
      import "fmt"
      func main() {
        fmt.println("hello world")
      }

Print Format view - represent Printf

      package main
      import "fmt"
      func main() {
            fmt.Printf("there are %v apples\n", 3)
            var x = "John"
            var y = 36
            fmt.Printf("name is %v, age is %#v\n", x, y)
      }

Print - it return a string instead of printing.

      package main
      import "fmt"
      func main() {

            var x = "gino"
            var y = 36
            var s = fmt.Sprintf("name is %v, age is %v\n", x, y)
            fmt.Println(s == "name is gino, age is 36\n") // true
      }
      
  
 Print - it return a string instead of printing.

      package main
      import "fmt"
      func main() {

            var x = "gino"
            var y = 36
            var s = fmt.Sprintf("name is %v, age is %v\n", x, y)
            fmt.Println(s == "name is jino, age is 36\n") // false
      }
      
