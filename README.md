# Sentence Analysis Algorithm


## Description
A pseudocode algorithm that reads a sentence character by character and analyzes it.


## What it does
Given a sentence ending with a period, the algorithm determines:
- The **length** of the sentence (number of characters)
- The **number of words** (detected character by character using a boolean flag)
- The **number of vowels** (case-insensitive check)

## Algorithm
```
ALGORITHM SentenceAnalysis
VAR
    c       : CHARACTER
    length  : INTEGER
    words   : INTEGER
    vowels  : INTEGER
    inWord  : BOOLEAN
BEGIN
    length ← 0
    words  ← 0
    vowels ← 0
    inWord ← FALSE

    WRITE("Enter a sentence ending with a point: ")

    REPEAT
        READ(c)
        IF (c ≠ '.') THEN
            length ← length + 1
            IF (c ≠ ' ') THEN
                IF (inWord = FALSE) THEN
                    words  ← words + 1
                    inWord ← TRUE
                END IF
            ELSE
                inWord ← FALSE
            END IF
            IF LOWERCASE(c) IN ['a','e','i','o','u'] THEN
                vowels ← vowels + 1
            END IF
        END IF
    UNTIL (c = '.')

    WRITE("Length  : ", length)
    WRITE("Words   : ", words)
    WRITE("Vowels  : ", vowels)
END
```

## Example
**Input:** `Welcome to YUMYUM.`

**Output:**
```
Length  : 17
Words   : 3
Vowels  : 6
```

## Key Concepts
- Characters are read one by one
- Words are counted using a `BOOLEAN` flag (`inWord`) instead of counting spaces
- Vowel check uses `LOWERCASE()` to reduce comparisons from 10 down to 5
- The period is not counted in the length
```