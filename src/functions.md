# Functions

Functions contain a series of arguments, a return type, and a body with
multiple statements.

The way to declare functions in Rivet is as follows:

```swift
func <name>(<args>) [-> return_type] {
	...
}
```

For example:

```swift
func add(a: int32, b: int32) -> int32 {
	return a + b;
}
```

`add` returns the result of adding the arguments `a` and `b`.

Functions can have 0 arguments.

```swift
// `f1` returns a simple numeric value of type `int32`.
func f1() -> int32 {
	return 0;
}

// `f2` takes an argument of type `int32` and prints it to the console.
func f2(a: int32) {
	println("a: {}", a);
}

// `f3` takes no arguments and returns void.
func f3() { }
```

A function body is made up of 1 or more statements and can be empty.

```swift
func x() {
	/* empty body */
}

func y() {
	my_var := 1; // statement
}
```

## Arguments

The arguments are declared as follows: `<name>: <type> [:= default_value]`,
for example: `arg1: int32`, `arg2: bool := false`.

The arguments are immutable.

They can also have default values, this bypasses the need to pass the
argument each time the function is called: `arg1: int32 = 5`.

So, if we have a function called `f5` with a default value argument,
we can call it in 3 ways:

```swift
func f5(arg1: int32 := 5) {
	println("arg1: {}", arg1);
}

f5(); // use the default value `5`
f5(100); // will print 100 instead of 5 to the console

// this uses a feature called `named argument`, which allows an optional
// argument to be given a value by its name in any order
f5(arg1: 500); // will print 500 instead of 5 to the console
```
