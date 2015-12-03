# eScheme
This is an interpreter implemented in Python for a subset of the Scheme language.

##Usage
Launch a terminal, input ```python3 scheme.py``` to enter the interactive mode ```escm>   ```, then you can type standard scheme commands.

You can find examples in the ```tests.scm``` file.

For instance,

```
python3 scheme.py tests.scm

escm> 10
10
escm> (+ (* 3 (+ (* 2 4) (+ 3 5))) (+ (- 10 7) 6))
57
escm> (+ (* 3
            (+ (* 2 4)
               (+ 3 5)))
         (+ (- 10 7)
            6))
57
escm> (or False (/ 1 0))
Error: division by zero
escm> (or (quote hello) (quote world))
hello
scm> (define fact (lambda (n) (if (<= n 1) 1 (* n (fact (- n 1))))))
fact
scm> (fact 50)
30414093201713378043612608166064768844377641568960512000000000000
escm> ((lambda (x) (display x) (newline) x) 2)
2
2
scm> (define (len s)
       (if (eq? s '())
         0
         (+ 1 (len (cdr s)))))
len
scm> (len '(1 2 3 4))
4
escm> (exit)
```

##Supported Features
* Data types: boolean, number, symbol, pair, list, etc
* Procedures: lambda procedure, user defined procedure, etc
* Expressions: if, and, or, cond, etc
* Operators: addition, multiplication, subtraction, division, relational, logical, etc
