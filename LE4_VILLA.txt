#include <stdio.h>

int main() {
    char fullname[50];
    char section[50];
    float q1, q2, q3, q4;
    float generalaverage;
    char remarks[50];

    printf("Enter Complete Name: ");
    fgets(fullname, sizeof(fullname), stdin);

    printf("Enter section: ");
    fgets(section, sizeof(section), stdin);

    printf("\n");
    printf("Enter 1st Quarter Grade: ");
    scanf("%f", &q1);
    printf("Enter 2nd Quarter Grade: ");
    scanf("%f", &q2);
    printf("Enter 3rd Quarter Grade: ");
    scanf("%f", &q3);
    printf("Enter 4th Quarter Grade: ");
    scanf("%f", &q4);

    generalaverage = (q1 + q2 + q3 + q4) / 4;

    printf("\n");
    printf("Student: %s", fullname);
    printf("Section: %s", section);
    printf("General Average: %.2f\n", generalaverage);
    printf("Remarks: ");

    if (generalaverage >= 90 && generalaverage <= 100) {
        printf("Outstanding\n");
    } else if (generalaverage >= 85 && generalaverage <= 89) {
        printf("Very Satisfactory\n");
    } else if (generalaverage >= 80 && generalaverage <= 84) {
        printf("Satisfactory\n");
    } else if (generalaverage >= 75 && generalaverage <= 79) {
        printf("Fair\n");
    } else if (generalaverage < 75) {
        printf("Failed\n");
    }

    return 0;
}