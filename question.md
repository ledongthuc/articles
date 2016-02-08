# Question
This is list question that I gather with golang

### 1. What value will be printed in screen? And why?
```
package main

import "fmt"

type Person struct {
	Age int
}

func (p Person) SetAge(newAge int) {
	p.Age = newAge
}

func main() {
	benGurion := &Person{
		Age: 10,
	}
	benGurion.SetAge(11)
	fmt.Println(benGurion.Age)
}
```

### 2. Which line of code will through error, and why?
```
package main

import "fmt"

type Dog struct {
	Age int
}

func (d *Dog) Growl() {
	fmt.Println("Bow wow	")
}

func main() {
	var realDog *Dog = nil
	realDog.Growl()
	realDog.Age = 10
}
```