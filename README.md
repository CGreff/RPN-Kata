# Reverse Polish Notation Converter
## Description
The Reverse Polish Notation Converter describes a library with an API that can convert
between expressions of an 'infix' and a 'postfix' form. This means that it can take the string
'a+b' and turn it into 'ab+' or vice versa. 

## API
A library is provided that includes public methods to convert either from an infix to a postfix
expression, or a postfix to an infix expression.
These are:


## Strategy
This solution aims at using a binary syntax tree as the underlying data structure for an
expression. This means that the expression: 'a+(b-c)' is stored as a tree of this format:
          +
    a            -
            b         c 

This tree can then be easily output as either an infix or postfix expression, simply by
changing how you traverse it. An 'in-order' traversal of the tree will output the infix
expression, while a 'post-order' traversal of the tree outputs the postfix Reverse Polish
Notation expression of 'abc-+'.
