# Functional Programming Concepts

Functional programming is a programming paradigm. A programming paradigm consists of the rules and design principles of building software; it’s a way of thinking about a programming language. The functional paradigm focuses on building software using pure functions organized in a way that describes what software must do, not how it must do it.

To learn about functional programming we need understanding the 3 principles:

## Immutability

All values are immutable. I use _elixir_ programming language on that example:

```elixir
list = [1, 2, 3, 4]
List.delete_at(list, -1)
# => [4]

list ++ [1]
# => [1, 2, 3, 4, 1]

IO.inspect(list)
# => # => [1, 2, 3, 4]
```

## Pure Functions

Pure function have these properties:

* The value are immutable
* The function result is affected only by the function arguments
* The functions doesn't generate effects beyond the value it returns

A simple example is:

```elixir
add2 = fn (n) -> n + 2 end add2.(2)
# => 4
```

## Declarative Code

Programming declaratively usually generates less code than programming imperatively. Less code means fewer things to write, more things done, and fewer bugs.

To see the diference between imperative and declarative, let’s look at a simple example that transforms a list of strings into uppercase.

That example use imperative mindset with JavaScript
```javascript
var list = ["we", "learning", "about fp"];

function upcase(list) {
    var newList = [];
    for (var i = 0; i < list.length; i++) {
        newList.push(list[i].toUpperCase()); 
    }
    return newList; 
}

upcase(list);
// => ["WE", "LEARNING", "ABOUT FP"]
```

and that example use declarative mindset with elixir
```elixir
defmodule StringList do
  def upcase([]), do: []
  def upcase([first | rest]), do: [String.upcase(first) | upcase(rest)]
end

StringList.upcase(["we", "learning", "about fp"])
# => ["WE", "LEARNING", "ABOUT FP"]
```