# Code Structure

## Comments
```swift
// This is a single line comment.
/*
This is a multiline comment.
*/
```

You can use comments to make reminders, notes, or similar things in your
code.

## Entry point

In Rivet, the entry point of a program is a function named `main`.
```swift
func main() {
    // code goes here
}
```

## Top-level declarations

On the top level only declarations are allowed.
```swift
import "module" { import_list, ... };

const Foo: int32 = 0;

let Foo: int32 = 0;

type Foo = int32;

trait Foo { /* ... */ }

struct Foo { /* ... */ }

enum Foo { /* ... */ }

extend Foo { /* ... */ }

func foo() { /* ... */ }

test "Foo" { /* ... */ }
```
