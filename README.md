# Electronic Door Lock System (C Implementation)

A C-based console application simulating an **Electronic Door Lock System**. This project demonstrates basic input handling, PIN length validation, attempt tracking, system lockout countdowns using POSIX/C standard libraries, and interactive menu-driven control flow across multi-step development tasks.

---

## 📁 Project Structure

The project is developed in **Code::Blocks** and split across several progressive tasks (`task1.c` to `task4.c` alongside `main.c`):

```text
Assignments/
├── main.c
├── task1.c    # Basic PIN validation (length checking: exact 4 digits)
├── task2.c    # Interactive Door/System menu handling
├── task3.c    # Attempt counting, lockout countdown timer (unistd.h / sleep)
└── task4.c    # Complete integrated Electronic Door Lock System
```

---

## 🚀 Key Features

1. **PIN Length Validation:**
   - Validates that the input PIN is exactly 4 digits.
   - Rejects inputs that are too short (`< 4 digits`) or too long (`> 4 digits`).

2. **Attempt Tracking & Security Lockout:**
   - Limits the user to a maximum number of incorrect PIN attempts (e.g., `MAX_ATTEMPTS = 3`).
   - Tracks remaining attempts dynamically.
   - Enforces a timed security lock (5-second countdown lock using `unistd.h`) upon reaching the maximum allowed failed attempts.

3. **Interactive Control Menu:**
   - Displays system options upon successful PIN authentication:
     1. **Unlock/Lock Door**
     2. **Change Username** *(Feature coming soon)*
     3. **Change PIN**
     4. **Exit System**

---

## 🛠️ Requirements & Setup

### Prerequisites
* A C Compiler (GCC, Clang, or MSVC)
* IDE: [Code::Blocks](https://www.codeblocks.org/) (or any standard C compiler setup)
* standard POSIX header `<unistd.h>` (or `<windows.h>` on Windows if modifying timer functions)

### Compiling and Running
1. Clone or download this repository.
2. Open `Assignments.cbp` in **Code::Blocks**.
3. Select the active build target or task file (e.g., `task4.c` / `main.c`).
4. Click **Build and Run** (`F9`).

---

## 💻 Sample Program Output

### Incorrect Attempts & System Lockout (`task3.c`)
```text
Enter your PIN: 5670
Incorrect PIN. You have 2 attempt(s) left.
Enter your PIN: 2345
Incorrect PIN. You have 1 attempt(s) left.
Enter your PIN: 6780
Incorrect PIN. You have 0 attempt(s) left.
System locked! Wait for 5 seconds...
5...
4...
3...
2...
1...
You can try again now.
```

### Successful Authentication & System Menu (`task4.c`)
```text
=== ELECTRONIC DOOR LOCK SYSTEM ===

Enter 4-digit PIN: 1111
PIN is exactly 4 digits
Incorrect PIN.
Attempts remaining: 2

Enter 4-digit PIN: 0987
PIN is exactly 4 digits

--- SYSTEM MENU ---
1. Unlock Door
2. Change Username
3. Change PIN
4. Exit
Enter your choice (1-4): 1
Access granted. Door unlocked
```

---


