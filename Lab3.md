# Samyaak Gharat - Lab 3 (No Images)

## ✅ Script: enhanced_numbers.sh

### Code

``` #!/bin/bash
# Script to print numbers from start to end with a given step

# Take user inputs
read -p "Enter start value: " start
read -p "Enter end value: " end
read -p "Enter step value: " step

# Validate inputs
if ! [[ "$start" =~ ^-?[0-9]+$ && "$end" =~ ^-?[0-9]+$ && "$step" =~ ^[0-9]+$ ]]; then
    echo "Error: Inputs must be integers, and step must be a positive integer."
    exit 1
fi

if [ "$step" -le 0 ]; then
    echo "Error: Step must be greater than zero."
    exit 1
fi

# Print numbers
echo "Printing numbers from $start to $end with step $step:"
for (( i=$start; i<=$end; i+=$step ))
do
    echo "$i"
done ```

### Make it executable
```bash
chmod +x enhanced_numbers.sh
```

### Example Run
```bash
Number:1
Number:2
Number:3
Number:4
Number:5
Number:6
Number:7
Number:8
Number:9
Number:10
```

---

## Modified Script (enhanced_numbers.sh)

### Purpose
- Print numbers based on user-defined start, end, and step.

### Features
- **Input:** User enters values at runtime.
- **Validation:**
  - Step must be a positive integer.
  - All inputs must be integers.
- **Output:** Prints the sequence according to user input.

### Example Runs
```sh
$ ./enhanced_numbers.sh
Enter start: 1
Enter end: 10
Enter step: 2
1 3 5 7 9

$ ./enhanced_numbers.sh
Enter start: 5
Enter end: 20
Enter step: 5
5 10 15 20
```

---

### Question 1 — Difference between $1, $@, and $# in Bash?

- **$1** → Refers to the first argument passed to the script.
  ```bash
  #!/bin/bash
  echo "First argument: $1"
  ```
  Run:
  ```sh
  $ ./script.sh apple banana cherry
  First argument: apple
  ```

- **$@** → Represents all arguments passed to the script (as separate words).
  ```bash
  #!/bin/bash
  echo "All arguments: $@"
  ```
  Run:
  ```sh
  $ ./script.sh apple banana cherry
  All arguments: apple banana cherry
  ```
  If arguments have spaces:
  ```sh
  $ ./script.sh "red apple" banana
  All arguments: red apple banana
  ```

- **$#** → Shows the total number of arguments.
  ```bash
  #!/bin/bash
  echo "Number of arguments: $#"
  ```
  Run:
  ```sh
  $ ./script.sh apple banana cherry
  Number of arguments: 3
  ```

---

### Question 2 — What does `exit 1` mean in a script?

- `exit 1` terminates the script with a **status code of 1**.
- By convention:
  - `exit 0` → Success (script executed without issues).
  - `exit 1` (or any non-zero value) → Error/Failure (something went wrong).

---
