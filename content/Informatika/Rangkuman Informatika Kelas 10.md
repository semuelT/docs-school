# Algoritma
>Algoritma adalah suatu kumpulan instruksi terstruktur dan terbatas yang dapat diimplementasikan dalam bentuk program komputer untuk menyelesaikan suatu permasalahan komputasi tertentu. Algoritma merupakan bentuk dari suatu strategi atau ‘resep’ yang kalian gunakan untuk menyelesaikan suatu masalah.
>[[../Media/Informatika-BS-KLS-X.pdf#page=147|Informatika-Kelas-X]]

## Tujuan Menulis Algoritma dengan baik dan benar
>  Algoritma adalah abstraksi dari sebuah program sehingga kemampuan menuliskan algoritma dengan baik akan membantu dalam membuat program yang baik dan benar.
>  [[../Media/Informatika-BS-KLS-X.pdf#page=147|Informatika-Kelas-X]]

> [!info]
> Program ditulis agar dapat dipahami oleh mesin, sedangkan algoritma ditulis agar dapat dipahami oleh manusia.

# Psudocode
> Pseudocode (kode semu atau kode pseudo) adalah suatu bahasa buatan manusia yang sifatnya informal untuk merepresentasikan algoritma.
> [[../Media/Informatika-BS-KLS-X.pdf#page=154|Informatika-Kelas-X]]

> [!info]
> Pseudocode dibuat untuk menutupi kekurangan diagram alir dalam merepresentasikan konsep-konsep pemrograman terstruktur. Pseudocode memungkinkan representasi langkah-langkah yang lebih detail dan dekat dengan bahasa pemrograman.

Baca juga [[./Diagram alir|Diagram alir]]. 
# Bahasa Pemrograman C
>Bahasa Pemrograman C, selanjutnya disebut bahasa C saja, dikembangkan oleh Dennis M. Ritchie dan Brian W. Kernighan pada awal tahun 1970. C memiliki berbagai spesifikasi sebab sejarah yang panjangnya namun spesifikasi yang digunakan paling banyak adalah ISO 9899 yang dibuat ISO/IEC. Versi spesifikasi terbaru ISO 9899 adalah ISO 9899:2018 yang disebut C17.
## Proses dan Fungsi `Compile`
> Kompilator (compiler) yang akan membaca kode bahasa C yang telah ditulis dan mengubahnya menjadi bahasa mesin, atau bahasa assembly. Setelah itu, terdapat sebuah assembler yang akan mengubah bahasa mesin tersebut ke dalam kode biner yang dapat dipahami dan dieksekusi oleh komputer. Terakhir, terdapat sebuah penghubung (linker) yang akan menyatukan beberapa berkas yang dihasilkan dalam proses-proses sebelumnya ke dalam sebuah bentuk berkas yang dapat dieksekusi (executable).

>[!info]
>Pada awalnya, Perangkat lunak tersebut (diatas) terpisah, tetapi untuk memudahkan, akhirnya, dibuatlah sebuah perangkat lunak terintegrasi yang mencakup semua perangkat lunak di atas. Perangkat lunak tersebut disebut lingkungan pengembangan terpadu (integrated development environment). Untuk bahasa C, beberapa IDE yang biasa digunakan ialah Eclipse, Atom, Code::Blocks, Geany, dan Visual Studio. Selain itu, terdapat juga CppDroid,Mobile C, dan Coding C yang dapat digunakan pada ponsel cerdas.

## Tipe-tipe Data Dalam Bahasa C

| Nama Tipe | Jenis Data                                            | Ukuran Memori | Rentang                      |
| --------- | ----------------------------------------------------- | ------------- | ---------------------------- |
| int       | Bilangan Bulat                                        | 4 byte        | -2.1x10^9 hingga 2.1x10^9    |
| short     | Bilangan Bulat                                        | 2 byte        | -32768 hingga 32767          |
| long      | Bilangan Bulat                                        | 8 byte        | -9.2x10^8 hingga 9.2x10^8    |
| float     | Bilangan rill                                         | 4 byte        | 1.2x10^38 hingga 3.4x10^38   |
| double    | Bilangan rill                                         | 8 byte        | 2.3x10^308 hingga 1.7x10^308 |
| char      | Karakter [ASCII](https://id.wikipedia.org/wiki/ASCII) | 1 byte        | -127 hingga 128              |
> Perhatikan bahwa rentang yang diberikan memungkinkan nilai negatif hingga positif, atau disebut tipe data signed. Apabila kalian menambahkan kata kunci unsigned di depan tipe data, tipe data tersebut hanya akan menampung bilangan positif dengan rentang dari 0 hingga 2^jumlah bit - 1.

## Syntax Bahasa Pemrograman C
### Variabel
> Pada matematika, kalian mengenal variabel sebagai sebuah wadah untuk menyimpan suatu nilai. Variabel pada program memiliki fungsi yang sama. Nilai yang diberikan pada sebuah variabel akan disimpan di memori komputer.
```c
// Variabel dalam C memiliki bentuk 
// <tipe_data> <nama_variabel> = <nilai_awal> (Nilai awal opsional).
int totalHarga = 100;
float pi = 3.14;
char hurufA = 'A';
int apakahTua;
```
### Konstanta
>Berbeda dengan variabel yang nilainya dapat berubah, konstanta tidak dapat diubah. Saat dideklarasikan, nilai dari konstanta diberikan dan tidak dapat diubah kembali.
```c
// Cara menulis konstanta sama dengan variabel namun tambahkan `const` didepan.
const float PI = 3.14;
```
### `printf()` dan `scanf()`
#### `printf()`
```c
printf() // Berfungsi untuk mengirimkan output yang diformat (teks) ke konsol (output standar)
// Contoh
#include <stdio.h>
int main() {
	int age = 30;
	printf("Halo, saya berusia %d tahun.\n", age);
	return 0;
 }
// Output
"Halo, saya berusia 30 tahun.";
```
#### `scanf()`
```c
scanf() // Berfungsi untuk membaca input dari input standar (biasanya keyboard)
// Contoh
#include <stdio.h>
int main() {
	int num;
	printf("Masukkan bilangan bulat: ");
	scanf("%d", &num); // contoh dimasukkan 10
	printf("Anda memasukkan: %d\n", num);
	return 0;
 }
 // Output
 "Masukan bilangan bulat:";
 "10"; //input
 "Anda memasukkan: 10";
```

> [!info]
> Apakah kalian lihat `\n` diatas? `\n` adalah salah satu dari `escape sequence`. Lihat dibawah untuk contoh lainnya.
> ```
> \n (newline)
> \t (tab)
> \v (vertical tab)
> \f (new page)
> \b (backspace)
> \r (carrrige return)
> \a (bell, beep)
> \\ (garis miring)
> \" (tanda kutip ganda)
> \` (tanda kutip)
> ```

> Sebuah `\` berarti kita ingin meng`escape` sebuah karakter. Contohnya
> Kita ingin menulis "Quote: "Bla-bla-bla" -Blabber" dalam C kita harus meng`escape` tanda kutip ganda (") dengan `\`. Dalam C teks tersebut menjadi "Quote: \\"Bla-bla-bla\\" -Blabber".

## Format Specifier dalam Bahasa C
> Format specifier dalam bahasa pemrograman C adalah kode-kode khusus yang digunakan dalam fungsi `printf()` dan `scanf()` untuk menunjukkan bagaimana data harus diformat untuk output atau input. Berikut adalah beberapa format specifier umum:

**Tipe Bilangan Bulat:**

- `%d`: Mencetak atau membaca bilangan bulat desimal bertanda.
- `%i`: Sama dengan `%d` (sering digunakan untuk konsistensi).
- `%u`: Mencetak atau membaca bilangan bulat desimal tidak bertanda.
- `%o`: Mencetak atau membaca bilangan bulat oktal tidak bertanda (basis 8).
- `%x`: Mencetak atau membaca bilangan bulat heksadesimal tidak bertanda (basis 16).
- `%X`: Mencetak atau membaca bilangan bulat heksadesimal tidak bertanda dalam huruf besar (basis 16).

**Tipe Titik Mengambang:**

- `%f`: Mencetak atau membaca bilangan titik mengambang presisi tunggal dalam format desimal.
- `%lf`: Mencetak atau membaca bilangan titik mengambang presisi ganda dalam format desimal (sering digunakan untuk presisi lebih tinggi).
- `%e`: Mencetak atau membaca bilangan titik mengambang dalam notasi ilmiah (misalnya, 1.23e+05).
- `%E`: Sama seperti `%e` tetapi menggunakan eksponen huruf besar (misalnya, 1.23E+05).
- `%g`: Mencetak atau membaca bilangan titik mengambang dalam format desimal atau notasi ilmiah, mana yang lebih ringkas.

**Tipe Karakter dan String:**

- `%c`: Mencetak atau membaca satu karakter.
- `%s`: Mencetak atau membaca string yang diakhiri null (urutan karakter).

**Format Specifier Lainnya:**

- `%%`: Mencetak tanda persen literal (%) itu sendiri.
- `%p`: Mencetak alamat pointer dalam format heksadesimal.

## Alur kontrol dalam Bahasa C
> **Alur kontrol** dalam pemrograman C memungkinkan Anda menentukan **bagaimana program Anda akan bercabang dan bereaksi** berdasarkan kondisi tertentu. Berikut adalah ringkasan singkat dari struktur alur kontrol umum yang digunakan dalam C:

**1. Percabangan if-else:**

- Digunakan untuk **mengeksekusi blok kode yang berbeda** berdasarkan **kondisi yang benar atau salah**.
- Sintaks:

```c
if (kondisi) {
  // Blok kode yang dieksekusi jika kondisi benar
} else {
  // Blok kode yang dieksekusi jika kondisi salah
}
```

**Contoh:**

```c
int age = 18;

if (age >= 18) {
  printf("Anda sudah dewasa.\n");
} else {
  printf("Anda masih belum dewasa.\n");
}
```

**2. Percabangan switch-case:**

- Digunakan untuk **mengeksekusi blok kode yang berbeda** berdasarkan **nilai variabel**.
- Sintaks:

```c
switch (variabel) {
  case nilai1:
    // Blok kode untuk nilai1
    break;
  case nilai2:
    // Blok kode untuk nilai2
    break;
  default:
    // Blok kode default (opsional)
}
```

**Contoh:**

```c
char grade = 'B';

switch (grade) {
  case 'A':
    printf("Sangat Bagus!\n");
    break;
  case 'B':
    printf("Bagus!\n");
    break;
  case 'C':
    printf("Cukup.\n");
    break;
  default:
    printf("Nilai tidak valid.\n");
}
```

**3. Perulangan while:**

- Digunakan untuk **mengulangi blok kode** **selama kondisi tertentu benar**.
- Sintaks:

```c
while (kondisi) {
  // Blok kode yang diulang
}
```

**Contoh:**

```c
int i = 1;

while (i <= 5) {
  printf("%d\n", i);
  i++;
}
```

**4. Perulangan do-while:**

- Mirip dengan `while`, tetapi **menjalankan blok kode setidaknya sekali**, **kemudian mengecek kondisinya**.
- Sintaks:

```c
do {
  // Blok kode yang diulang
} while (kondisi);
```

**Contoh:**

```c
int i = 1;

do {
  printf("%d\n", i);
  i++;
} while (i <= 5);
```


# Tanggung Jawab Profesi dalam Bidang Informatika
| Posisi Perkerjaan                                                    | Deskripsi dan Tanggung Jawab                                                                                                                                                                                                        |
| -------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Chief Information Officer<br>(CIO)/Chief Technology<br>Officer (CTO) | Bertanggung jawab pada seluruh aspek terkait<br>teknologi informasi di suatu perusahaan.                                                                                                                                            |
| Computer Programmer                                                  | Menulis program komputer yang telah didesain.                                                                                                                                                                                       |
| Computer Scientist                                                   | Menciptakan suatu prinsip, metode, atau praktik baru<br>di bidang ilmu komputer.                                                                                                                                                    |
| Hardware Engineer                                                    | Menciptakan, mengimplementasikan, dan menguji<br>komponen fisik dari komputer.                                                                                                                                                      |
| Software Engineer                                                    | Mengembangkan, merawat, menguji, mengevaluasi,<br>dan meningkatkan kualitas suatu perangkat lunak<br>berdasarkan kebutuhan yang telah diberikan oleh<br>analis sistem atau arsitek.                                                 |
| Software Developer                                                   | Menganalisis kebutuhan pengguna dan software<br>requirements untuk menentukan kelayakan desain<br>dalam batasan waktu, risiko, kualitas dan biaya.<br>Mengembangkan desain sistem, software, prosedur<br>dan dokumentasi pengujian. |
| Web Developer                                                        | Bertanggung jawab untuk membuat web.                                                                                                                                                                                                |
| Database Administrator                                               | Mengembangkan dan menerapkan pemantauan,<br>kinerja, kapasitas, dan strategi perluasan database.<br>Menginstal, mengonfigurasi, meng-upgrade,<br>memantau, dan melakukan pemeliharaan pada<br>database.                             |
| IT Architect                                                         | Mendesain arsitektur teknologi informasi untuk<br>mendukung proses suatu perusahaan.                                                                                                                                                |
| Network Administrator                                                | Memelihara, mengoperasikan, mengelola, dan<br>mendukung infrastruktur jaringan.                                                                                                                                                     |
| Systems Analyst                                                      | Menganalisis dan menerjemahkan tujuan bisnis<br>menjadi produk-produk, dalam konteks Informatika,<br>produk ini disebut computational artefact, yaitu<br>berupa proses bisnis dan spesifikasi kebutuhan sistem<br>informasinya.     |
| Security Analyst                                                     | Menganalisis dan menerjemahkan aspek keamanan<br>dari sistem yang akan dikembangkan untuk<br>mendukung tujuan bisnis.                                                                                                               |
| Information Researcher                                               | Menciptakan suatu prinsip, metode, atau praktik baru<br>untuk mengolah data dan informasi.                                                                                                                                          |
| Video Game Developer                                                 | Mengembangkan perangkat lunak permainan dan<br>bekerja sama dengan tim profesional kreatif untuk<br>meningkatkan kualitas permainan.                                                                                                |
| Health Information<br>Technician                                     | Mengolah data terkait kesehatan menggunakan<br>prinsip dan praktik informatika.                                                                                                                                                     |
| Data Scientist                                                       | Merancang, mengembangkan, dan menerapkan model<br>statistik prediktif (biasanya pada set data besar)                                                                                                                                |
| Data Engineer                                                        | Mengolah data yang dimiliki perusahaan untuk<br>mendapatkan wawasan baru yang berguna bagi<br>perusahaan.                                                                                                                           |
| Web Designer                                                         | Merancang antarmuka pengguna web untuk<br>memberikan grafik, konten, markup dan skrip.                                                                                                                                              |
| Mobile Apps developer                                                | Bertanggung jawab mengembangkan aplikasi dalam<br>bentuk ponsel cerdas (Mengadaptasi bentuk/dll dari Aplikasi ke bentuk Ponsel Cerdas. Karena PC, Laptop, Tablet, dan Smartphone berbeda dalam banyak Hal.).                        |
