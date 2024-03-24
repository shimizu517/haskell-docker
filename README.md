# How to execute Haskell in various ways using docker.

## GHCi
```bash
docker run -it --rm haskell
```

## Execute .hs file.
```bash
docker run -it --rm -v $(pwd)/app:/app --entrypoint bash -w /app haskell
runhaskell ./baby.hs
```

## Compile .hs file and execute it.
```bash
docker run -it --rm -v $(pwd)/app:/app --entrypoint bash -w /app haskell
ghc baby.hs
```

## Start ghci and load module(baby.hs)
```bash
docker run -it --rm -v $(pwd)/app:/app --entrypoint bash -w /app haskell
ghci
:l baby.hs
```

# Haskell basic syntax examples.

| operation                         | e.g.,                 | e.g., result    |
| --------------------------------- | --------------------- | --------------- |
| addition of numbers               | 1 + 1                 | 2               |
| subtraction of numbers            | 5 - 3                 | 2               |
| multiplication of numbers         | 2 * 4                 | 8               |
| division of numbers               | 10 / 2                | 5               |
| exponentiation                    | 2 ** 3                | 8               |
| negation of a number              | -5                    | -5              |
| equality comparison               | 3 == 3                | True            |
| inequality comparison             | 4 /= 3                | True            |
| greater than comparison           | 5 > 3                 | True            |
| less than comparison              | 2 < 4                 | True            |
| logical AND                       | True && False         | False           |
| logical OR                        | True \|\| False       | True            |
| logical NOT                       | not True              | False           |
| concatenation of strings          | "Hello, " ++ "world!" | "Hello, world!" |
| access element in a list          | [1, 2, 3] !! 1        | 2               |
| check if element is in a list     | elem 3 [1, 2, 3]      | True            |
| take first n elements from a list | take 2 [1, 2, 3]      | [1, 2]          |
| drop first n elements from a list | drop 2 [1, 2, 3]      | [3]             |
| reverse a list                    | reverse [1, 2, 3]     | [3, 2, 1]       |
| define a function                 | double x = x * 2      |                 |
| call a function                   | double 5              | 10              |


# Haskell advanced syntax examples.

| operation          | e.g.,                                               | e.g., result     |
| ------------------ | --------------------------------------------------- | ---------------- |
| currying           | add x y = x + y                                     |                  |
|                    | add5 = add 5                                        |                  |
|                    | add5 3                                              | 8                |
| composite function | square x = x * x                                    |                  |
|                    | doubleSquare x = square (2 * x)                     |                  |
|                    | doubleSquare 3                                      | 36               |
| pattern matching   | factorial 0 = 1                                     |                  |
|                    | factorial n = n * factorial (n - 1)                 |                  |
|                    | factorial 5                                         | 120              |
| lambda function    | (\x -> x + 1) 5                                     | 6                |
| list comprehension | [x * 2 \| x <- [1..5]]                              | [2, 4, 6, 8, 10] |
| recursion          | fibonacci 0 = 0                                     |                  |
|                    | fibonacci 1 = 1                                     |                  |
|                    | fibonacci n = fibonacci (n - 1) + fibonacci (n - 2) |                  |
