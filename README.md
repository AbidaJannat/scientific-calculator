#include <stdio.h>
#include <math.h>
#include <stdlib.h>

#define MAX 10


void addition()
 {
    int a, b, result;
    printf("Enter two numbers: ");
    scanf("%d %d", &a, &b);
    result = a + b;
    printf("Result: %d\n", result);
}


void subtraction()
{
    int a, b, result;
    printf("Enter two numbers: ");
    scanf("%d %d", &a, &b);
    result = a - b;
    printf("Result: %d\n", result);
}


void multiplication()
{
    int a, b, result;
    printf("Enter two numbers: ");
    scanf("%d %d", &a, &b);
    result = a * b;
    printf("Result: %d\n", result);
}


void division()
{
    double a, b, result;
    printf("Enter two numbers: ");
    scanf("%lf %lf", &a, &b);
    if (b != 0)
        {
        result = a / b;
        printf("Result: %.2f\n", result);
    } else {
        printf("Error: Division by zero is not allowed.\n");
    }
}


void sin_function()
 {
    double angle_degrees, angle_radians, result;
    printf("Enter angle in degrees: ");
    scanf("%lf", &angle_degrees);
    angle_radians = angle_degrees * (M_PI / 180);
    result = sin(angle_radians);
    printf("Result: %.2f\n", result);
}


void cos_function()
 {
    double angle_degrees, angle_radians, result;
    printf("Enter angle in degrees: ");
    scanf("%lf", &angle_degrees);
    angle_radians = angle_degrees * (M_PI / 180);
    result = cos(angle_radians);
    printf("Result: %.2f\n", result);
}


void tan_function()
{
    double angle_degrees, angle_radians, result;
    printf("Enter angle in degrees: ");
    scanf("%lf", &angle_degrees);
    angle_radians = angle_degrees * (M_PI / 180);
    result = tan(angle_radians);
    printf("Result: %.2f\n", result);
}


void logBasee()
{
    double a, result;
    printf("Enter number: ");
    scanf("%lf", &a);
    if (a <= 0.0)
        {
        printf("Math Error\n");
        }
     else
     {
         result = log(a);
        printf("Result = %lf",result);
    }
}
void logBasee10()
{
    double a, result;
    printf("Enter number: ");
    scanf("%lf",&a);
    if(a<= 0.0)
    {
        printf("Math Error\n");
    }
    else
    {
        result = log10(a);
        printf("Result = %lf",result);
    }
}


void squareRoot()
 {
    double a, result;
    printf("Enter number: ");
    scanf("%lf", &a);
    if (a >= 0)
        {
        result = sqrt(a);
        printf("Result: %.2f\n", result);
    } else
    {
        printf("Error: Square root of negative number is not allowed.\n");
    }
}


void power()
 {
    double base, exponent, result;
    printf("Enter base and exponent: ");
    scanf("%lf %lf", &base, &exponent);
    result = pow(base, exponent);
    printf("Result = %.lf\n", result);
}

void cubeRoot()
{
    int n;
    double result;
    printf("Enter a number: ");
    scanf("%d",&n);
    result = cbrt(n);
    printf("Result = %f",result);
}

void factorial()
{
    int n, i;
    unsigned long long fact = 1;
    printf("Enter an integer: ");
    scanf("%d", &n);
    if (n < 0)
        printf("Factorial of a negative number doesn't exist.\n");
    else {
        for (i = 1; i <= n; i++)
            {
            fact *= i;
        }
        printf("Factorial of %d = %llu\n", n, fact);
    }
}
void matrix_addition()
 {
    int rows, cols;
    printf("Enter number of rows and columns: ");
    scanf("%d %d", &rows, &cols);

    if (rows > MAX || cols > MAX)
        {
        printf("Matrix size exceeds maximum allowed (%d).\n", MAX);
        return;
    }

    double matrix1[rows][cols], matrix2[rows][cols], result[rows][cols];

    printf("Enter elements of the first matrix:\n");
    for (int i = 0; i < rows; i++)
        for (int j = 0; j < cols; j++)
            scanf("%d", &matrix1[i][j]);

    printf("Enter elements of the second matrix:\n");
    for (int i = 0; i < rows; i++)
        for (int j = 0; j < cols; j++)
            scanf("%d", &matrix2[i][j]);


    for (int i = 0; i < rows; i++)
        for (int j = 0; j < cols; j++)
            result[i][j] = matrix1[i][j] + matrix2[i][j];


    printf("Result of matrix addition:\n");
    for (int i = 0; i < rows; i++)
        {
        for (int j = 0; j < cols; j++)
            printf("%d ", result[i][j]);
        printf("\n");
    }
}


