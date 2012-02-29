#calculator02buggy.cpp
`5 + (6 ∗ 2)/(8 − 3) =`

When the program is executed `main()` fires and waits for input from the user.  After input is received it is tokenized by `Token_stream::get()` which identifies the input as either an operator, or a number, and creates a new `Token` object for it.  If it comes across a parenthesis, it evaluates that first before evaluating the whole expression.  