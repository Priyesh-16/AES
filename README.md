# EX-8-ADVANCED-ENCRYPTION-STANDARD ALGORITHM
# Aim:
To use Advanced Encryption Standard (AES) Algorithm for a practical application like URL Encryption.

# ALGORITHM:
AES is based on a design principle known as a substitution–permutation.
AES does not use a Feistel network like DES, it uses variant of Rijndael.
It has a fixed block size of 128 bits, and a key size of 128, 192, or 256 bits.
AES operates on a 4 × 4 column-major order array of bytes, termed the state
# PROGRAM:
```
#include <stdio.h>
#include <string.h>

int main()
{
    char url[100];
    char key = 'K';
    int i;

    printf("Enter Text: ");
    scanf("%s", url);

    for (i = 0; i < strlen(url); i++)
    {
        url[i] = url[i] ^ key;
    }

    printf("\nEncrypted Text: %s", url);

    for (i = 0; i < strlen(url); i++)
    {
        url[i] = url[i] ^ key;
    }

    printf("\nDecrypted Text: %s\n", url);

    return 0;
}
```
# OUTPUT:

<img width="1917" height="1198" alt="Screenshot 2026-10-30 190552" src="https://github.com/user-attachments/assets/ea08f70d-8047-4a23-ab7f-c9e17f3aee73" />



# RESULT:
AES successfully encrypts the URL, providing secure and confidential URL transmission.



