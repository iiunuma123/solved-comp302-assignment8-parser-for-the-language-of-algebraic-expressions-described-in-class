Download Link: https://assignmentchef.com/product/solved-comp302-assignment8-parser-for-the-language-of-algebraic-expressions-described-in-class
<br>
<strong>Question 1</strong>In this question you will implement a parser for the language of algebraic expressions described in class. We use the following type definition to capture expression trees:

type exptree = Var of char | Expr of char * exptree * exptree

The input will be just plain strings and the output has to be an exptree. The input strings consist of simple algebraic expressions with + and * and <strong>one-character </strong>symbols that are just lower-case letters. It is also possible to use parentheses in the input expressions. <strong>Blanks are not allowed in the input</strong><a href="#_ftn1" name="_ftnref1"><sup>[1]</sup></a>. The parser itself will consist of three mutually recursive functions as explained in class. There is a template installed in the LearnO’Caml system with more details. I will put a file with examples on the course web page. I am interested in making sure that the parser works correctly on valid input strings, I won’t worry about dealing with bad strings and implementing error handling. I have not written the parser to detect all the possible problems. In the file called examples.ml you will see that not all bad strings are reported as bad strings, one simply gets the wrong parse tree. The most complicated part is the recursive procedure called primary which I have written for you. This is defined together with expr and term as three mutually recursive functions.

<strong>Question 2</strong>] In this question you will implement a toy code generator for the very simple stack machine as explained in class. Use the output from the parser as input to the code generator. The code generator should just print the “machine instructions”. Use statements like

Printf.printf “LOAD %c
” c

Printf.printf “ADD %c
” c

Printf.printf “MUL %c
” c

Printf.printf “STORE %i
” tempstore Printf.printf “ADD %i
” tempstore

within your program to get this effect.

1

<a href="#_ftnref1" name="_ftn1">[1]</a> If you want to do something fancier please do so on your own <strong>but do not submit it!</strong>