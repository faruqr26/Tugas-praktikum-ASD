
SS SOURCE CODE :

![Cuplikan layar 2024-03-14 083841](https://github.com/faruqr26/Tugas-praktikum-ASD/assets/163359023/598d1a6e-92dd-476f-b9cc-da5580df74bc)
![Cuplikan layar 2024-03-14 084059](https://github.com/faruqr26/Tugas-praktikum-ASD/assets/163359023/593a51a8-ddfc-43da-b58e-82b3bb7e4d7b)

OUTPUT :

![image](https://github.com/faruqr26/Tugas-praktikum-ASD/assets/163359023/282cd4e0-bb62-4c02-8d20-6feb372dc51d)

INPUT FILE TXT :

![Cuplikan layar 2024-03-14 075146](https://github.com/faruqr26/Tugas-praktikum-ASD/assets/163359023/34746c2d-05ef-4de0-b5c7-b43a1a35381c)



PENJELASAN CODE : 

1. #include <stdio.h>       : Library standar input-output
2. #include <stdlib.h>      : Library standar untuk fungsi-fungsi umum
3. #include <string.h>      : Library standar untuk manipulasi string
4. #define MAX_LENGTH 10    : Panjang maksimum teks
5. #define MIN_LENGTH 7     : Panjang minimum teks
6. void lessThanRequired (int* lengthOfText)  : Fungsi untuk teks kurang dari panjang minimum
7. printf("The length of your text is less than specified, please update your text\n");   : Mencetak pesan
8. *lengthOfText = MIN_LENGTH;   : Mengubah panjang teks menjadi panjang minimum
9. void equalThanRequired (int* lengthOfText)   : Fungsi untuk teks sama dengan panjang minimum
10. printf("Thank you, Your text length is correct\n");   : Mencetak pesan
11. (void) lengthOfText;   : Memanfaatkan variabel lengthOfText agar tidak muncul warning "unused parameter"
12. void moreThanRequired (int* lengthOfText)   : Fungsi untuk teks lebih dari panjang minimum
13.printf("Your text is too long, please reduce the text\n");   : Mencetak pesan
14.*lengthOfText = MIN_LENGTH;   : Mengubah panjang teks menjadi panjang minimum
15. int checkLenghtRequirement(char* text)   : Fungsi untuk memeriksa panjang teks
16. int length = strlen(text);   : Menghitung panjang teks
17. if (length < MIN_LENGTH)   : Jika panjang kurang dari minimum
18. return 0;   : Mengembalikan 0
19. else if (length == MIN_LENGTH)   : Jika panjang sama dengan minimum
20. return 1;   : Mengembalikan 1
21. else   : Jika panjang lebih dari minimum
22. return 2;   : Mengembalikan 2
23. int lengthOfText, selectOption;   : Deklarasi variabel panjang teks dan opsi pilihan
24. FILE *fptr = NULL;   : Deklarasi pointer ke file
25.char text[MAX_LENGTH];   : Deklarasi array untuk menyimpan teks
26. fptr = fopen("file.txt", "w");   : Membuka file untuk ditulis
27. if(fptr == NULL){   : Jika file tidak dapat dibuka
28. printf("Erorr");   : Mencetak pesan error
29. exit(1);   : Menghentikan program
30. fgets(text, MAX_LENGTH, fptr);   : Membaca teks dari file
31. fclose(fptr);   : Menutup file
32. selectOption = checkLenghtRequirement(text);   : Memeriksa panjang teks
33. void (functionArray[3])(int) = {lessThanRequired, equalThanRequired, moreThanRequired};   : Array fungsi pointer
34. functionArray[selectOption](&lengthOfText);   : Memanggil fungsi sesuai dengan opsi pilihan
35. printf("\nThe Length is updated to %d", lengthOfText);   : Mencetak panjang teks yang telah diperbarui
36. return 0;   : Mengembalikan nilai 0 untuk menandakan program berjalan dengan sukses

