# [Learn to Program](../../README.md) #
## Integer and String Values ##

A computer program is all about values and every value has a type.

### Strings ###
The following are examples of _string_ values and we always write them inside double-quotes:
- `"Jan"`
- `"Sunflower"`
- `"Good morning my friend!"`

A string can be any text, and it may even have special characters as we saw in the Hello World example where we printed a string:

`"Hello, 世界"`

### Integers ###
The following are examples on _integer_ values:
- `1`
- `2`
- `0`
- `-6`
- `10000`
- `-32211`

Integer values are whole numbers and they can be positive or negative. We never write a `+` infront of a positive number, but we do write a `-` infront of a negative number.

## Print Values ##

Write this simple program to show you have we can print integer and string values.

You can copy and paste the program to save time, but you should not. When you copy and paste, you will miss subtle things, brackets and quotes that are very important. You will get quicker through the training, but when you have to write your own program, you will struggle.

So...

*** DO NOT COPY AND PASTE ***

*** WRITE THEM YOURSELF ***


Reminder:
- a Go program must always start with the first line `package main`
- since we use the `fmt` package, it must also have a next line `import "fmt"` and then the main program function.

```
package main

import "fmt"

func main() {
	fmt.Println("My name is Jan")
	fmt.Println("I am")
	fmt.Println(10)
	fmt.Println("years old.")
}
```

The output is:
```
My name is Jan
I am
10
years old.
```

You have printed a string in the first two and the last line and an integer in the 2nd last line.

Again, might look trivial but you need to understand there are different types, and both can be printed.

### Exercise ###
Can you guess how one should change the program to print like this, still using 4 statements?

```
My name is Jan. I am 10 years old.
```

Answer:
```
func main() {
	fmt.Print("My name is Jan. ")
	fmt.Print("I am ")
	fmt.Print(10)
	fmt.Println(" years old.")
}
```

Changes:
- The first 3 instructions changed from `Println()` to only `Print()` so they do not jump to the next line.
- I also added a dot and space to the first line, to separate it from the start if the next sentence "I am ...".
- I added a space before "years old" as well.

Note that a space inside the quotes will be printed:
```fmt.Println(" years old.")```

A space outside the quotes has no meaning and the compute will ignore it:
```fmt.Println( "years old.")```

[Next: Print Format Strings](../int_and_string_values/README.md)

[Back](../../README.md#getting-started)