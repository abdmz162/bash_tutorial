
---

#  Introduction to Bash Commands and Scripting
#### By Abdul Muiz

---

## What is Bash?

**Bash** (short for **Bourne Again SHell**) is a command-line interpreter that allows you to interact directly with your computer’s operating system.  
Using Bash, you can manage files, automate tasks, and build powerful workflows — all by typing simple text commands.  
Learning Bash is a rite of passage for anyone serious about mastering Unix-like systems.

---

##  Essential Bash Commands

The following commands form the foundation of working in a Bash environment.

###  File and Directory Management

| Command | Description | Example |
|:---|:---|:---|
| `pwd` | Display the current working directory | `pwd` |
| `ls` | List files and directories | `ls -l` |
| `cd` | Change directory | `cd ~/Documents` |
| `mkdir` | Create a new directory | `mkdir NewFolder` |
| `touch` | Create a new, empty file | `touch notes.txt` |
| `cp` | Copy files or directories | `cp source.txt destination.txt` |
| `mv` | Move or rename files or directories | `mv oldname.txt newname.txt` |
| `rm` | Remove files | `rm file.txt` |
| `rmdir` | Remove empty directories | `rmdir EmptyFolder` |

---

###  Clearing the Terminal

You can clear the terminal screen using:

```bash
clear
```

---

###  Editing Files with Vim

**Vim** is a powerful text editor built directly into the terminal. To create or edit a file:

```bash
vim myfile.sh
```

**Basic Vim commands**:
- Press `i` to **enter Insert mode** (start typing).
- Press `Esc` to **exit Insert mode**.
- Type `:w` to **save** the file.
- Type `:q` to **quit** Vim.
- Type `:wq` to **save and quit** in one step.

---

##  Writing Your First Bash Script

### Step 1: Create a Script File

Open a new file using Vim:

```bash
vim myscript.sh
```

Inside, write the following:

```bash
#!/bin/bash
echo "Hello, world! Welcome to Bash scripting."
```

> The first line (`#!/bin/bash`) is called the **shebang** — it tells the system to use Bash to run the script.

---

### Step 2: Make the Script Executable

Before running the script, you need to make it executable:

```bash
chmod +x myscript.sh
```

---

### Step 3: Run the Script

Execute your script:

```bash
./myscript.sh
```

You should see:

```
Hello, world! Welcome to Bash scripting.
```

Congratulations — you have written and executed your first Bash script.

---

##  Key Concepts in Bash Scripting

| Concept | Description |
|:---|:---|
| `#` | A comment. Used to explain your code. |
| `echo` | Prints text to the terminal. |
| `read` | Takes input from the user. |
| Variables (`$VAR`) | Store and reuse data. |
| `if`, `then`, `else`, `fi` | Conditional logic (decisions). |
| `for`, `while`, `do`, `done` | Loops (repeat actions). |

---

##  Simple Script Examples

###  Greeting the User

```bash
#!/bin/bash

echo "Enter your name:"
read username
echo "Welcome, $username!"
```

---

###  Basic If-Else Example

```bash
#!/bin/bash

echo "Enter a number:"
read number

if [ $number -gt 10 ]; then
    echo "The number is greater than 10."
else
    echo "The number is 10 or less."
fi
```

---

###  Loop Example

```bash
#!/bin/bash

for i in {1..5}
do
    echo "Iteration number $i"
done
```

---

##  Useful Bash Shortcuts

- `&&` → Run the next command **only if** the first one succeeds:

  ```bash
  mkdir TestFolder && cd TestFolder
  ```

- `||` → Run the next command **only if** the first one fails:

  ```bash
  cd Nonexistent || echo "Directory does not exist."
  ```

- `;` → Run multiple commands sequentially:

  ```bash
  echo "First command"; echo "Second command"
  ```

- `$(...)` → Capture the output of a command:

  ```bash
  echo "Today is $(date)"
  ```

---

##  Final Thoughts

Learning Bash is more than learning a set of commands — it is about thinking systematically and automating your work.  
It turns the computer from a passive machine into a powerful tool that bends to your will.


---
