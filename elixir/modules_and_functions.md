# Modules and Functions

On elixir, we always use functions and modules. An module is group of functions.
So, it's an example of a module in elixir:

```elixir
	defmodule Calculate do
		# It's multiple lines function example
		def sum(number1, number2) do
			# We can having multiple lines on this function
			IO.puts(number1 + number2)
			IO.puts say_thanks()
		end

		# It's one line function example
		def sub(number1, number2), do: IO.puts(number1 - number2)

		# It's a private function example
		defp say_thanks(), do: IO.puts "Thank you!"
	end
```
On that example we can call method on our terminal with the command:

```bash
iex(2)> Calculate.sum(1,3)
4
Thank you!

$ Calculate.sub(5,1)
4
```
