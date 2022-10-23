# [Learn to Program](../../README.md) #
## Int and String Variables ##

In the previous section you learned about values. In a program, we store values in variable, so that we can change the value then use the same code over and over with different values.

For example I define a variable called `name` and in it I store the string value `"Jan"`. Then I write a program that does many things with `name`, then change the name and run the program again with that name, and repeat it a million times with different names from a list...

You will use variables a lot... for everything!

Try this simple example:

```
func main() {
    var name string
    name = "Jan"
	fmt.Printf("My name is %v.\n", name)
}
```

That defines a name, set the value then use it in the print statement.

Now we can change the name and use the same statement many times without changing the print statement:

```
func main() {
    var name string
    name = "Jan"
	fmt.Printf("My name is %v.\n", name)
    name = "Joey"
	fmt.Printf("My name is %v.\n", name)
    name = "Chris"
	fmt.Printf("My name is %v.\n", name)
}
```

Not cool that we had to repeat the print line! But do not worry, we will soon fix that.

Important to note in this program that we first had to declare a variable before we could use it. We also had to tell the program that the variable holds a string value and then we cannot store an integer in that variable - it will be an error and the program will not run.

You can try to store an integer with this change:
```
    var name string
    name = 10
```

The program will fail to run with:

```
./prog.go:9:9: cannot use 10 (untyped int constant) as string value in assignment
```

It says 10 is an `untyped int const` and it cannot be stored in a `string` variable.

We could also create integer variables with the `int` type. Here we have two variables for name (a string) and age (an int) and we set both before each print statement and then print both with two `%v` place holders in the format string:

```
func main() {
	var name string
	var age int

	name = "Jan"
	age = 10
	fmt.Printf("%v is %v years old.\n", name, age)

	name = "Joey"
	age = 12
	fmt.Printf("%v is %v years old.\n", name, age)
}
```

The output is:

```
Jan is 10 years old.
Joey is 12 years old.
```

Go lang also allow you to define variables without declaring them first. In this case you must use `:=` instead of just `=`, and you can only define the variable one. If you try to define the same variable again, the program will not run.

The above can change to:

```
func main() {
	name := "Jan"
	age := 10
	fmt.Printf("%v is %v years old.\n", name, age)

	name = "Joey"
	age = 12
	fmt.Printf("%v is %v years old.\n", name, age)
}
```

So we got rid of the `var name string` variable declaration lines and now name and age are both defined using their first values.

Go is clever enough to realise you store a string in name and an int in age, and therefor Go will not allow you to store other types in them later - just as when you first declared the variables types.

In most of the examples we will define variables like this. It is quicker and less code to write. There are only a few cases where we will use the var declaration first but that will be explained later.

To remember:
- Variables can be declared with a `var name type` statement, or simply define it with a `name := value` statement.
- After a variable was defined, you can change the value with `name = value` but you cannot again use a `:=` on the same variable name.

[Next: Arrays of Integers and Strings](../arrays_of_ints_and_strings/README.md)

[Back](../../README.md#getting-started)
