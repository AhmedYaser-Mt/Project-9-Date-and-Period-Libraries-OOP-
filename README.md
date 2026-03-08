# 📅 Date & Period Libraries (C++ OOP)

![C++](https://img.shields.io/badge/C%2B%2B-Programming-blue?logo=c%2B%2B)
![OOP](https://img.shields.io/badge/OOP-Design%20Principles-green)
![Algorithms](https://img.shields.io/badge/Algorithms-Date%20Processing-orange)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

A reusable **C++ Date and Period Utility Library** built using **Object-Oriented Programming (OOP)** principles.

This project converts previously implemented **date and time algorithms** into reusable libraries by organizing them into two main classes:

- `clsDate`
- `clsPeriod`

The goal is to design **clean, reusable, and extensible components** that simplify working with dates and periods in C++ applications.

---

# 📑 Table of Contents

- Project Overview
- Features
- Concepts Applied
- Project Structure
- Example Usage
- Example Output
- Future Improvements
- Learning Source

---

# 🚀 Project Overview

Working with **dates and time calculations** is a common requirement in many applications.

Instead of rewriting date-related functions repeatedly, this project organizes a large set of **date algorithms** into a reusable **C++ class library**.

The project demonstrates how **algorithmic solutions can evolve into structured OOP libraries** that improve:

- Code organization
- Reusability
- Maintainability
- Scalability

---

# ✨ Features

## 📅 Date Operations (`clsDate`)

The `clsDate` class provides many utilities for handling dates.

### Basic Date Utilities

- Get current system date
- Convert date from/to string
- Validate dates
- Determine leap years

### Date Calculations

- Add / subtract:
  - Days
  - Weeks
  - Months
  - Years
  - Decades
  - Centuries
  - Millennia

### Date Analysis

- Calculate difference between two dates
- Calculate age in days
- Get number of days in month/year
- Determine business days vs weekends

### Calendar Functions

- Print **monthly calendar**
- Print **yearly calendar**

### Date Comparisons

- Check if a date is before another
- Check if dates are equal
- Check if a date is after another

---

## ⏳ Period Operations (`clsPeriod`)

The `clsPeriod` class handles operations between two dates representing a **time period**.

Features include:

- Check if two periods **overlap**
- Calculate **period length**
- Check if a **date is within a period**
- Count **overlapping days** between two periods

---

# 🧠 Concepts Applied

This project demonstrates multiple important programming concepts:

- Object-Oriented Programming (OOP)
- Encapsulation
- Static Methods
- Function Overloading
- Code Reusability
- Algorithm Design
- Clean Code Practices

---

# 📂 Project Structure

```
Project-9-Date-Period-Libraries-OOP
│
├── clsDate.h
│   Date utility class containing all date algorithms
│
├── clsPeriod.h
│   Period utility class for handling date ranges
│
└── main.cpp
    Demonstration of library usage

```

---

# 💻 Example Usage

```cpp
#include <iostream>
#include "clsDate.h"
#include "clsPeriod.h"

using namespace std;

int main()
{
    clsDate Date1;
    Date1.Print(); // today's system date

    clsDate Date2("31/1/2022");
    Date2.Print();

    clsDate Date3(20, 12, 2022);
    Date3.Print();

    clsDate Date4(250, 2022); // 250th day of the year
    Date4.Print();

    Date1.IncreaseDateByOneMonth();
    Date1.Print();

    Date3.PrintYearCalendar();

    cout << "\nIs Date Valid: " << Date2.IsValid();

    cout << "\nMy Age in Days: "
         << clsDate::CalculateMyAgeInDays(clsDate(6, 11, 1977));

    clsPeriod Period1(clsDate(1,1,2022), clsDate(10,1,2022));
    clsPeriod Period2(clsDate(3,1,2022), clsDate(5,1,2022));

    cout << "\nOverlap: "
         << Period1.IsOverLapWith(Period2);

    return 0;
}
```

---

# 🖥️ Example Output

```
20/8/2025
31/1/2022
20/12/2022
7/9/2022
20/9/2025
[Year Calendar Printed]
Is Date Valid: 1
My Age in Days: 17482
Overlap: 1
```


---

# 🎓 Learning Source

This project was implemented as part of the **Programming Advices Training Track**.

Instructor  
👨‍🏫 **Dr. Mohammed Abu-Hadhoud**

Platform  
📚 **Programming Advices**

The project focuses on transforming algorithm-based exercises into **professional reusable OOP libraries**.

---
