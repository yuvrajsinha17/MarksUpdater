# MarksUpdater
Following in a python code to update the marks of the students and show its previous and current rank.
def nameRank(names, marks, updates, n):
    m=max(marks)
    # Array of students
    x = [[0 for j in range(n)] for i in range(n)]
    for i in range(n):
        # Store the name of the student
        x[i][0] = names[i]

        # Update the marks of the student
        x[i][1] = marks[i] + updates[i]

        # Store the current rank of the student
        x[i][2] = i + 1
    highest = [x[0][1], x[1][1], x[2][1]]
    l=names[highest.index(max(highest))]
    print("Name: ", l)
    print("previous rank: ",names.index(l)+1)
    print("current rank: ", highest.index(max(highest)))

# Names of the students
names = ["Yuvraj Sinha", "Anurag Sinha", "Aayush Sinha"]

# Marks of the students
marks = [75, 77, 85]

# Updates that are to be done
updates = [4, 6, -5]

# Number of students
n = len(marks)

nameRank(names, marks, updates, n)
