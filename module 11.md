# NAME : SOMESHWAR S
# REGNO : 212224040322

# EXP NO:21 C PROGRAM TO CREATE A FUNCTION TO FIND THE GREATEST NUMBER

Aim:
To write a C program to create a function to find the greatest number

Algorithm:
1.	Include the necessary header #include <stdio.h>.
2.	Use a series of if and else if statements to compare the values and return the maximum among them.
3.	Declare variables n1, n2, n3, n4, and greater to store user input and the result.
4.	Use scanf to take four integers as input.
5.	Call the max_of_four function with the input integers and store the result in the greater variable
 
Program:
```
#include<stdio.h>
int max_of_four(int a,int b,int c,int d){
    int max=a;
    if(b>max){
        max=b;
    }
    if(c>max){
        max=c;
    }
    if(d>max){
        max=d;
    }
    return max;
}
int main(){
    int a,b,c,d;
    scanf("%d%d%d%d",&a,&b,&c,&d);
    printf("%d",max_of_four(a,b,c,d));
    return 0;
}
```

Output:


![image](https://github.com/user-attachments/assets/a5485f04-be0f-4e04-9542-60937db8c0b2)


Result:
Thus, the program  that create a function to find the greatest number is verified successfully.


 
EXP NO:22 C PROGRAM TO PRINT THE MAXIMUM VALUES FOR THE AND, OR AND  XOR COMPARISONS

Aim:
To write a C program to print the maximum values for the AND, OR and XOR comparisons

Algorithm:
1.	Define a function calculate_the_max that takes two integers n and k as parameters.
2.	Declare variables a, o, and x to store the maximum values for AND, OR, and XOR operations, respectively.
3.	Use nested loops to iterate through pairs of integers (i, j) from 1 to n.
4.	Within the loops, check conditions for AND, OR, and XOR operations and update the corresponding maximum values (a, o, x).
5.	Declare variables n and k to store user input.
6.	Use scanf to take two integers as input.
7.	Call the calculate_the_max function with input values.
 
Program:

```
#include<stdio.h>
int main(){
    int n,k,a=0,o=0,x=0;
    scanf("%d %d",&n,&k);
    for(int i=1;i<n;i++){
        for(int j=i+1;j<=n;j++){
            if((i&j)<k&&(i&j)>a)a=i&j;
            if((i|j)<k&&(i|j)>o)o=i|j;
            if((i^j)<k&&(i^j)>x)x=i^j;
        }
    }
        printf("%d\n%d\n%d",a,o,x);
}
```

Output:


![image](https://github.com/user-attachments/assets/1b7aba2f-60c4-4d0b-8395-3f35c87a78e8)


Result:
Thus, the program to print the maximum values for the AND, OR and XOR comparisons
is verified successfully.


 
EXP NO:23 C PROGRAM TO WRITE THE LOGIC FOR THE REQUESTS

Aim:
To write a C program to write the logic for the requests

Algorithm:
1.	Declare variables noshel and noque to store the number of shelves and the number of queries, respectively.
2.	Use scanf to take two integers as input for the number of shelves and queries.
3.	Declare a 2D array shelarr to represent shelves and books, and an array nobookarr to store the number of books on each shelf.
4.	Declare variables k and c to keep track of the book index and the total number of books.
5.	Use a for loop to iterate over the queries.
 
Program:
```
#include <stdio.h>
int s[100][1000],c[100]={0};
int main(){
    int n,q,x,y,t;
    scanf("%d %d",&n,&q);
    while(q--){
        scanf("%d",&t);
        t==1? (scanf("%d %d",&x,&y), s[x][c[x]++]=y):
        t==2?(scanf("%d %d",&x,&y),printf("%d\n",s[x][y])):
        (scanf("%d",&x),printf("%d\n",c[x]));
    }
}
```

Output:


![image](https://github.com/user-attachments/assets/24d22216-610e-4198-a72c-2e597dae9afc)



Result:
Thus, the program to write the logic for the requests is verified successfully.


 
EXP NO:24 C PROGRAM PRINT THE SUM OF THE INTEGERS IN THE ARRAY.

Aim:
To write a C program print the sum of the integers in the array.

Algorithm:
1.	Declare a variable n to store the number of integers.
2.	Use scanf to take an integer n as input.
3.	Declare an array a of size n to store the integers.
4.	Declare a variable sum and initialize it to zero.
5.	Use a for loop to iterate n times:
6.	Use scanf to input each integer and add it to the sum.
7.	Print the final sum using printf.



Program:

```
#include<stdio.h>
#include<stdlib.h>
int main(){
    int n;
    scanf("%d",&n);
    int sum=0;
    int*arr=(int*)malloc(n*sizeof(int*));
    for(int i=0;i<n;i++){
        scanf("%d",&arr[i]);
        sum+=arr[i];
    }
    printf("%d",sum);
}
```

Output:


![image](https://github.com/user-attachments/assets/76837834-4026-4653-b125-5f9225943011)




Result:
Thus, the program prints the sum of the integers in the array is verified successfully.


 
EXP NO 25: C PROGRAM TO COUNT THE NUMBER OF WORDS IN A      SENTENCE

Aim:

To write a C program that counts the number of words in a given sentence.

Algorithm:

1.	Input the sentence: Take a sentence from the user.
2.	Initialize a counter variable: This will keep track of the number of words.
3.	Process each character of the sentence:
o	Iterate through the sentence, checking each character.
o	If a character is not a space, it may belong to a word. If it's the first non-space character after a space or at the start, increment the word count.
4.	Handle spaces and punctuation: Skip over spaces, punctuation marks, and consider each word as a sequence of characters separated by spaces.
5.	Display the result: After processing the sentence, output the total word count.



Program:
```
#include <stdio.h>
#include <ctype.h>

int main() {
    char sentence[1000];
    int i = 0, word_count = 0;
    int in_word = 0;


    fgets(sentence, sizeof(sentence), stdin); 

    while (sentence[i] != '\0') {
        if (isspace(sentence[i]) || ispunct(sentence[i])) {
            in_word = 0; 
        } else if (in_word == 0) {
            in_word = 1; 
            word_count++;
        }
        i++;
    }

    printf("Number of words: %d\n", word_count);
    return 0;
}
```

Output:


![Screenshot 2025-04-26 212609](https://github.com/user-attachments/assets/c7f4e060-db6e-4dca-9a65-913f84496219)



Result:

Thus, the program that counts the number of words in a given sentence is verified 
successfully.
