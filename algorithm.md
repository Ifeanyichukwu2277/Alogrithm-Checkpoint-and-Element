ALGORITHM SentenceAnalysis


VAR

    c       : CHARACTER
    length  : INTEGER
    words   : INTEGER
    vowels  : INTEGER
    inWord  : BOOLEAN


BEGIN

    // Initialize all counters to 0

    length : 0
    words  : 0
    vowels : 0

    // Flag to track if we are currently inside a word
inWord : FALSE

    WRITE("Enter a sentence ending with a point: ")

      // Read and process each character one by one until the period is reached

REPEAT
        
    READ(c)

        // Process only if the character is not the ending period

    IF (c != '.') THEN

            // Count every character except the period
        length : length + 1

            // Word detection using a boolean flag

         IF (c != ' ') THEN

                // We just entered a new word

                IF (inWord = FALSE) THEN
                    words  : words + 1
                    inWord : TRUE

END IF
           
     ELSE
                // Space detected, we are no longer inside a word
                inWord : FALSE

 END IF

            // Vowel check — convert to lowercase to reduce comparisons from 10 to 5
            IF LOWERCASE(c) IN ['a','e','i','o','u'] THEN
                vowels ← vowels + 1
            
END IF

             // Stop the loop when the period is encountered

    UNTIL (c = '.')

    // Display the results

    WRITE("Length  : ", length)
    WRITE("Words   : ", words)
    WRITE("Vowels  : ", vowels)
END

// Input

" i am looking for a city with a true foundation."

// output 

Length  : 48
Words   : 9
Vowels  : 18