      https://highon.coffee/blog/penetration-testing-tools-cheat-sheet/#nmap-udp-scanning

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

Printf format values and types

      package main
      import "fmt"
      func main() {
            //v represent for value
            //T represent by Type
            var x = 3
            fmt.Printf("%v\n", x) // 3
            fmt.Printf("%T\n", x) // int

            var x2 = 3.4
            fmt.Printf("%v\n", x2) // 3.4
            fmt.Printf("%T\n", x2) // float64

      }

  Comment golang
  
      package main
      import "fmt"
      func main() {
            // this is a comment - single line
            fmt.Println(3)
            /*  -> multiline
            this is a block comment
            can contain multiple lines
            cannot be nested
            */
      }

Intepreted String Literal

      package main
      import "fmt"
      func main() {
            var x = "ABC and ♥"
            fmt.Println(x)
            // abc and ♥
      }

Literal newline is not allowed

      package main
      import "fmt"
      func main() {
            var x = "ABC \"XYZ\" ♥"
            fmt.Println(x)
            // abc and ♥
      }

If you don't want backslash to have special meaning, use `

      package main
      import "fmt"
      var x = `long text
      many lines
            tab too`

      func main() {
            fmt.Printf("%v\n", x)
            fmt.Printf("%T\n", x)
      }

String Index

      package main
      import "fmt"
      func main() {
            var x = "abc"
            fmt.Printf("%#v\n", x[0]) // 0x61
            fmt.Printf("%#v\n", x[1]) // 0x62
            fmt.Printf("%#v\n", x[2]) // 0x63
      }

String Length - len(string) → returns the number of bytes in string.

      package main
      import "fmt"
      func main() {
            var x = "welcome"
            fmt.Printf("%v\n", len(x))
            fmt.Printf("%T\n", len(x))
      }

Sub-string s[n:m] → returns a substring of s from index n to m (excluding m).
The return value's type is string.

      package main
      import "fmt"
      func main() {
            var x = "012345"
            fmt.Printf("%#v\n", x[2:3]) // "2"
            fmt.Printf("%#v\n", x[2:4]) // "23"
            fmt.Printf("%#v\n", x[2:2]) // ""
      }

Join String - Use + to join string

      package main
      import "fmt"
      func main() {
            fmt.Printf("%v\n", "a"+"b") // ab
      }

Embed Expression in String?

      package main
      import "fmt"
      func main() {
            var name = "John"
            var age = 30
            var x = fmt.Sprintf("Name: %v, Age: %v", name, age)
            fmt.Println(x) // Name: John, Age: 30
      }

import strings function

      package main
      import (
            "fmt"
            "strings"
      )
      var print = fmt.Println
      func main() {
            print(strings.ToUpper("jino"))                                   //uppercase
            print(strings.ToLower("WELCOME TO ALL"))                         //lowercase
            print("ab" == "ab")                                              // 0
            print(strings.Contains("abcd", "bc"))                            // true
            print(strings.HasPrefix("abca", "ab"))                           // true
            print(strings.HasSuffix("abca", "ca"))                           // true
            print(strings.ToLower("ABC") == "abc")                           // true
            print(strings.Trim(" abc ", " ") == "abc")                       // true
            print(strings.Count("abcaab", "ab") == 2)                        // true
            print(strings.Index("abc", "bc") == 1)                           // true
            print(strings.Join([]string{"a", "and", "b"}, " ") == "a and b") // true
            // sprintit into slice
            print(strings.Split("a b c", " "))                               // [a b c]
      }

Variable with Value

    package main
      import "fmt"
      func main() {
            var x = 3
            fmt.Println(x)        // 3
            fmt.Printf("%T\n", x) // int
      }

Variable Parallel Assignment

      package main
      import "fmt"
      func main() {
            var x, y = 3, 4
            fmt.Println(x, y) // 3 4
      }


Variable Scope

Variables in a package are local to the package.
Variables inside function are local to the function.

      package main
      import "fmt"
      // package level variable
      var x = 3
      func main() {
            // function level variable
            var y = 4
            fmt.Println(x, y) // 3 4
      }

Variable Syntax Shortcut Inside Function

      package main
      import "fmt"
      func main() {
            k := 3 // var k = 3
            fmt.Println(k)
      }

Grouping Variable Declaration

      package main
      import "fmt"
      var (
            a int
            b = 2
            c = "some"
            d int
      )
      func main() {
            fmt.Println(a, b, c, d) // 0 2 some 0
      }

Constant variable - Constants are declared like variables, but its value cannot be changed.

      package main
      import "fmt"
      func main() {
            const c1 = 345
            const c2 = true
            var c3 = "JINO" 
            fmt.Println(c1, c2, c3) // 345 true
      }

IF Statement

      package main
      import "fmt"
      func main() {
            var x = 3
            if x > 0 {
                  fmt.Println("yes")
            } 
      }

IF ELSE Statement

      package main
      import "fmt"
      func main() {
            var x = 3
            if x < 0 {
                  fmt.Println("yes")
            } else {
                  fmt.Println("NO)
            }
      }

ELSE IF Statement

      package main
      import "fmt"
      func main() {
            var x = 3
            if x < 0 {
                  fmt.Println(-1)
            } else if x > 0 {
                  fmt.Println(1)
            } else {
                  fmt.Println(0)
            }
      }

IF ELSE statement - Shortform

      package main
      import "fmt"
      func main() {
            var x = 3
            // if statement can start with a short statement
            if i := -2; x < i {
                  fmt.Println("no")
            }
            fmt.Println("yes")
     }


Example program

      import (
            "fmt"
            "os"
            "os/exec"
      )

      func main() {
            if len(os.Args) == 2 {
                  var x = os.Args[1]
                  var cmd = exec.Command(x)
                  output, err := cmd.Output()
                  if err != nil {
                        panic(err)
                  }
                  fmt.Println(string(output))

            } else {
                  fmt.Println("your input is not valid")
                  os.Exit(1)
            }
            fmt.Println("programming end")
      }


example one:
      
      package main
      import "fmt"

      func main(){
          var num[100] int
          var temp,sum,avg int
          fmt.Print("Enter number of elements: ")
          fmt.Scanln(&temp)
          for i := 0; i < temp; i++ {
              fmt.Print("Enter the number : ")
              fmt.Scanln(&num[i])     
              sum += num[i]
          }

          avg = sum/temp
          fmt.Printf("The Average of entered %d number(s) is %d",temp,avg)
      }


      
