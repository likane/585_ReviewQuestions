Go Reinforcement Practice

1. Who created Go and in what year?

Robert Griesemer
Rob Pike
Ken Thompson
google/2009

2. What is the url of the Go Language Home Page?
https://golang.org/

3. What kinds of problems was Go created to solve?
Google sized problems

4. Go programs begin by calling a function called ________________ inside a package called ________________.
main/main

5. What line of code writes "Hello, world??
package main

import "fmt"

func main() {
	fmt.Println("Hello, 世界")
}

6. Must every Go file have a package declaration or is it optional?
yes.

7. How do you get the command line arguments in a Go program?
argsWithProg := os.Args
argsWithoutProg := os.Args[1:]

8. How do you split a string s on separator sep? How do you join the elements of s with separator sep?
s := strings.Split("a,b,c", ",")
 // Create a slice and append three strings to it.
    values := []string{}
    values = append(values, "cat")
    values = append(values, "dog")
    values = append(values, "bird")

    // Join three strings into one.
    result := strings.Join(values, "...")


9. How do you pronounce the type []int?
Array of type int

10. What does the conditional expression look like in Go?
if(condition) {
	// Code to be executed if the condition is true.
}

11. How do you swap the values of two variables?
a, b := "second", "first"
fmt.Println(a, b) // Prints "second first"
b, a = a, b

12. Show four different syntaxes for declaring a local variable found with initial value false.
k := false
var k = false

var i bool
i = false

13. Can a variable ever be underfined in Go?
yes

14. How do you write a while-loop in Go?
sum := 1
	for sum < 1000 {
		sum += sum
	}
15. How do you iterate through the indices of array a?
a := []string{"Foo", "Bar"}
for i, s := range a {
    fmt.Println(i, s)
}

16. How do you iterate through the values of array a?

a := []string{"Foo", "Bar"}
for _, s := range a {
    fmt.Println(s)
}

17. Name all of the built-in integer types in Go. Include all aliases.
uint8 , uint16 , uint32 , uint64 , int8 , int16 , int32 and int64. 8, 16, 32 and 64

18. Name all of the built-in floating point and complex number types in Go.
loat32 and float64 (also often referred to as single precision and double precision respectively) as well as two additional types for representing complex numbers (numbers with imaginary parts): complex64 and complex128 .

19. For each of the following types, give their default values: int32, complex128, bool, string.
int32 -- 0
complex128 -- 0.0
bool -- false
string -- " "


20. What is the value of len("こんにちは世界")? Why is it not 7? What expression, using len and the string "こんにちは世界", does give 7?
TODO

21. Name the 8 composite types of Go.
array, struct, pointer, function, interface, slice, map, and channel

22. What are the default values of the types [3]bool, []string, struct {X int; Y string}, map[string][float64]?
TODO

23. What are the default values of the types func(int)int, *complex128*, interface{}, chan bool?
TODO