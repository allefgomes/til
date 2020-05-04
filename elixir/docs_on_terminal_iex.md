# Documentation on terminal iex

To enter on a elixir terminal you can run:

```bash
  $ iex
```

Then, to show documentation of a specific function you can use _h_ like that example:


```bash
  $ h round/1

  # =>                              def round(number)                                

  # => @spec round(number()) :: integer()

  # => guard: true

  # => Rounds a number to the nearest integer.

  # => If the number is equidistant to the two nearest integers, rounds away from zero.

  # => Allowed in guard tests. Inlined by the compiler.
  ## Examples

      iex> round(5.6)
      # => 6
      
      iex> round(5.2)
      # => 5
      
      iex> round(-9.9)
      # => -10
      
      iex> round(-9)
      # => -9
      
      iex> round(2.5)
      # => 3
      
      iex> round(-2.5)
      # => -3

```
In this case, _round/1_ is a function called *round* that recieves an argument/arity.
