Removing all characters from string except alphabets
In this article we will learn about Removing all characters from string except alphabets.

In the process to do this all the special characters (!,@,#,etc.) and numeric characters (1,2,3,etc.) need to removed from the string. 

Input:- 12Pre5pinst45a
Output:- prepinsta
Removing all characters from the string except alphabets
Algorithm:
Initialize the variables.
Accept the input.
Initialize a for loop.
Iterate each character through the loop.
Remove non alphabetical characters
Terminate for loop.
Print result.
 
While loop in C
C programming code to remove all characters from string except alphabets
Run
#include <stdio.h>
int main()
{
    //Initializing variable.
    char str[100];
    int i, j;
    
     //Accepting input.
    printf(" Enter a string : ");
    gets(str);

     //Iterating each character and removing non alphabetical characters.
    for(i = 0; str[i] != '\0'; ++i)
    {
        while (!( (str[i] >= 'a' && str[i] <= 'z') || (str[i] >= 'A' && str[i] <= 'Z') || str[i] == '\0') )
        {
            for(j = i; str[j] != '\0'; ++j)
            {
                str[j] = str[j+1];
            }
            str[j] = '\0'; 
        }
    }
     //Printing output.
    printf(" After removing non alphabetical characters the string is :");
    puts(str);
    return 0;
}
Output:
Enter a string : *1prep_insta*
After removing non alphabetical characters the string is :prepinsta
