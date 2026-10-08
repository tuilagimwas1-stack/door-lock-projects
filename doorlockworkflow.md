# Electronic Door Lock System — Task Evidence & Documentation

This repository serves as complete evidence for the implementation and testing of the **Electronic Door Lock System** C program. Below is a breakdown of each task, including the corresponding execution output and visual evidence.

---

## 📋 Task 1: Basic Input Validation (PIN Length Check)

**Objective:** Validate the length of the entered PIN to ensure it meets the required 4-digit specification.

* **Length Check:**
  * Checks if input is less than 4 digits (`PIN is too short`).
  * Checks if input is greater than 4 digits (`PIN is too long`).
  * Accepts valid 4-digit PINs (`PIN is exactly 4 digits`).
* **Access Control:** Grants access upon entering the correct default PIN (`0987`) and denies access for invalid PINs.

### Visual Evidence:

#### 1. Valid 4-Digit Correct PIN
![Correct PIN Access Granted](/door%20lock/taskone/doorcorrect.png)

#### 2. PIN Too Long (> 4 digits)
![PIN Too Long](/door%20lock/taskone/doorlong.png)

#### 3. PIN Too Short (< 4 digits)
![PIN Too Short](/door%20lock/taskone/doorthree.png)

#### 4. Incorrect PIN Entry
![Incorrect PIN Access Denied](/door%20lock/taskone/doorwrong.png)

---

## 📋 Task 2: System Menu Navigation

**Objective:** Provide an interactive menu interface following successful authentication, allowing users to perform various door management actions.

* **Menu Options:**
  1. Unlock Door
  2. Change Username *(In development)*
  3. Change PIN
  4. Exit

### Visual Evidence:

#### Feature Placeholder ("Change Username")
![Change Username Coming Soon](/door%20lock/tasktwo/comingsoon.png)

---

## 📋 Task 3: Attempt Counter & Timed System Lockout

**Objective:** Enhance system security by limiting incorrect authentication attempts and enforcing a timed penalty lockout.

* **Attempt Tracking:** Decrements remaining attempts for each failed PIN attempt (max 3 attempts).
* **System Lockout:** Triggers a 5-second countdown lock using `<unistd.h>` standard timer delays when all attempts are exhausted.

### Visual Evidence:

#### System Lockout Countdown Execution
![System Lockout Countdown](/door%20lock/taskthree/wrongone.png)

---

## 📋 Task 4: Complete System Integration

**Objective:** Integrate length validation, attempt counting, menu control flow, and authentication into a unified console system.

* **Integrated Workflow:** Combines 4-digit input checking, remaining attempt counters, system menu handling, and access granting.

### Visual Evidence:

#### Attempt Tracking & Successful System Menu Access
![Integrated System Execution](/door%20lock/taskfour/attempts.png)

---

## 🛠️ Project File Layout

```text
.
├── main.c
├── task1.c
├── task2.c
├── task3.c
├── task4.c
└── door lock/
    ├── taskone/
    │   ├── doorcorrect.png
    │   ├── doorlong.png
    │   ├── doorthree.png
    │   └── doorwrong.png
    ├── tasktwo/
    │   └── comingsoon.png
    ├── taskthree/
    │   └── wrongone.png
    └── taskfour/
        └── attempts.png
```
