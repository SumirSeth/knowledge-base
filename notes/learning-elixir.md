---
title: "Learning Elixir."
description: "Documenting the process of learning elixir programming language."
tags: ["coding", "programming", "elixir", "learning"]
---

# Learning Elixir

## Overview

Elixir is a **<u>functional, concurrent, fault tolerant</u>** programming language. It is also **immutable** and **pattern-matching first**. Focus is on *scalability*.

- **<u>Functional</u>** : Emphasizes immutability and first class functions.
- **<u>Concurrency</u>** : Uses lightweight processes with message passing for handling thousands of tasks simultaneously. Elixir is explicitly based on Actor model.
- **<u>Fault Tolerance</u>** : Much inspired by Erlang's 'Let it crash' philosophy. This is crucial as this translates to scale, hot fixing and self healing applications.
- **<u>Distributed Computing</u>** : Built in support for running across multiple nodes.
- **<u>Metaprogramming</u>** : Macros allow modifying the language itself.
- **<u>Immutable Data</u>** : Ensures safety in concurrent environments.
- **<u>Dynamic Typing</u>** : Similar to Python and Ruby when it comes to typing.

## Functional Programming

> Ponder: Syntax vs Semantics

Functional languages consist of expressions. It focuses on composition of functions instead of concatenation of commands.

Unspoken rule: Keep your data and keep your functions separate.

**An illustration from *Malte Skarupke*** :

"*To talk about functional programming let’s bake a cake. Taking a recipe from [here](http://allrecipes.com/Recipe/A-Number-1-Banana-Cake/), this is how you bake an imperative cake:*

1. *Preheat oven to 175 degrees C. Grease and flour 2 – 8 inch round pans. In a small bowl, whisk together flour, baking soda and salt; set aside.*
2. *In a large bowl, cream butter, white sugar and brown sugar until light and fluffy. Beat in eggs, one at a time. Mix in the bananas. Add flour mixture alternately with the buttermilk to the creamed mixture. Stir in chopped walnuts. Pour batter into the prepared pans.*
3. *Bake in the preheated oven for 30 minutes. Remove from oven, and place on a damp tea towel to cool.*

*I’d take some issue with the numbering there (clearly every step is actually several steps) but let’s see how we bake a functional cake.*

1. *A cake is a hot cake that has been cooled on a damp tea towel, where a hot cake is a prepared cake that has been baked in a preheated oven for 30 minutes.*
2. *A preheated oven is an oven that has been heated to 175 degrees C.*
3. *A prepared cake is batter that has been poured into prepared pans, where batter is mixture that has chopped walnuts stirred in. Where mixture is butter, white sugar and brown sugar that has been creamed in a large bowl until light and fluffy…*"

### Functions

- Single Values, maybe total maps between sets.

Eg:

```python
def square(x):
	return x*x
```

the above block is a function in python.

Mathematically, you would write it as:

$$f: \Z \longrightarrow \Z$$ such that $x \mapsto x * x$ maps to $f: x \mapsto x*x$ or $f: f(x) = x*x$

This is closer to how functional programming would define functions.

> Functions in this paradigm do not create side effects. For example, a function like `increaseByOne(a) => return a+1` is fine. But doing, `increaseByOne(a) => num = num + 1; return a+1` is not fine. This function changes `num` value as a side effect, assuming you have `num = somevalue` somewhere in the code.

### Anonymous Functions

$(parameters) \mapsto f(parameters)$

eg:

`sum_of_squares` = `(a, b)` $\mapsto$ `sum(square(a), square(b))`

One can use anon functions as inputs and outputs of another functions. For example, `f((x) --> (x+1))` outputs `(x) --> (11)`.

Another example,

`foo = (y) --> (x --> y * x)` : takes  number y, returns a **function** and not a value. The returned functions is a function such that `f(x) = y*x`. Re-iterating, the output of `foo` is `f(x)` and not `y*x` explicitly.

Think about what would be the output of `foo(2)(5)`.

...

It would output, 2*5 = 10. Since `foo(2)` returns a functions that takes an input and returns the input * 2.

`foo(2) --> f(x) = 2 * x`, `f(5) --> 2 * 5 --> 10`.

 ### Iterations and Conditionals

Functional languages use **<u>recursion</u>** instead of iterations. Instead of mutating variables in a loop, functional recursion relies on function calls to process data iteratively.

For example,

To sum a list in python, you would do something like:

```python
def sum_list(lst):
    total = 0
    for num in lst:
        total += num
    return total
```

In Elixir, we replace loops with recursion,

