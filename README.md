# STRING-MANIPULATIONS-USING-LOOPS-SOURCE CODE: #include <iostream.h> #include <string.h> #include <conio.h> void reverseString(char *str) { int start = 0; int end = strlen(str) - 1; char temp; while (start < end) { temp = str[start]; str[start] = str[end]; str[end] = temp; start++; end--; } } int stringLength(const char*str) { int length=0; while(*str!='\0'){ length++; str++; } return length; } void concatenateStrings(char *str1, const char *str2) { while (*str1 != '\0') { str1++;  } while (*str2 != '\0') {  *str1 = *str2;  str1++;  str2++;  }  *str1 = '\0'; } void convertToLowercase(char *str) { while (*str != '\0') {  if (*str >= 'A' && *str <= 'Z') {  *str += 32; } str++; } } void convertToUppercase(char *str) { while (*str != '\0') { if (*str >= 'a' && *str <= 'z') { *str -= 32; } str++; } } void main() { char str[100]; char str1[100]="Hello"; clrscr(); cout<<"Enter a string:"; cin.getline(str,100); concatenateStrings(str1, str); cout << "Concatenated String: " << str1 << endl; int length=stringLength(str); cout<<"Length of the string:" << length << endl; convertToLowercase(str); cout << "String in Lowercase: " << str << endl; convertToUppercase(str); cout << "String in Uppercase: " << str << endl; reverseString(str); cout<<"Reverse string:"<<str<<endl; getch(); } 
