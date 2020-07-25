# Basic Types in Elixir
Learning Basic Types

### Integers
>Support for binary, octal and hexadecimal numbers

255,
10,
0b0110,
0x1F

## Floats
>Float numbers require a decimal after at least one digit.
>It support **e** for exponent values

1.4,
5.5,
1.0e-10

## Booleans
>Everything is truthy except for **false** and **nil**

true,
false,
!!:test

## Atoms
>Atom is a constant whose name is its value. Names of modules are also atoms.

:development,
:elixir,
true,
false,
is_atom(App.ModuleName)

## Strings
>Strings are **UTF-8** encoded and are wrapped in double quotes

"Hello",
"Olá"