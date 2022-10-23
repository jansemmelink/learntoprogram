# [Learn to Program](../../README.md) #
## Print Format Strings ##

Very often we need to print values and text together to create something that will be easy to read.

Say we want to print again:

`My name is Jan. I am 10 years old.`

In this, `Jan` and `10` are my values and you will soon learn that the values can change, then we need to print:

`My name is Joey. I am 12 years old.`

The whole point of a computer program is that it can do that for us very fast and efficient, without us writing the sentence a thousand times for all the names in a list.

This is where formatting becomes important.

We are gong to change the previous program from this:
```
func main() {
	fmt.Print("My name is Jan. ")
	fmt.Print("I am ")
	fmt.Print(10)
	fmt.Println(" years old.")
}
```

to a single statement that substitutes the values into a _format_ string:

```
func main() {
	fmt.Printf("My name is %v. I am %v years old.", "Jan", 10)
}
```

Run that and you will see the same output as we had before, but from a single statement.

The use of `%v` is a placeholder in the string where the values will be substituted.

We can now copy that line and change the values to get more sentences:

```
func main() {
	fmt.Printf("My name is %v. I am %v years old.", "Jan", 10)
	fmt.Printf("My name is %v. I am %v years old.", "Joey", 12)
	fmt.Printf("My name is %v. I am %v years old.", "Chris", 15)
}
```

When you run that, you will notice once again the lines are all printed on one line. That is because `fmt.Printf()` does not automatically move to the next line like `fmt.Println()` does. There is not function to do formatting and print a new linem but we can still tell the program to print a new line by adding the `new-line character` (`\n`) to each format string:

```
func main() {
	fmt.Printf("My name is %v. I am %v years old.\n", "Jan", 10)
	fmt.Printf("My name is %v. I am %v years old.\n", "Joey", 12)
	fmt.Printf("My name is %v. I am %v years old.\n", "Chris", 15)
}
```

The `new-line-character` can be added to any string value. You can even add it to the names, with strange results! Wherever there is a `new-line-character` the program will go to the next line and you can even have a few of them together. If you add two of them to the end of each line, there will be an empty line after each sentence, because the program move to the next line, then, without printing anything it again move to the next line, leaving one line empty:

```
func main() {
	fmt.Printf("My name is %v. I am %v years old.\n\n", "Jan", 10)
	fmt.Printf("My name is %v. I am %v years old.\n\n", "Joey", 12)
	fmt.Printf("My name is %v. I am %v years old.\n\n", "Chris", 15)
}
```

Output:

```
My name is Jan. I am 10 years old.

My name is Joey. I am 12 years old.

My name is Chris. I am 15 years old.

```

For the next sections we will use a log of `fmt.Printf()` statements. If anything is not clear, read this section again.

[Next: Int and String Variables](../int_and_string_variables/README.md)

[Back](../../README.md#getting-started)
