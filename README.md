# EX. NO: 1(A) : IMPLEMENTATION OF CAESAR CIPHER

-AADHITHAN B 212224040001

## AIM:
To implement the simple substitution technique named Caesar cipher using C language.

## ALOGORITHM:

STEP-1: Read the plain text from the user.

STEP-2: Read the key value from the user.

STEP-3: If the key is positive then encrypt the text by adding the key with each character in the plain text.

STEP-4: Else subtract the key from the plain text.

STEP-5: Display the cipher text obtained above.

## PROGRAM:
```
#include <stdio.h> 
#include <ctype.h> // for isupper(), islower() 
 
void encrypt(char text[], int shift) { 
    for (int i = 0; text[i] != '\0'; i++) { 
        if (isupper(text[i])) { 
            text[i] = (text[i] - 'A' + shift) % 26 + 'A'; 
        } 
        else if (islower(text[i])) { 
            text[i] = (text[i] - 'a' + shift) % 26 + 'a'; 
        } 
    } 
} 
// Function to decrypt text 
void decrypt(char text[], int shift) { 
    for (int i = 0; text[i] != '\0'; i++) { 
        if (isupper(text[i])) { 
            text[i] = (text[i] - 'A' - shift + 26) % 26 + 'A'; 
        } 
        else if (islower(text[i])) { 
            text[i] = (text[i] - 'a' - shift + 26) % 26 + 'a'; 
        } 
    } 
} 
int main() { 
char text[100]; 
int shift; 
printf("Enter a message: "); 
fgets(text, sizeof(text), stdin); // read input including spaces 
printf("Enter shift key: "); 
scanf("%d", &shift); 
encrypt(text, shift); 
printf("Encrypted text: %s", text); 
decrypt(text, shift); 
printf("Decrypted text: %s", text); 
return 0; 
}
```

## OUTPUT:

<img width="832" height="405" alt="image" src="https://github.com/user-attachments/assets/53f4b448-02e0-47b3-8b80-aac0871625c0" />


## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.
