## Arithmetic Expansion
`$((<SomeArithmeticOperation>))`

The `$(( ))` syntax is called an "Arithmetic Expansion" denotes a *math context* it's performed following the same syntax as C. It obeys the same basic rules as all `$...` substitutions.

**Note:** Bash only allows integer math. Floating point math is not possible. Floating point must be done with the assistance of an external program e.g. `awk` or `dc`

## Arithmetic Commands
In addition to Arithmetic Expansion, Bash offers two Arithmetic *Commands* that use a *math context*. The first of which is `let`:
```sh
let a=17+23
```
Each expression must be passed as a single argument to the let command, if there are spaces or globbing characters quotes are required e.g.
```sh
let a='17 + 23'		# Quoted Single Arithmetic Expression
let a=17 a+=23		# Two Arithmetic Expressions
let 'a[1]=1+1'		# a[1] is a Globbing expression and must be quoted
```

The second command is `(( ))`. This works identically to `let` but has no need to quote expressions as they are delimited by the `((` and `))` syntax.

The `(( ))` syntax works well with `if`/`while` commands and therefore is used more widely than `let`.