# Compilers

## Practical Class 1 - Regular Expressions in ANTLR Sample Exercises 2024

### 1 - Consider the following CFG grammar,
```
S → aABe
A → Abc | b
B → d
```
where 'a', 'b', 'c' and 'd' are terminals, and 'S' (start symbol), 'A' and 'B' are non-terminals.

**a)** Parse the sentence "abbcde" using right-most derivations.
```
S → aABe → aAde → aAbcde → abbcde
```

**b)** Parse the sentence "abbcde" using left-most derivations.
```
S → aABe → aAbcBe → abbcBe → abbcde
```

**c)** Draw the parse tree.
```
      S - [e]
    / | \ 
  [a] A  B - [d]
    / | \
   A [b] [c]
   |
  [b]
```

### 2 - Consider the following CFG grammar over the non-terminals {X,Y,Z} and terminals {a,c,d} with the productions below and start symbol Z.
```
X → a
X → Y
Z → d
Z → XYZ
Y → c
Y → ε
```
For this grammar compute the FIRST and FOLLOW sets of every non-terminal and the set of non-terminals
that are nullable. Determine if the grammar can be parsed using the table-driven LL parsing algorithm.

Non-terminal | FIRST | FOLLOW
|-|-|-|
X | {a, c, ε} | {$, d}
Y | {c, ε} | {d}
Z | {d, a, c, ε} | {d}

```Y is the only nullable non-terminal.```
