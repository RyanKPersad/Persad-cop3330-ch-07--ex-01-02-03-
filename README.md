 Simple calculator
    This program implements a basic expression calculator.
    Input from cin; output to cout.
    The grammar for input is:
    Calculation:
        Statement
        
        Print
        Quit
        Help
        Calculation Statement
    Statement:
        Declaration
        Expression
    Declaration:
        "let" Name "=" Expression
        "const" name "=" Expression
    Name:
        letter
        letter Sequence
    Sequence:
        letter
        digit
        "_"
        letter Sequence
        digit Sequence
        "_" Sequence
    Print:
        ";"
    Quit:
        "quit"
    Help
        "help"
    Expression:
        Term
        Expression "+" Term
        Expression "-" Term
    Term:
        Primary
        Term "*" Primary
        Term "/" Primary
        Term "%" Primary
    Primary:
        Number
        "(" Expression ")"
        "-" Primary
        "+" Primary
        "sqrt(" Expression ")"
        "pow(" Expression "," Integer ")"
        Name
        Name "=" Expression
    Number:
        floating-point-literal
    Input comes from cin through the Token_stream called ts.