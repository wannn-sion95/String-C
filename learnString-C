// Tugas Pendahuluan Nomor 1

#include <stdio.h>
#include <string.h> // Untuk fungsi strlen

int main()
{
    char str[100]; // Buffer untuk menyimpan string input

    // Meminta input dari pengguna
    printf("Masukkan String: ");
    fgets(str, sizeof(str), stdin);

    // Menghapus karakter newline (\n) yang ditambahkan fgets
    str[strcspn(str, "\n")] = '\0';

    // Menghitung panjang string
    int panjang = strlen(str);

    // Menampilkan hasil
    printf("Jadi panjang stringnya adalah %d\n", panjang);

    return 0;
}

// Tugas Pendahuluan Nomor 2

#include <stdio.h>
#include <string.h>
#include <ctype.h>

int main()
{
    char nama[100];  // Buffer untuk menyimpan input nama
    char hasil[100]; // Buffer untuk menyimpan hasil terbalik
    int panjang, i;

    // Meminta input dari pengguna
    printf("Masukkan nama Anda dalam huruf besar: ");
    fgets(nama, sizeof(nama), stdin);

    // Menghapus karakter newline (\n) yang ditambahkan fgets
    nama[strcspn(nama, "\n")] = '\0';

    // Mengubah semua huruf ke huruf kecil
    for (i = 0; nama[i] != '\0'; i++)
    {
        nama[i] = tolower(nama[i]);
    }

    // Membalikkan urutan huruf
    panjang = strlen(nama);
    for (i = 0; i < panjang; i++)
    {
        hasil[i] = nama[panjang - 1 - i];
    }
    hasil[panjang] = '\0'; // Menambahkan terminator string

    // Menampilkan hasil
    printf("Hasil setelah diubah ke huruf kecil dan dibalik: %s\n", hasil);

    return 0;
}

// Tugas Percobaan Nomor 1

#include <stdio.h>
#include <string.h>
#include <ctype.h>

// Fungsi untuk menghapus spasi dan karakter non-alfabet
void bersihkanKalimat(char *asli, char *bersih)
{
    int i, j = 0;
    for (i = 0; asli[i] != '\0'; i++)
    {
        if (isalnum(asli[i]))
        {                                   // Memeriksa karakter alfanumerik
            bersih[j++] = tolower(asli[i]); // Konversi ke huruf kecil
        }
    }
    bersih[j] = '\0'; // Menambahkan null terminator
}

// Fungsi untuk mengecek apakah string adalah palindrom
int cekPalindrom(char *str)
{
    int panjang = strlen(str);
    for (int i = 0; i < panjang / 2; i++)
    {
        if (str[i] != str[panjang - 1 - i])
        {
            return 0; // Bukan palindrom
        }
    }
    return 1; // Palindrom
}

int main()
{
    char kalimat[200]; // Buffer untuk input
    char bersih[200];  // Buffer untuk kalimat yang dibersihkan

    // Meminta input dari pengguna
    printf("Masukkan sebuah kalimat: ");
    fgets(kalimat, sizeof(kalimat), stdin);

    // Menghapus karakter newline (\n)
    kalimat[strcspn(kalimat, "\n")] = '\0';

    // Membersihkan kalimat (menghapus spasi dan karakter non-alfabet)
    bersihkanKalimat(kalimat, bersih);

    // Mengecek apakah kalimat bersih adalah palindrom
    if (cekPalindrom(bersih))
    {
        printf("Kalimat: %s\nTermasuk PALINDROM\n", kalimat);
    }
    else
    {
        printf("Kalimat: %s\nBukan PALINDROM\n", kalimat);
    }

    return 0;
}

// Tugas Percobaan Nomor 2

#include <stdio.h>
#include <string.h>

int main()
{
    char str[100]; // Buffer untuk menyimpan input string
    int i;

    // Meminta input dari pengguna
    printf("Masukkan sebuah string: ");
    fgets(str, sizeof(str), stdin);

    // Menghapus karakter newline (\n) yang ditambahkan fgets
    str[strcspn(str, "\n")] = '\0';

    // Mengganti huruf 'a' dengan 'i'
    for (i = 0; str[i] != '\0'; i++)
    {
        if (str[i] == 'a')
        {
            str[i] = 'i';
        }
        else if (str[i] == 'A')
        { // Jika huruf 'A' kapital, ubah ke 'I'
            str[i] = 'I';
        }
    }

    // Menampilkan hasil
    printf("Hasil setelah mengganti 'a' dengan 'i': %s\n", str);

    return 0;
}

// Tugas Percobaan Nomor 3

#include <stdio.h>
#include <string.h>

int main()
{
    char string1[100], string2[100]; // Buffer untuk menyimpan kedua string

    // Meminta input string pertama
    printf("Masukkan string pertama: ");
    fgets(string1, sizeof(string1), stdin);

    // Menghapus karakter newline (\n) dari string pertama
    string1[strcspn(string1, "\n")] = '\0';

    // Meminta input string kedua
    printf("Masukkan string kedua: ");
    fgets(string2, sizeof(string2), stdin);

    // Menghapus karakter newline (\n) dari string kedua
    string2[strcspn(string2, "\n")] = '\0';

    // Membandingkan kedua string
    if (strcmp(string1, string2) == 0)
    {
        printf("Kedua string sama\n");
    }
    else
    {
        printf("Kedua string tidak sama\n");
    }

    return 0;
}

// Tugas Percobaan Nomor 4

#include <stdio.h>
#include <string.h>

#define MAX_NAMA 100
#define MAX_PANJANG 100

int main()
{
    int jumlah, i, j;
    char nama[MAX_NAMA][MAX_PANJANG], temp[MAX_PANJANG];

    // Meminta jumlah nama
    printf("Masukkan jumlah nama: ");
    scanf("%d", &jumlah);
    getchar(); // Menghapus karakter newline setelah input jumlah

    // Membaca nama-nama
    for (i = 0; i < jumlah; i++)
    {
        printf("Nama ke-%d: ", i + 1);
        fgets(nama[i], sizeof(nama[i]), stdin);
        nama[i][strcspn(nama[i], "\n")] = '\0'; // Menghapus newline
    }

    // Mengurutkan nama menggunakan bubble sort
    for (i = 0; i < jumlah - 1; i++)
    {
        for (j = 0; j < jumlah - i - 1; j++)
        {
            if (strcmp(nama[j], nama[j + 1]) > 0)
            { // Membandingkan string
                // Menukar nama[j] dan nama[j + 1]
                strcpy(temp, nama[j]);
                strcpy(nama[j], nama[j + 1]);
                strcpy(nama[j + 1], temp);
            }
        }
    }

    // Menampilkan hasil setelah diurutkan
    printf("\nSesudah diurutkan:\n");
    for (i = 0; i < jumlah; i++)
    {
        printf("Nama ke-%d: %s\n", i + 1, nama[i]);
    }

    return 0;
}
