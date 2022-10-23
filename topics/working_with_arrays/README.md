# [Learn to Program](../../README.md) #
## Working with Arrays ##

We start again with an array of numbers:
```nrs := []int{5, 6, 7}```

When we iterate over the numbers, we can add them together to get the total sum of all the numbers, which will be 5+6+7 which is 18:

```
func main() {
	nrs := []int{5, 6, 7}
	sum := 0
	for _, nr := range nrs {
		sum = sum + nr
	}
	fmt.Printf("The sum of %v numbers %v is %v\n", len(nrs), nrs, sum)
}
```

Notes in that program:
- We defined the nrs array as before.
- We defined a new integer variable `sum` with value 0.
- Then we iterate over all the numbers in the array, and add them to the sum.
- Finally we print a nice summary of what we calculated.

The output is:
```
The sum of 3 numbers [5 6 7] is 18
```

Note how we calculate the sum of the numbers. It is a very common thing to do in programming:
- We define a variable to store the sum
- We set its value to 0
- We iterate and add each value to it, saying `sum = sum + nr` which means we take the sum that we already got, add this nr, then store that again in sum. This value will then be used in the next iteration to also add the next number and the next etc.

Let's use a few more numbers in random order, and determine the minimum and maximum values:

```
	nrs := []int{9, -7, 30, 20, -5, 6, 7}
	sum := 0
	min := 0
	max := 0
	for _, nr := range nrs {
		sum = sum + nr
		if nr < min {
			min = nr
		}
		if nr > max {
			max = nr
		}
	}
	fmt.Printf("The sum of %v numbers %v is %v, min is %v, max is %v\n", len(nrs), nrs, sum, min, max)
```

The output is:

```
The sum of 7 numbers [9 -7 30 20 -5 6 7] is 60, min is -7, max is 30
```

Note again how we calculcated the min and max, by defining a value outside the loop and in each iteration, now also check if the nr is smaller than the min or bigger than the max. At the end, we know the min and max and sum.

BUT! There is a bug.

If you run the same program with the following values, you will see the bug:

```
nrs := []int{1,2,3,4}
```
And run it also with:
```
nrs := []int{-1,-2,-3,-4}
```

When the nrs are all greater than 0, the minimum will report 0. And when the numbers are all less than zero, the max will be reported as 0.

Why is that?

It is because we initialise the min and max at 0. So if no number is smaller than 0, we will never change the min value and it was say min=0 even though all the nrs are more than 0. Similar for max.

To fix that, we must use the first value as the min and max, not 0:

We can change the program to initialise min and max like this:

```
	min := nrs[0]
	max := nrs[0]
```

Now if you test with the above, the report will be correct.

But there is still one more thing that can break that program.

When an array has one item, we can get its value with index 0, e.g. `nrs[0]` is the first number.

We can always do that when there is one or more items in the array.

Similarly we can get the second item with `nrs[1]` as long as there are *two* or more items in the array.

So when the array is empty, our program will fail because then there is no `nrs[0]` to use for min and max.

To make the program work in all cases, we must not determine min or max when the array is empty. For now, we can just put all the number processing inside an if-statement like this, so the program will only do that processing if the array is not empty.

```
	nrs := []int{9, -7, 30, 20, -5, 6, 7}
	if len(nrs) > 0 {
		sum := 0
		min := nrs[0]
		max := nrs[0]
		for _, nr := range nrs {
			sum = sum + nr
			if nr < min {
				min = nr
			}
			if nr > max {
				max = nr
			}
		}
		fmt.Printf("The sum of %v numbers %v is %v, min is %v, max is %v\n", len(nrs), nrs, sum, min, max)
	}
```

[Back](../../README.md#getting-started)
