# Getting Started

## Overview

Rivet's goal is to be a very powerful programming language and at the same time easy to
use, with a syntax that is the result of mixing Go + Zig + C#, and by other languages
such as Python, Lua, TypeScript, D, etc.

Rivet uses the C programming language as its main backend.

> Before continuing, I assume you know how to use a console, otherwise you can read this tutorial:
> [The Linux command line for beginners](https://ubuntu.com/tutorials/command-line-for-beginners#1-overview).

## Run the compiler

### Dependencies

* The compiler requires Python 3.

* The Rivet compiler currently generates C code, so a C compiler, which supports C11,
    is required to generate executables. Over time the compiler will add support for
    generating binaries directly without the need for a C compiler.

The compiler has been tested on **linux**.

Just execute ``python3 rivetc some_file.ri``.

You can see all available compiler options by using the ``-h``/``--help`` flag.

``python3 rivetc -h``

## Hello World!

Let's start with the typical ``Hello World!``:

We create a file called ``hello_world.ri`` with the following content:

```swift
import std/console;

func main() {
    console.println("Hello World!");
}
```

Then we compile that file:

```bash
$ python3 rivetc hello_world.ri
```

We'll get an executable called ``hello_world`` as output, so we run it:

```bash
$ ./hello_world
```

We should see this output:

```bash
Hello World!
```

Excellent! You have compiled your first program in Rivet!

## Editor/IDE support

* [LiteXL](https://github.com/lite-xl/lite-xl-plugins/blob/master/plugins/language_rivet.lua)
  (Syntax-highlighting only).
