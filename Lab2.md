# Samyaak Gharat - Lab 2 (Revised, No Images)

## 2. Script: numbers_loop.sh

### Aim
- This script uses a loop to print numbers from 1 through 5.

### Code
```bash
#!/bin/bash
# A simple loop to display numbers 1–5
for i in {1..5}
do
  echo "Current number: $i"
done
```

### Step-by-step explanation
1. `#!/bin/bash` — specifies Bash as the shell to run this script.
2. `# A simple loop to display numbers 1–5` — comment describing the purpose.
3. `for i in {1..5}` — creates a loop that cycles through numbers 1, 2, 3, 4, and 5.
4. `do` — starts the block of commands to run each iteration.
5. `echo "Current number: $i"` — prints the value of `i` with a message.
6. `done` — marks the end of the loop.

### Example output
```sh
$ ./numbers_loop.sh
Current number: 1
Current number: 2
Current number: 3
Current number: 4
Current number: 5
```

---

## 3. Script: greetings_array.sh

### Aim
- This script demonstrates the use of arrays by greeting each name stored inside it.

### Code
```bash
#!/bin/bash
# Using an array and looping through its values
names=("samyaak" "gharat")
for person in "${names[@]}"
do
  echo "Welcome, $person!"
done
```

### Step-by-step explanation
1. `#!/bin/bash` — runs the script in the Bash shell.
2. `# Using an array and looping through its values` — comment about the script’s purpose.
3. `names=("samyaak" "gharat")` — declares an array with your first and last name.
4. `for person in "${names[@]}"` — iterates through each array element and assigns it to the variable `person`.
5. `do` — starts the commands for each loop cycle.
6. `echo "Welcome, $person!"` — prints a greeting for the current element.
7. `done` — ends the loop.

### Example output
```sh
$ ./greetings_array.sh
Welcome, samyaak!
Welcome, gharat!
```

---

### Question 1 — How do you make a script executable?

By giving execute permission:
```sh
chmod +x my_script.sh
```


