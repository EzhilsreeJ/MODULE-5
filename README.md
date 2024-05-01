## EXPERIMENT-33-FACTORIAL CALCULATOR

### AIM:
To develop a program that calculates the factorial of a given number using pointers.

### ALGORITHM:
1. Begin the program.
2. Declare an integer variable `n` to store the input number.
3. Prompt the user to input a number.
4. Read the input value for `n` using `scanf()` function.
5. Declare an integer variable `fact` and a pointer variable `ptr` to store the factorial value and its address respectively.
6. Assign the address of `fact` to the pointer `ptr`.
7. Initialize `fact` to 1.
8. Use a for loop to calculate the factorial of the input number:
   - Iterate `i` from 1 to `n`.
   - Update the value pointed to by `ptr` by multiplying it with `i`.
9. Print the factorial of the entered number.
10. End the program.

## PROGRAM:
``` 
#include<stdio.h>
int main() {
    int n;
    scanf("%d",&n);
    int fact=1;
    int *ptr;
    ptr = &fact;
    for (int i=1;i<=n;i++){
        *ptr *= i;
    }
    printf("Factorial of entered number is : %d",*ptr);
} 

```
## SAMPLE OUTPUT :

![image](https://github.com/EzhilsreeJ/MODULE-5/assets/144870412/985718b4-584a-49ed-8df3-d268d32acf84)



## OUTPUT :

![image](https://github.com/EzhilsreeJ/MODULE-5/assets/144870412/8fba94cb-8f8b-4cb1-bfdc-e1ba6d3bb031)



## RESULT:
Thus the required program is written and executed successfully.



## EXPERIMENT-34-MODULO CALCULATOR

### AIM:
To create a program that calculates the modulo of two given integers using pointers.

### ALGORITHM:
1. Begin the program.
2. Declare two integer variables `a` and `b` to store the input integers.
3. Prompt the user to input two integers separated by a space.
4. Read the input values for `a` and `b` using `scanf()` function.
5. Calculate the modulo of `a` divided by `b` and store the result in integer variable `c`.
6. Declare an integer pointer variable `ptr` to store the address of `c`.
7. Assign the address of `c` to the pointer `ptr`.
8. Print the modulo value pointed to by `ptr`.
9. End the program.

## PROGRAM:
``` 
#include<stdio.h>
int main(){
    int a,b;
    scanf("%d %d",&a,&b);
    int c=a%b;
    int *ptr;
    ptr = &c;
    printf("Modulo = %d",*ptr);
}  

```
## SAMPLE OUTPUT :

![image](https://github.com/EzhilsreeJ/MODULE-5/assets/144870412/424fdf7c-fcab-435e-894f-ef4f5fa8a8b1)


## OUTPUT :
![image](https://github.com/EzhilsreeJ/MODULE-5/assets/144870412/e3a353d0-a94f-49c8-95f1-658c6cc93319)




## RESULT:
Thus the required program is written and executed successfully.


## EXPERIMENT-35-INTEGER POINTER SWAPPER

### AIM:
To develop a program that swaps the values of three integers using pointers.

### ALGORITHM:
1. Begin the program.
2. Declare three integer variables `m`, `n`, and `o` to store the input integers.
3. Prompt the user to input three integers separated by spaces.
4. Read the input values for `m`, `n`, and `o` using `scanf()` function.
5. Print the original values of `m`, `n`, and `o`.
6. Declare three integer pointer variables `a`, `b`, and `c` to store the addresses of `n`, `o`, and `m` respectively.
7. Assign the address of `n` to pointer `a`, the address of `o` to pointer `b`, and the address of `m` to pointer `c`.
8. Print the values pointed to by pointers `a`, `b`, and `c`, which effectively swaps the values of `m`, `n`, and `o`.
9. End the program.

## PROGRAM:
``` 
#include<stdio.h>
int main(){
    int m,n,o;
    scanf("%d %d %d",&m,&n,&o);
    printf("m is %d, n is %d, o is %d\n",m,n,o);
    int *a,*b,*c;
    a=&n;
    b=&o;
    c=&m;
    printf("m is %d, n is %d, o is %d\n",*a,*b,*c);
    
}

```


## OUTPUT :

![image](https://github.com/EzhilsreeJ/MODULE-5/assets/144870412/dfa9b991-1121-4db1-a21c-52ded2622b3b)



## RESULT:
Thus the required program is written and executed successfully.


## EXPERIMENT-36-RECURSIVE SUM OF DIGITS

### AIM:
To develop a program that calculates the sum of digits of a given number using recursion.

### ALGORITHM:
1. Begin the program.
2. Define a recursive function `sum_of_digits` that takes an integer `n` as input.
3. Inside the function:
   - If `n` is 0, return 0.
   - Otherwise, return the sum of the last digit of `n` and the result of calling `sum_of_digits` recursively with `n` divided by 10.
4. In the main function:
   - Declare an integer variable `num` and assign a test value (e.g., 12224).
   - Call the `sum_of_digits` function with `num` as argument and store the result in an integer variable `result`.
   - Print the sum of digits of `num`.
5. End the program.

## PROGRAM:
``` 
#include <stdio.h>

// Function to find sum of digits using recursion
int sum_of_digits(int n) {
    if (n == 0)
        return 0;
    else
        return (n % 10 + sum_of_digits(n / 10));
}

// Main function to test the above function
int main() {
    int num = 12224;
    int result = sum_of_digits(num);
    printf("Sum of digits of %d = %d\n", num, result);
    return 0;
}

```
## SAMPLE OUTPUT :

![image](https://github.com/EzhilsreeJ/MODULE-5/assets/144870412/e0195e30-b704-40c2-ad9a-3e3f3b61c73b)




## OUTPUT :
![image](https://github.com/EzhilsreeJ/MODULE-5/assets/144870412/12713e8d-1869-4788-90af-910b2d1c97f8)





## RESULT:
Thus the required program is written and executed successfully.


## EXPERIMENT-37-MATRIX TRIANGLE SUM

### AIM:
To create a program that calculates the sum of elements in the upper and lower triangles of a given matrix.

### ALGORITHM:
1. Begin the program.
2. Declare integer variables `rows`, `columns`, `i`, `j` to store the dimensions and loop indices.
3. Declare a 2D integer array `matrix` to store the matrix elements, assuming a maximum size of 3x3 for simplicity.
4. Prompt the user to input the number of rows and columns of the matrix.
5. Read the input values for `rows` and `columns` using `scanf()` function.
6. Use nested for loops to read the matrix elements from the user.
7. Display the entire matrix by iterating through each element and printing them row by row.
8. Print a newline for spacing.
9. Initialize variables `sumLower` and `sumUpper` to store the sum of elements in the lower and upper triangles respectively.
10. Iterate through each row and column of the matrix:
    - For the upper triangle:
        - If the column index is less than or equal to the row index, print the element and add it to `sumUpper`.
        - Otherwise, print a space.
    - Print a newline after each row.
11. Print the sum of elements in the lower triangle.
12. Repeat steps 10 and 11 for the lower triangle, adding the elements to `sumLower` if the column index is greater than or equal to the row index.
13. Print the sum of elements in the upper triangle.
14. End the program.

## PROGRAM:
``` 
#include <stdio.h>

int main() {
    int rows, columns, i, j;
    int matrix[3][3]; // Assuming a maximum size of 3x3 for simplicity
    int sumLower = 0, sumUpper = 0;
    scanf("%d %d", &rows, &columns);
    for (i = 0; i < rows; i++) {
        for (j = 0; j < columns; j++) {
            scanf("%d", &matrix[i][j]);
        }
    }

    // Display the entire matrix
    printf("matrix is\n");
    for (i = 0; i < rows; i++) {
        for (j = 0; j < columns; j++) {
            printf("%d ", matrix[i][j]);
        }
        printf("\n");
    }
    printf("\n");
    
    for (i = 0; i < rows; i++) {
        for (j = 0; j < columns; j++) {
            if (j <= i) { // Only print elements in the upper triangle
                printf("%d ", matrix[i][j]);
                sumUpper += matrix[i][j]; // Add to the sum
            } else {
                printf(" "); // Print spaces for the lower triangle part
            }
        }
        printf("\n");
    }
    
    printf("Sum of Lower Triangle is %d\n\n\n", sumUpper);
    for (i = 0; i < rows; i++) {
        for (j = 0; j < columns; j++) {
            if (j >= i) { // Only print elements in the lower triangle
                printf("%d ", matrix[i][j]);
                sumLower += matrix[i][j]; // Add to the sum
            } 
        }
        printf("\n");
    }
    printf("Sum of Upper Triangle is %d\n", sumLower);
    return 0;
}

```
## SAMPLE OUTPUT :

![image](https://github.com/EzhilsreeJ/MODULE-5/assets/144870412/78f897c1-3b65-4559-bf06-00c55d71497e)



## OUTPUT :
![image](https://github.com/EzhilsreeJ/MODULE-5/assets/144870412/1f89758c-b1bd-4d66-a2d6-e6b4b059c53f)


## RESULT:
Thus the required program is written and executed successfully.



## EXPERIMENT-38-ROW AND COLUMN SUM OF MATRIX

### AIM:
To develop a program that calculates the sum of elements in each row and each column of a given matrix dynamically allocated using memory allocation.

### ALGORITHM:
1. Begin the program.
2. Declare integer variables `rows`, `columns`, `i`, `j` to store the dimensions and loop indices.
3. Prompt the user to input the number of rows and columns of the matrix.
4. Read the input values for `rows` and `columns` using `scanf()` function.
5. Dynamically allocate memory for the matrix using 2D array of pointers.
6. Use nested for loops to read the matrix elements from the user.
7. Iterate through each row of the matrix and calculate the sum of elements in each row:
   - Initialize a variable `sum` to store the sum of elements in the current row.
   - Iterate through each column of the current row and add the element to `sum`.
   - Print the sum of elements in the current row.
8. Iterate through each column of the matrix and calculate the sum of elements in each column:
   - Initialize a variable `sum` to store the sum of elements in the current column.
   - Iterate through each row of the current column and add the element to `sum`.
   - Print the sum of elements in the current column.
9. Free the allocated memory for the matrix to prevent memory leaks.
10. End the program.

## PROGRAM:
``` 
#include <stdio.h>
#include <stdlib.h>

int main() {
    int rows, columns, i, j;
    scanf("%d %d", &rows, &columns);

    // Allocate memory for the matrix
    int** matrix = (int**)malloc(rows * sizeof(int*));
    for (i = 0; i < rows; i++) {
        matrix[i] = (int*)malloc(columns * sizeof(int));
    }

    // Read the matrix elements
    for (i = 0; i < rows; i++) {
        for (j = 0; j < columns; j++) {
            scanf("%d", &matrix[i][j]);
        }
    }

    // Calculate and print the sum of each row
    
    for (i = 0; i < rows; i++) {
        int sum = 0;
        for (j = 0; j < columns; j++) {
            sum += matrix[i][j];
        }
        printf("The Sum of Elements of a Rows in a Matrix =  ");
        printf("%d\n", sum);
    }
    for (j = 0;j < rows;j++) {
        int sum = 0;
        for (i = 0; i < columns; i++) {
            sum += matrix[i][j];
        }
        printf("The Sum of Elements of a Columns in a Matrix =  ");
        printf("%d\n", sum);
    }


    // Free allocated memory
    for (i = 0; i < rows; i++) {
        free(matrix[i]);
    }
    free(matrix);

    return 0;
}

```
## SAMPLE OUTPUT :

![image](https://github.com/EzhilsreeJ/MODULE-5/assets/144870412/42ff21a7-0275-4098-ab77-5dc015dd831d)



## OUTPUT :
![image](https://github.com/EzhilsreeJ/MODULE-5/assets/144870412/e894ae14-2691-44d7-ac6d-8082ce8eda00)



## RESULT:
Thus the required program is written and executed successfully.


## EXPERIMENT-39-STRING ANALYSIS

### AIM:
To develop a program that analyzes a given string and counts the number of alphabets, digits, and special characters in it.

### ALGORITHM:
1. Begin the program.
2. Declare a character array `str` to store the input string and integer variables `alphabets`, `digits`, and `specialChars` to store the counts.
3. Read the input string including spaces using `fgets()` function.
4. Remove the newline character added by `fgets()` function, if present.
5. Iterate through each character of the string:
   - If the character is an alphabet (using `isalpha()` function), increment the `alphabets` count.
   - If the character is a digit (using `isdigit()` function), increment the `digits` count.
   - If the character is a special character or whitespace (using `ispunct()` and `isspace()` functions), increment the `specialChars` count.
6. Print the counts of alphabets, digits, and special characters.
7. End the program.

## PROGRAM:
``` 
#include <stdio.h>
#include <ctype.h> // For isalpha(), isdigit(), and ispunct() functions
#include<string.h>
int main() {
    char str[100];
    int alphabets = 0, digits = 0, specialChars = 0;

    fgets(str, sizeof(str), stdin); // Read the string including spaces

    // Remove the newline character added by fgets
    str[strcspn(str, "\n")] = 0;

    for (int i = 0; str[i] != '\0'; i++) {
        if (isalpha(str[i])) {
            alphabets++;
        } else if (isdigit(str[i])) {
            digits++;
        } else if (ispunct(str[i]) || isspace(str[i])) {
            specialChars++;
        }
    }

    printf("Number of Alphabets in the string is : %d\n", alphabets);
    printf("Number of Digits in the string is : %d\n", digits);
    printf("Number of Special characters in the string is : %d\n", specialChars);

    return 0;
}

```


## OUTPUT :
![image](https://github.com/EzhilsreeJ/MODULE-5/assets/144870412/8cea8677-a338-4cf3-af61-fbfc28ff846e)



## RESULT:
Thus the required program is written and executed successfully.


## EXPERIMENT-40-LARGEST AND SMALLEST WORD

### AIM:
To develop a program that finds the largest and smallest words in a given string.

### ALGORITHM:
1. Begin the program.
2. Declare character arrays `input`, `largestWord`, and `smallestWord` to store the input string, largest word, and smallest word respectively. Also, declare integer variables `largestLength` and `smallestLength` to store the lengths of the largest and smallest words.
3. Read the input string including spaces using `fgets()` function.
4. Remove the newline character added by `fgets()` function, if present.
5. Initialize `largestLength` to 0 and `smallestLength` to a large value (e.g., 1000).
6. Use `strtok()` function to tokenize the input string into words using space (' ') as the delimiter.
7. Iterate through each word obtained from the string:
   - Calculate the length of the current word using `strlen()` function.
   - If the length of the current word is greater than `largestLength`, update `largestLength` and copy the word to `largestWord`.
   - If the length of the current word is less than `smallestLength`, update `smallestLength` and copy the word to `smallestWord`.
8. Print the largest and smallest words found in the input string.
9. End the program.
## PROGRAM:
``` 
#include <stdio.h>
#include <ctype.h> // For isalpha(), isdigit(), and ispunct() functions
#include<string.h>
int main() {
    char str[100];
    int alphabets = 0, digits = 0, specialChars = 0;

    fgets(str, sizeof(str), stdin); // Read the string including spaces

    // Remove the newline character added by fgets
    str[strcspn(str, "\n")] = 0;

    for (int i = 0; str[i] != '\0'; i++) {
        if (isalpha(str[i])) {
            alphabets++;
        } else if (isdigit(str[i])) {
            digits++;
        } else if (ispunct(str[i]) || isspace(str[i])) {
            specialChars++;
        }
    }

    printf("Number of Alphabets in the string is : %d\n", alphabets);
    printf("Number of Digits in the string is : %d\n", digits);
    printf("Number of Special characters in the string is : %d\n", specialChars);

    return 0;
}

```



## OUTPUT :
![image](https://github.com/EzhilsreeJ/MODULE-5/assets/144870412/c6a141fd-4e08-4cd0-bf86-2a2cc0083ace)




## RESULT:
Thus the required program is written and executed successfully.



















