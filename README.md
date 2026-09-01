# EX. NO: 1(A) : IMPLEMENTATION OF CAESAR CIPHER

## Name:Guru Prasad D.R.
## Reg No:212225040104

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
#include <string.h>

int main()
{
    char text[100], decrypted[100];
    int key, i;

    printf("Enter the plain text: ");
    scanf("%s", text);

    printf("Enter the key value: ");
    scanf("%d", &key);

    // Encryption
    for (i = 0; text[i] != '\0'; i++)
    {
        if (text[i] >= 'A' && text[i] <= 'Z')
        {
            text[i] = ((text[i] - 'A' + key) % 26 + 26) % 26 + 'A';
        }
        else if (text[i] >= 'a' && text[i] <= 'z')
        {
            text[i] = ((text[i] - 'a' + key) % 26 + 26) % 26 + 'a';
        }
    }

    printf("Cipher Text: %s\n", text);

    // Copy cipher text for decryption
    strcpy(decrypted, text);

    // Decryption
    for (i = 0; decrypted[i] != '\0'; i++)
    {
        if (decrypted[i] >= 'A' && decrypted[i] <= 'Z')
        {
            decrypted[i] = ((decrypted[i] - 'A' - key) % 26 + 26) % 26 + 'A';
        }
        else if (decrypted[i] >= 'a' && decrypted[i] <= 'z')
        {
            decrypted[i] = ((decrypted[i] - 'a' - key) % 26 + 26) % 26 + 'a';
        }
    }

    printf("Decrypted Text: %s\n", decrypted);

    return 0;
}
```
## OUTPUT:
<img width="552" height="243" alt="image" src="https://github.com/user-attachments/assets/9f407267-408b-4998-8cdc-4fee497ab5f8" />


## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.
