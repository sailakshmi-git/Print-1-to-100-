# Print-1-to-100-
Write a C program to print the numbers from 1 to 100 but avoid printing multiples of 3 and number containing digit 5(5,15,25,35,..). Use continue in the program.

Program:

```
#include <stdio.h>

int containsFive(int num) {
    while(num > 0) {
        if(num % 10 == 5)
            return 1;
        num /= 10;
    }
    return 0;
}

int main() {
    for(int i = 1; i <= 100; i++) {
        if(i % 3 == 0 || containsFive(i)) {
            continue;
        }
        printf("%d ", i);
    }
    return 0;
}
```

Output:

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/317cd593-f480-4f44-8f46-f75eda827b31" />
