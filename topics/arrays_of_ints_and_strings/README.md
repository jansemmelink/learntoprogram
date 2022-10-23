# [Learn to Program](../../README.md) #
## Arrays of Ints and Strings ##

A computer program takes time to write, and is only worth writing if it can repeat something many times over.

We use `arrays` to store lists of values.

Just like a variable that stores an int or a string, we can also create a variable that stores a list of ints or a list of strings!

An array is indicated with block brackets `[]`.

Here is a program that defines a list of three integer numbers and then print the whole list:

```
func main() {
	nrs := []int{5, 6, 7}
	fmt.Printf("nrs: %v\n", nrs)
}
```

The output is:

```
nrs: [5 6 7]
```

Few important things:
- A simple integer type is just `int`
- An array of integers has type `[]int`
- Here we create a variable, specify its type and set the value, all in one statements using: `nrs := []int{5, 6, 7}`.
- When it is printed, Go automatically print it inside block brackets to indicate its a list.

We can do the same with a list of names which is then an `array of strings`:

```
	names := []string{"Jan", "Joey", "Chris"}
	fmt.Printf("names: %v\n", names)
```

The output is:

```
names: [Jan Joey Chris]
```

Note that Go printed the list without quotes. It tries to print it compact, and omits the quotes to save space. Later we will see how to put the quotes back if you want to see them.

To make an array useful, we need to work with each item inside the array. We can get each element with its index, which is the position in the array and a computer number the items from 0, 1, 2, ...

The first nr will be `nr[0]` followed by `nr[1]` and `nr[2]`.

The first name will be `name[0]`, then `name[1]` and then `name[2]`.

We can also see how many entries there are in an array with the `len()` function, for example `len(names)` with have value 3.

We can print all of them by hand writing this:

```
	names := []string{"Jan", "Joey", "Chris"}
	fmt.Printf("names: %v\n", names)
	fmt.Printf("name: %v\n", names[0])
	fmt.Printf("name: %v\n", names[1])
	fmt.Printf("name: %v\n", names[2])
```

With this output:

```
names: [Jan Joey Chris]
name: Jan
name: Joey
name: Chris
```

That is poor programming because if somehow another name is added to the end of the list, your program will still only print the first 3 names!

For that, we use `iteration`, which simply means the program is going to repeat something for each item in the array.

Try this program to iterate over and print all the names:

```
	fmt.Printf("There are %v names:\n", len(names))
	for index, name := range names {
		fmt.Printf("name[%v] = %v\n", index, name)
	}
```

The output is:
```
There are 3 names:
name[0] = Jan
name[1] = Joey
name[2] = Chris
```

Now you can update the definition of names to add any number of names, and you program will tell you how many there are and print all of them, everytime!

Exercise: Try to do the same with the `nrs` array to print this:

```
There are 3 nrs:
nr[0] = 5
nr[1] = 6
nr[2] = 7
```

[Next: Working with Arrays](../working_with_arrays/README.md)

[Back](../../README.md#getting-started)
