# ini<stdio.h>
#include <stdlib.h>
#include <time.h>

#define WITH 40
#define HEIGHT 20

void drawDoodle() {
    char doodlenum[] = {'*', '#', '@', '%', '&', '+', '='};
    int num = sizeof(doodleChars) / sizeof(doodleChars[0]);

    srand(time(0)); // Seed the random number generator

    for (int y = 0; y < HEIGHT; y++) {
        for (int x = 0; x < WIDTH; x++) {
            char ch = doodleChars[rand() % numChars];
            printf("%c ", ch);
        }
        printf("\n");
    }
}

int main() {
    printf("Your Random ASCII Doodle:\n\n");
    drawDoodle();
    return 0;
}
