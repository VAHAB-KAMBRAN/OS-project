#include <stdio.h>
#include <stdlib.h>
#include <time.h>

void generatePassword(char *password, int length) {
    // Define characters to use in the password
    const char charset[] = "abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789!@#$%^&*()-_=+";
    int charset_length = sizeof(charset) - 1;

    for (int i = 0; i < length; i++) {
        int index = rand() % charset_length;
        password[i] = charset[index];
    }

    password[length] = '\0'; // Null-terminate the string
}

int main() {
    srand(time(NULL)); // Seed the random number generator with the current time

    int password_length;
    printf("Enter the password length: ");
    scanf("%d", &password_length);

    if (password_length <= 0) {
        printf("Password length should be greater than 0.\n");
        return 1;
    }

    char password[password_length + 1]; // +1 for the null terminator
    generatePassword(password, password_length);

    printf("Generated Password: %s\n", password);

    return 0;
}
