# Portfolio 1: Expressions
## Title: General Weighted Average (GWA) Calculator

### Description
This program calculates the weighted average grade of a student using four subject grades:
- Reading Comprehension
- Mathematics
- Science
- Language Proficiency

The program also determines the student's academic status based on the computed average.

### Formula Used

Average = (0.15 × Reading) + (0.35 × Math) + (0.25 × Science) + (0.25 × Language Proficiency)

### Grading Scale
- All grades are 95 and above -> Running for Dean's List
- 90 and above -> Passed  
- 85 to 89 -> Okay
- 75 to 84 -> Fair
- Below 75 -> Failed


read = float(input("Enter Grade in Reading Comprehension: "))
math = int(input("Enter Grade in Mathematics: "))
science = int(input("Enter Grade in Science: "))
langprof = int(input("Enter Grade in Language Proficiency: "))

average = (0.15 * read) + (0.35 * math) + (0.25 * science) + (0.25 * langprof)

print("Average:", average)

if average >= 90:
    
    if read >= 95 and math >= 95 and science >= 95 and langprof >= 95:
        print("Running for Dean's List")
    
    else:
        print("Passed")

elif 85 <= average < 90:
    print("Okay")

elif 75 <= average < 85:
    print("Fair")

else:
    print("Failed")