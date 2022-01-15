```sh

if [[ <some test> ]]; then
	<commands>
fi
```

Else If is supported as `elif`

Note that `if [ <condition> ];` is different to `if [[ condition ]];`. Singular brackets are an implementation of the program `Test` which is a POSIX utility. Double brackets are a bash keyword which improve on the singular brackets. Generally double brackets are safer, though less portable. 
<sub>Portability is less of an issue at present due to bash being the default shell in many systems</sub>

The below arguments assume double brackets are used

|Category|Argument|Use|
|--------|--------|---|
|String Comparison|`>`|LHS comes after RHS|
|String Comparison|`<`|LHS comes before RHS|
|String Comparison|`=` (or `==`)| LHS is equal to RHS|
|String Comparison|`!=`|LHS is not equal to RHS|
|Integer Comparison|`-gt`|LHS Greater than RHS|
|Integer Comparison|`-lt`|LHS Less than RHS|
|Integer Comparison|`-ge`|LHS Greater than or equal to RHS|
|Integer Comparison|`-le`|LHS Less than or Equal to RHS|
|Integer Comparison|`-eq`|LHS Equal to RHS|
|Integer Comparison|`-ne`|LHS Not Equal to RHS|
|Conditional|`&&`|LHS And RHS|
|Conditional|`||`|LHS Or RHS|
|Expression Grouping|`(...)`|Treat the contents of the parentheses as a single condition|
|Pattern Matching|`=` (or `==`)|Basic pattern matching between LHS and RHS e.g. `[[ xyz = a* ]]`
|Regex Matching|`=~`|LHS matches Regex on RHS|

**Note** that if wanting to use mathematival symbols for arithmetic instead of `-eq` and the like, [[Math Contexts]] should be used