```elixir
defmodule MathUtils do
  def sum_list([]), do: 0  # Base case: sum of empty list is 0
  def sum_list([head | tail]), do: head + sum_list(tail)  # Recursive case
end
```

Here, the function keeps recursively breaking the list until it's empty and then sums the numbers while returning.

What about `if () {}` and other conditional statements?

Conditionals in functional languages:

- Pattern Matching

- Case Expressions

- Guards

**<u>Using Patter Matching instead of `if`</u>** :
Instead of 

```python
def sign(n):
    if n > 0:
        return "positive"
    elif n < 0:
        return "negative"
    else:
        return "zero"
```

In Elixir, we can write:

```elixir
defmodule Sign do
  def check(n) when n > 0, do: "positive"
  def check(n) when n < 0, do: "negative"
  def check(_), do: "zero"
end

IO.puts Sign.check(-5) # Output: "negative"
```

This uses guards ( `when n>0` ) to control flow instead of `if`.

Another alternative to `if` is **<u>Case Expressions</u>** :

```elixir
case x do
  0 -> "zero"
  n when n > 0 -> "positive"
  _ -> "negative"
end
```

## Use Cases

- Pattern Matching + Algebraic data types = Instant interpreters.

#### Reads on functional programming:

- [The Curious Failure of Functional Programming for Parallel Applications | Probably Dance](https://probablydance.com/2014/09/07/the-curious-failure-of-functional-programming-for-parallel-applications/)
- [Functional Programming Is Not Popular Because It Is Weird | Probably Dance](https://probablydance.com/2016/02/27/functional-programming-is-not-popular-because-it-is-weird/)

#### End Note:

The world of functional programming is too vast and crazy, and it definitely does not end here. Explore more using languages like Elixir. At the end of the day, these are just paradigms, OOP is no better or worse then Functional. Take your call.

---

## More on Elixir

### Variables and Pattern Matching

#### Variables

```bash
iex> x = 10
10
iex> y = "Hello"
"Hello"
```

Variables hold value but they do not change like in imperative languages.

#### Pattern Matching

```bash
iex> {a, b} = {1, 2}
{1, 2}

iex> a
1

iex> b
2
```

The tuple {1,2} is matched to {a,b} assigning `a = 1` and `b = 2`

:x: **Invalid Match**

```bash
iex> {x, y} = {1, 2, 3}
```

#### Using `_` to ignore values while matching

```bash
iex> {x, _} = {10, 20}
iex> x
10
```

Here `20` is ignored.

#### Matching lists

```bash
iex> [head | tail] = [1, 2, 3, 4]
iex> head
1
iex> tail
[2, 3, 4]
```

Elixir splits the first element and the rest of the list as `head` and `tail` respectively.

### Functions

#### Anon Functions

```bash
iex> add = fn (a, b) -> a + b end
iex> add.(3, 5)
8
```

Key point

- Function are called using `.` so `add.(3,5)` instead of just `add(3,5)`.

#### Pattern Matching in Function

```bash
iex> compare = fn
...>   0, _ -> "First argument is zero"
...>   _, 0 -> "Second argument is zero"
...>   a, b -> "Neither is zero: #{a} and #{b}"
...> end
```

`_` is used to ignore values.

#### Shorthand Anon Functions

```bash
iex> square = &(&1 * &1)
iex> square.(4)
16
```

Key Points:

- `&1`, `&2`, etc., represent arguments.

- `&(&1 * &1)` is equivalent to `fn x -> x * x end`.

### Named Functions

In Elixir, functions inside modules are defined using `def`.

#### Defining a Simple Module and Function

```elixir
defmodule Math do
  def add(a, b) do
    a + b
  end
end

IO.puts(Math.add(3, 8))
```

Output would be `11`.

- `defmodule` creates a module.
- `def add(a, b)` defines a named function.

#### Functions Arity

Functional overloading is allowed.

```elixir
defmodule Greetings do
  def hello(), do: "Hello, world!"
  def hello(name), do: "Hello, #{name}!"
end
```

For `Greetings.hello()` output would be "Hello, world!"

For `Greetings.hello("Sumir")` output would be "Hello,  Sumir!"

#### Pattern Matching

Similar to anon functions.

```elixir
defmodule Math do
  def multiply(_, 0), do: 0  # If second argument is 0, return 0
  def multiply(a, b), do: a * b #If second argument is non zero, return the product.
 
end
```

#### Recursion in Elixir

Since Elixir avoids loop, recursion is key.

```elixir
defmodule Factorial do
  def calc(0), do: 1
  def calc(n), do: n * calc(n - 1)
end
```

`Factorial.calc(5)` would return `120`.
