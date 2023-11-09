# Tut 10
## Code
```
class Student:
    stuCount = 0
    def __init__(self, fname, lname, dob, gender, roll_number, marks):
        self.firstName = fname
        self.lastName = lname
        self.studentID = Student.stuCount
        Student.stuCount+=1
        self.DoB = dob
        self.gender = gender
        self.rollNumber = roll_number
        self.marks = marks

def sort_students_by_marks(slistudents):
    for i in range(len(slistudents)-1):
        for j in range(len(slistudents)-1):
            if slistudents[j][5] > slistudents[j+1][5]:
                slistudents[j], slistudents[j+1] = slistudents[j+1], slistudents[j]

    return slistudents
    

lis=[]
n=int(input('Enter no of students:'))
for i in range(n):
    fname, lname, dob, gender, roll_number, marks=input('enter firstname, laste name, dob(year-month-date), gender, rollno, marks: ').split(',')
    marks=int(marks)
    lis.append((fname, lname, dob, gender, roll_number, marks))
lis=sort_students_by_marks(lis)
print(lis)
studentlis=[]
for i in lis:
    studentlis.append(Student(*i))
    
for i in studentlis:
        print(f"{i.firstName} {i.lastName} - Marks: {i.marks}")

print(Student.stuCount)




class Rectangle:
    def __init__(self, width, height):
        self.width = width
        self.height = height

def print_rectangle(rectangle):
    print(f"Rectangle - Width: {rectangle.width}, Height: {rectangle.height}")


x= int(input('enter width of rectangle: '))
y= int(input('enter height of rectangle: '))


rectangle = Rectangle(x, y)
print_rectangle(rectangle)
```

## Test case

In first line `Enter no of students`=n

and in n lines after first `enter firstname, laste name, dob(year-month-date), gender, rollno, marks:`

after that `enter width of rectangle` and then `enter height of rectangle`
```
test case 1:-

2
a,s,d,f,g,10
q,w,e,r,t,30
10
4
```
