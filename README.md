#include <stdio.h>

#include <string.h>

int main() {

   int a, b;
   int sum, score;
   score = 1;
   sum = 0;
   char s[80];
   scanf("%d", &a);
   for (int i = 0; i < a; i++) {
      scanf("%s", s);
      for (int j = 0; j<strlen(s); j++) {
         if (s[j] == 'O') {
            sum += score;
            score++;
         }
         else if (s[j] == 'X') score = 1;
      }
      printf("%d", sum);
   }

}
