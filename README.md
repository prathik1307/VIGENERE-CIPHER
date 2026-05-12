# VIGENERE-CIPHER
## EX. NO: 4
### NAME: PRATHIKSHA R
### REG NO : 212224040244

## PROGRAM
```
#include <stdio.h>
#include <string.h>

void vigenereCipher(char *text, char *key, int decrypt) {
    int len = strlen(text), keyLen = strlen(key);

    for (int i = 0; i < len; i++) {
        int shift = key[i % keyLen] - 'A';
        text[i] = 'A' + (text[i] - 'A' + (decrypt ? 26 - shift : shift)) % 26;
    }
}

int main() {
    char text[100], key[100];

    printf("Enter text (UPPERCASE): ");
    scanf("%s", text);

    printf("Enter key (UPPERCASE): ");
    scanf("%s", key);

    vigenereCipher(text, key, 0);
    printf("Encrypted Message: %s\n", text);

    vigenereCipher(text, key, 1);
    printf("Decrypted Message: %s\n", text);

    return 0;
}
```
## OUTPUT
<img width="1875" height="788" alt="image" src="https://github.com/user-attachments/assets/40e29a5c-4755-40c3-8d12-e48914a19ac1" />

## RESULT
The code is excuted successfully 
