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
  [a]  A  B - [d]
     / | \
    A [b] [c]
    |
   [b]
```
