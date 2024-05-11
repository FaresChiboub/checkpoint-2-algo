# Algorithm: AlgorithmAnalysis

## Variables:
- `i`: INTEGER := 0
- `j`: INTEGER := 0
- `Set1`: ARRAY := [3, 1, 7, 9]
- `Set2`: ARRAY := [2, 4, 1, 9, 3]
- `sum`: INTEGER := 0
- `notfound`: BOOLEAN

## Begin
- FOR `i` from 0 to `Set1.length - 1`
  - `notfound` := TRUE  <!-- Reset `notfound` for each element in `Set1` -->
  - FOR `j` from 0 to `Set2.length - 1`
    - IF `Set1[i] ≠ Set2[j]` THEN
      - `notfound` := TRUE  <!-- Set `notfound` to FALSE if the element is present in `Set2` -->
    - ELSE 
      - `notfound` := FALSE
    - END_FOR
  - IF (`notfound = TRUE`) THEN
    - `sum` := `sum + Set1[i]`
  - END_IF
- END_FOR

- FOR `j` from 0 to `Set2.length - 1`
  - `notfound` := TRUE  <!-- Reset `notfound` for each element in `Set1` -->
  - FOR `i` from 0 to `Set1.length - 1`
    - IF `Set2[j] ≠ Set1[i]` THEN
      - `notfound` := TRUE  <!-- Set `notfound` to FALSE if the element is present in `Set2` -->
    - ELSE 
      - `notfound` := FALSE
    - END_FOR
  - IF (`notfound = TRUE`) THEN
    - `sum` := `sum + Set2[j]`
  - END_IF
- END_FOR

     
      
