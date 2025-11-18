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

int main() {
    char text[100];
    int shift;

    printf("Enter a message: ");
    fgets(text, sizeof(text), stdin);

    printf("Enter shift value: ");
    scanf("%d", &shift);

    for (int i = 0; text[i] != '\0'; i++) {
        char ch = text[i];

        if (ch >= 'A' && ch <= 'Z') {
            ch = ((ch - 'A' + shift) % 26) + 'A';
        }
        else if (ch >= 'a' && ch <= 'z') {
            ch = ((ch - 'a' + shift) % 26) + 'a';
        }

        text[i] = ch;
    }

    printf("Encrypted: %s", text);

    for (int i = 0; text[i] != '\0'; i++) {
        char ch = text[i];

        if (ch >= 'A' && ch <= 'Z') {
            ch = ((ch - 'A' - shift + 26) % 26) + 'A';
        }
        else if (ch >= 'a' && ch <= 'z') {
            ch = ((ch - 'a' - shift + 26) % 26) + 'a';
        }

        text[i] = ch;
    }

    printf("Decrypted: %s", text);

    return 0;
}

```

## OUTPUT:

<img width="832" height="405" alt="image" src="https://github.com/user-attachments/assets/53f4b448-02e0-47b3-8b80-aac0871625c0" />


## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.
