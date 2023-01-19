# Statements

Each statement must end with a semicolon.

## Variables

Variables are like boxes that contain values.

Variables are declared as follows: `[mut] <name>[: <type>] := <value>;`.
Example:

```rust
x: i32 := 1;
```

We have created a variable called `x`, which contains the value 1 and is
of type `i32`.

The type of the variable can be omitted.

```rust
x := 1; // via inference, the compiler knows that `x` is an `i32`.
```

By default, all variables are immutable, that is, their values do not change.
To change the value of a variable you have to declare it with `mut`.

```rust
mut x := 1;
x = 2; // this is valid

y := 1;
y = 2; // error: `y` is immutable
```

Multiple values can be assigned on a single line via tuple-destructuring, example:

```rust
(a, b, c) := (1, 2, 3);
(c: i32, d: i32, e: i32) := (4, 5, 6);
(f, g, h) := tuple_fn();

// this is a short form for:

a := 1;
b := 2;
c := 3;

c: i32 := 4;
d: i32 := 5;
e: i32 := 6;

tmp_tuple_fn := tuple_fn();
f := tmp_tuple_fn.0;
g := tmp_tuple_fn.1;
h := tmp_tuple_fn.2;
```
