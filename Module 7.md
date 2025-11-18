EXP NO:1 C PROGRAM FOR ARRAY OF STRUCTURE TO CHECK ELIGIBILITY FOR THE VACCINE.

Aim:
To write a C program for array of structure to check eligibility for the vaccine person age above 6 years of age.

Algorithm:
1.	Declare structure eligible with age (integer) and n (character array)
2.	Declare variable e of type eligible
3.	Input age and name using scanf, store in e
4.	If e.age <= 6
-	Print "Vaccine Eligibility: No"
Else
-	Print "Vaccine Eligibility: Yes"
5.	Print details (e.age, e.n)
6.	Return 0
 
Program:
```
#include <stdio.h>

struct person {
    int age;
    char name[100];
};

int main() {
    struct person arr[1];

    if (scanf("%d", &arr[0].age) != 1) return 0;
    if (scanf("%s", arr[0].name) != 1) return 0;

    printf("Age:%d\n", arr[0].age);
    printf("Name:%s", arr[0].name);
    printf("vaccine:%d\n", arr[0].age);
    if (arr[0].age > 18)
        printf("eligibility:yes\n");
    else
        printf("eligibility:no\n");

    return 0;
}
```



Output:

<img width="850" height="315" alt="image" src="https://github.com/user-attachments/assets/3a61d41d-f1ae-4e27-85bf-29902f910d9b" />



Result:

Thus, the program is verified successfully. 



EXP NO:2 C PROGRAM FOR PASSING STRUCTURES AS FUNCTION ARGUMENTS AND RETURNING A STRUCTURE FROM A FUNCTION
Aim:
To write a C program for passing structure as function and returning a structure from a function

Algorithm:
1.	Define structure numbers with members a and b.
2.	Declare variable n of type numbers.
3.	Prompt the user to enter values for a and b.
4.	Input values for a and b into n using scanf.
5.	Call the add function with n as an argument.
6.	Print the result returned by the add function.
7.	Return 0
 
Program:
```
#include <stdio.h>
struct addition
{
    int a,b;
    int result;
    
};
int add(struct addition a1)
{
    a1.result=a1.a+a1.b;
    return a1.result;
}
int main()
{   
    struct addition a1;
    scanf("%d",&a1.a);
    scanf("%d",&a1.b);
    printf("%d",add(a1));
}
```




Output:

<img width="852" height="401" alt="image" src="https://github.com/user-attachments/assets/00297846-59b7-43cb-94c4-5820855a6421" />





Result:

Thus, the program is verified successfully


 
EXP.NO:3 C PROGRAM TO READ A FILE NAME FROM USER AND WRITE THAT FILE USING FOPEN()

Aim:
To write a C program to read a file name from user

Algorithm:
1.	Include the necessary header file stdio.h.
2.	Begin the main function.
3.	Declare a file pointer p.
Declare a character array name to store the file name.
4.	Prompt the user to enter a file name.
Use scanf to input the file name into the name array.
5.	Print a message indicating that the file with the specified name has been created successfully.
6.	Use fopen to open a file with the name provided by the user in write mode ("w").
-	If successful, continue to the next step.
-	If unsuccessful, print an error message and exit the program with a non-zero status.
1.	Print a message indicating that the file has been opened successfully.
2.	Use fclose to close the file.
3.	Print a message indicating that the file has been closed.
4.	End the main function.
5.	Return 0 to indicate successful program execution.
 
Program:
```
#include <stdio.h>

int main() {
    char filename[50];
    FILE *fp;
    scanf("%s", filename);
    fp = fopen(filename, "w");

    if (fp == NULL) {
        printf("Error in creating file");
        return 1;
    }
    printf("%s File Created Successfully\n", filename);
    printf("%s File Opened\n", filename);
    fclose(fp);
    printf("%s File Closed", filename);
    return 0;
}
```




Output:


<img width="836" height="478" alt="image" src="https://github.com/user-attachments/assets/163b8954-0514-4439-86a0-fe7f8cfbd720" />












Result:

Thus, the program is verified successfully
 


EXP NO:4   PROGRAM TO READ A FILE NAME FROM USER, WRITE THAT FILE AND INSERT TEXT IN TO THAT FILE
Aim:
To write a C program to read, a file and insert text in that file
Algorithm:
1.	Include the necessary header file stdio.h.
2.	Begin the main function.
3.	Declare a file pointer p.
Declare character arrays name and text. Declare an integer variable num.
4.	Prompt the user to enter a file name and the number of strings.
Use scanf to input the file name into the name array and the number of strings into the num variable.
5.	Use fopen to open a file with the name provided by the user in write mode ("w").
-	If successful, continue to the next step.
-	If unsuccessful, print an error message and exit the program with a non-zero status.
6.	Print a message indicating that the file has been opened successfully.
1.	Use a loop to input strings from the user and write them to the file using fputs.
2.	Use fclose to close the file.
3.	Print a message indicating that data has been added successfully.
4.	End the main function.
5.	Return 0 to indicate successful program execution.
 
Program:
```
#include <stdio.h>

int main() {
    char filename[50];
    FILE *fp;
    int n;
    char text[100];
    scanf("%s", filename);
    fp = fopen(filename, "w");

    if (fp == NULL) {
        printf("Error in creating file");
        return 1;
    }
    scanf("%d", &n);
    for (int i = 0; i < n; i++) {
        scanf("%s", text);
        fprintf(fp, "%s\n", text);
    }

    printf("%s Opened\n", filename);
    printf("Data added Successfully");
    fclose(fp);
    return 0;
}
```





Output:


<img width="832" height="442" alt="image" src="https://github.com/user-attachments/assets/be0f378d-32db-404c-9eb8-dbb0a6a2cfdd" />







Result:
Thus, the program is verified successfully



Ex No 5 :  C program to find the biggest among three numbers using structure?
Aim:
The aim of this program is to  C program to find the biggest among three numbers using structure?
Algorithm:
1.Input the number of subjects.

2.Declare a structure Numbers with fields a, b, c. Create a variable n of that type.

3.Declare an integer variable biggest to hold the result.

4.Read three integers from input and store them in n.a, n.b, n.c.

5.Compare n.a with n.b and n.c:

6.If n.a is greater than or equal to both n.b and n.c, set biggest = n.a.

7.Otherwise, compare n.b with n.a and n.c:

8.If n.b is greater than or equal to both n.a and n.c, set biggest = n.b.

9.Otherwise (neither a nor b was the largest), set biggest = n.c.

10Print the value of biggest.

11.End the program by returning 0.

Program:
```
#include <stdio.h>


struct Numbers {
    int a, b, c;
};

int main() {
    struct Numbers n;
    int biggest;

    
    scanf("%d %d %d", &n.a, &n.b, &n.c);

  
    if (n.a >= n.b && n.a >= n.c)
        biggest = n.a;
    else if (n.b >= n.a && n.b >= n.c)
        biggest = n.b;
    else
        biggest = n.c;


    printf("%d", biggest);

    return 0;
}
```




Output:


<img width="827" height="311" alt="image" src="https://github.com/user-attachments/assets/493701e3-886b-41b7-9e0f-0c779d02e0bf" />







Result:
Thus, the program is verified successfully
