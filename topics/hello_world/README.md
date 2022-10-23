# [Learn to Program](../../README.md) #
## Hello World! ##

This is usually the first program anyone writes when they learn a computer language.

When you open the Playground the first time, the Hello World program will already be written for you, albeit with a few funny characters in the message:

```
// You can edit this code!
// Click here and start typing.
package main

import "fmt"

func main() {
	fmt.Println("Hello, 世界")
}
```

All you need to do now is click on the [Run] button at the top of the window.

It will say `Waiting for remote server ...` for a while and there after the program will run to print the message `Hello, 世界`.

After that it will say `Program exited.` which is not part of your program. It just tells you your program stopped and is no longer running.

This was very simple... you just clicked [Run]!

Let's look at the program before you change is:

1. Any line starting with `//` are called comments. This is just for us humans to make a few notes in our own language and the computer is not going to read that. You can write any thing in those line after the `//`.
1. The first line of the program is `package main`. That line is required and must be exacly like that, and it must be first. It tells the computer this is your main program.
1. `import "fmt"` is also required to tell the computer you are using the package called `fmt` in your program. See point 5.
1. The line `func main() {` is the beginning of your program and your program ends where the closing `}` is on the last line. Everything betweeh the `{` and `}` are instructions that the computer with execute when the program runs.
1. The only instruction in the program currently is `fmt.Println("...")` which tells the computer to print the text inside the quotes.

Make the following changes to this program to see the effects. After each change, click [Run] to see how the output has changed.

1. Change the "Hello, 世界" to be something else, like "Hello South Africa!". When you click run, you will see the message changed.

1. Copy and paste the line a few times and run again. You will see the program print it as many times as you pasted it.

1. You can change some of those lines ... and you know what will happen :-).

1. Now a bigger change: Change `fmt.Println` to `fmt.Print`. When you run, you will notice that all the lines you printed are printed after one another, not below each other!

Program:
```
package main

import "fmt"

func main() {
    fmt.Print("Hello South Africa")
    fmt.Print("Hello Spain")
    fmt.Print("Hello Hong Kong")
}
```

Output:
```
Hello South AfricaHello SpainHello Hong Kong
```

That is no coincidense. The previous function was Println and the `ln` letters stands for `line` so when we talk, we read that function as `print line` and it automatically print AND move to the next line. Without that, it only prints and stays on the current line.

It may sound silly at first, but you will soon learn this is very powerful...

[Next: Integer and String Values](../int_and_string_values/README.md)

[Back](../../README.md#getting-started)