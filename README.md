# Grading-system-of-students-
This project implements an Automatic Grade Calculator in C that evaluates students’ academic performance based on marks obtained in five subjects. It determines grades automatically and checks for subject-wise pass criteria.

#include <stdio.h>
int main() {
    int n; 
    printf("Enter number of students: ");
    scanf("%d", &n);
   for (int i = 1; i <= n; i++) {
        int marks[5];
        float percentage;
        int pass = 1;

        printf("\n++++ Enter marks for Student %d ++++\n", i);
        printf("Physics: ");
        scanf("%d", &marks[0]);
        printf("Mathematics: ");
        scanf("%d", &marks[1]);
        printf("Computer Science: ");
        scanf("%d", &marks[2]);
        printf("English: ");
        scanf("%d", &marks[3]);
        printf("Chemistry: ");
        scanf("%d", &marks[4]);
   for (int j = 0; j < 5; j++) {
            if (marks[j] < 50) {
                pass = 0; 
            }
        }
        percentage = (marks[0] + marks[1] + marks[2] + marks[3] + marks[4]) / 5.0;
        printf("\nResult for Student %d:\n", i);
        if (pass == 1) {
            if (percentage >= 90)
                printf("Grade: A\n");
            else if (percentage >= 80)
                printf("Grade: B\n");
            else if (percentage >= 70)
                printf("Grade: C\n");
            else if (percentage >= 60)
                printf("Grade: D\n");
            else
                printf("Grade: E (Needs improvement)\n");
        } else {
            printf("Not eligible (Failed in one or more subjects)\n");
        }
    }

    return 0;
}
