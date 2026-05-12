# Portfolio 1: Expressions
## Title: Student Academic Status Checker

### Description
This program calculates the weighted average grade of a student using four subject grades:
- Reading Comprehension
- Mathematics
- Science
- Language Proficiency

The program also determines the student's academic status based on the computed average.

# Student Academic Status Checker

# Formula Used:
# Average = (0.15 × Reading) + (0.35 × Math)
#         + (0.25 × Science) + (0.25 × Language Proficiency)

print("=== Grading Scale ===")
print("95 and above in ALL subjects -> Running for Dean's List")
print("90 and above -> Passed")
print("85 to 89 -> Okay")
print("75 to 84 -> Fair")
print("Below 75 -> Failed")
print()

# Input grades
read = float(input("Enter Grade in Reading Comprehension: "))
math = float(input("Enter Grade in Mathematics: "))
science = float(input("Enter Grade in Science: "))
langprof = float(input("Enter Grade in Language Proficiency: "))

# Compute weighted average
average = (
    (0.15 * read) +
    (0.35 * math) +
    (0.25 * science) +
    (0.25 * langprof)
)

# Display average
print("\nAverage:", round(average, 2))

# Determine academic status
if average >= 90:

    if read >= 95 and math >= 95 and science >= 95 and langprof >= 95:
        print("Status: Running for Dean's List")

    else:
        print("Status: Passed")

elif 85 <= average < 90:
    print("Status: Okay")

elif 75 <= average < 85:
    print("Status: Fair")

else:
    print("Status: Failed")