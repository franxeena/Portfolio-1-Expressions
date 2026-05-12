# Portfolio 1: Expressions
## Title: Student Academic Status Checker

### Description
This program calculates the weighted average grade of a student using four subject grades:
- Reading Comprehension
- Mathematics
- Science
- Language Proficiency

The program also determines the student's academic status based on the computed average.

## Formula Used

```python
average = (0.15 * read) + (0.35 * math) + (0.25 * science) + (0.25 * langprof)
```
### Grading Scale
- All grades are 95 and above -> Running for Dean's List
- 90 and above -> Passed
- 85 to 89 -> Okay
- 75 to 84 -> Fair
- Below 75 -> Failed

```python
# ==========================================
# Student Grade Evaluation Program
# ==========================================

# Input grades from the user
# float is used for Reading Comprehension
# int is used for the remaining subjects

read = float(input("Enter Grade in Reading Comprehension: "))
math = int(input("Enter Grade in Mathematics: "))
science = int(input("Enter Grade in Science: "))
langprof = int(input("Enter Grade in Language Proficiency: "))

# ==========================================
# Compute the weighted average
# Formula:
# (Reading × 15%) + (Math × 35%)
# + (Science × 25%) + (Language × 25%)
# ==========================================

average = (0.15 * read) + (0.35 * math) + (0.25 * science) + (0.25 * langprof)

# Display the computed average
print("Average:", average)

# ==========================================
# Determine the student's evaluation
# ==========================================

# If average is 90 and above
if average >= 90:

    # Check if all subject grades are 95 and above
    if read >= 95 and math >= 95 and science >= 95 and langprof >= 95:
        print("Running for Dean's List")

    # Otherwise, the student passed
    else:
        print("Passed")

# If average is between 85 and 89
elif 85 <= average < 90:
    print("Okay")

# If average is between 75 and 84
elif 75 <= average < 85:
    print("Fair")

# If average is below 75
else:
    print("Failed")