void matrix_subtraction()
{
    int rows, cols;
    printf("Enter number of rows and columns: ");
    scanf("%d %d", &rows, &cols);

    if (rows > MAX || cols > MAX) {
        printf("Matrix size exceeds maximum allowed (%d).\n", MAX);
        return;
    }

    double matrix1[rows][cols], matrix2[rows][cols], result[rows][cols];

    printf("Enter elements of the first matrix:\n");
    for (int i = 0; i < rows; i++)
        for (int j = 0; j < cols; j++)
            scanf("%d", &matrix1[i][j]);

    printf("Enter elements of the second matrix:\n");
    for (int i = 0; i < rows; i++)
        for (int j = 0; j < cols; j++)
            scanf("%d", &matrix2[i][j]);

    for (int i = 0; i < rows; i++)
        for (int j = 0; j < cols; j++)
            result[i][j] = matrix1[i][j] - matrix2[i][j];

    printf("Result of matrix subtraction:\n");
    for (int i = 0; i < rows; i++) {
        for (int j = 0; j < cols; j++)
            printf("%d ", result[i][j]);
        printf("\n");
    }
}

void solve_linear_equation()
 {
    double a1, b1, c1;
    double a2, b2, c2;

    printf("For system of equations:\n");
    printf("a1 * x + b1 * y = c1\n");
    printf("a2 * x + b2 * y = c2\n");

    printf("Enter coefficient a1: ");
    scanf("%lf", &a1);
    printf("Enter coefficient b1: ");
    scanf("%lf", &b1);
    printf("Enter constant c1: ");
    scanf("%lf", &c1);

    printf("Enter coefficient a2: ");
    scanf("%lf", &a2);
    printf("Enter coefficient b2: ");
    scanf("%lf", &b2);
    printf("Enter constant c2: ");
    scanf("%lf", &c2);

    double determinant = a1 * b2 - a2 * b1;

    if (determinant == 0)
        {
        if (a1 * c2 == a2 * c1 && b1 * c2 == b2 * c1)
            printf("Infinite solutions (the system is consistent but dependent).\n");
        else
            printf("No solution (the system is inconsistent).\n");
    } else {
        double x = (c1 * b2 - c2 * b1) / determinant;
        double y = (a1 * c2 - a2 * c1) / determinant;
        printf("Solution: x = %.2f, y = %.2f\n", x, y);
    }
}


int main()
{
    int choice;
    while (1)
        {
        printf("             SCIENTIFIC CALCULATOR             \n");
        printf(" 1. Addition\n");
        printf(" 2. Subtraction\n");
        printf(" 3. Multiplication\n");
        printf(" 4. Division\n");
        printf(" 5. Sine (sin)\n");
        printf(" 6. Cosine (cos)\n");
        printf(" 7. Tangent (tan)\n");
        printf(" 8. LogBasee\n");
        printf(" 9. LogBasee10\n");
        printf(" 10. Square root (sqrt)\n");
        printf(" 11. Power (x^y)\n");
        printf(" 12. cubeRoot\n");
        printf(" 13. factorial\n");
        printf(" 14. Matrix Addition\n");
        printf(" 15. Matrix Subtraction\n");
        printf(" 16. Solve Linear Equation \n");
        printf(" 17. Exit\n");
        printf("Enter your choice: ");
        scanf("%d", &choice);

        switch (choice)
        {
            case 1: addition();
            break;
            case 2: subtraction();
            break;
            case 3: multiplication();
             break;
            case 4: division();
            break;
            case 5: sin_function();
             break;
            case 6: cos_function();
            break;
            case 7: tan_function();
             break;
            case 8: logBasee();
            break;
            case 9: logBasee10();
            break;
            case 10: squareRoot();
             break;
            case 11: power();
             break;
             case 12: cubeRoot();
             break;
             case 13: factorial();
             break;
            case 14: matrix_addition();
             break;
            case 15: matrix_subtraction();
              break;
            case 16: solve_linear_equation();
             break;
            case 17: printf("Exiting...\n");
            break;
            return 0;
            default: printf("Invalid choice. Please try again.\n");
        }
    }
    return 0;
}
