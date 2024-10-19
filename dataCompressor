#include <stdio.h>
#include <string.h>

void encode(const char *input, char *encoded) {
    // Mapping based on your specification
    char *mapping[26] = {
        "a",  // A
        "b",  // B
        "c",  // C
        "d",  // D
        "aa", // E
        "bb", // F
        "cc", // G
        "dd", // H
        "ab", // I
        "ba", // J
        "ac", // K
        "ca", // L
        "ad", // M
        "da", // N
        "bc", // O
        "cb", // P
        "bd", // Q
        "db", // R
        "cd", // S
        "dc", // T
        "aaa", // U
        "bbb", // V
        "ccc", // W
        "ddd", // X
        "abc", // Y
        "adb"  // Z
    };

    int length = strlen(input);
    int index = 0;

    for (int i = 0; i < length; i++) {
        char c = input[i];
        if (c >= 'a' && c <= 'z') {
            index = c - 'a';
            strcat(encoded, mapping[index]);
        } else if (c >= 'A' && c <= 'Z') {
            index = c - 'A';
            strcat(encoded, mapping[index]);
        }
    }
}

void convertToBinary(char *encoded, char *binary) {
    int len = strlen(encoded);
    for (int i = 0; i < len; i++) {
        if (encoded[i] == 'a') {
            strcat(binary, "00");
        } else if (encoded[i] == 'b') {
            strcat(binary, "01");
        } else if (encoded[i] == 'c') {
            strcat(binary, "10");
        } else if (encoded[i] == 'd') {
            strcat(binary, "11");
        }
    }
}

int main() {
    char input[100];
    char encoded[300] = ""; // To store the encoded string
    char binary[600] = "";  // To store the binary representation

    printf("Enter a string to encode: ");
    scanf("%s", input);

    // Display original bytes
    size_t originalSize = strlen(input);
    printf("Original byte size: %lu\n", originalSize);

    // Encoding the string
    encode(input, encoded);
    printf("Encoded string: %s\n", encoded);

    // Convert to binary
    convertToBinary(encoded, binary);
    printf("Binary representation: %s\n", binary);

    // Calculate final byte size
    size_t finalSize = strlen(binary) / 8; // In bytes (8 bits = 1 byte)
    printf("Final byte size: %lu\n", finalSize);

    // Calculate and display compression
    if (finalSize < originalSize) {
    double compressionPercentage = (1.0 - (double)finalSize / originalSize) * 100;
    printf("Compression achieved: %.2f%%\n", compressionPercentage);
} else {
    printf("No compression achieved.\n");
}

    return 0;
}
