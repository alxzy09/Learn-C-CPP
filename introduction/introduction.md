# Compiler

Alat penting yang dibutuhkan untuk mengikuti tutorial ini adalah sebuah komputer dan **compiler toolchain** yang mampu mengompilasi kode C++ dan membangun program untuk dapat dijalankannya.

C++ adalah bahasa yang telah banyak berkembang selama bertahun-tahun, dan tutorial ini menjelaskan banyak fitur baru yang baru saja ditambahkan ke dalam bahasa tersebut. Oleh karena itu, agar dapat mengikuti tutorial dengan baik, diperlukan compiler yang terbaru. Compiler tersebut harus mendukung (meskipun hanya sebagian) fitur-fitur yang diperkenalkan oleh standar tahun 2011.

Banyak vendor compiler mendukung fitur-fitur baru ini dalam tingkat yang berbeda-beda. Lihat bagian bawah halaman ini untuk beberapa compiler yang diketahui mendukung fitur-fitur yang dibutuhkan. Beberapa di antaranya gratis!

Jika karena suatu alasan Anda perlu menggunakan compiler yang lebih lama, Anda dapat mengakses versi tutorial yang lebih lama di sini (tidak lagi diperbarui).

## Apa itu Compiler?

Komputer hanya memahami satu bahasa dan bahasa tersebut terdiri dari kumpulan instruksi yang terbuat dari angka satu dan nol. Bahasa komputer ini disebut dengan tepat sebagai **bahasa mesin**.

Satu instruksi untuk komputer mungkin terlihat seperti ini:

```text
00000	10011110
```

Program bahasa mesin pada komputer tertentu yang memungkinkan pengguna memasukkan dua angka, menjumlahkan kedua angka tersebut, dan menampilkan totalnya mungkin mencakup instruksi kode mesin berikut:

```text
00000	10011110
00001	11110100
00010	10011110
00011	11010100
00100	10111111
00101	00000000
```

Seperti yang bisa Anda bayangkan, pemrograman komputer secara langsung dalam bahasa mesin hanya menggunakan angka satu dan nol sangat membosankan dan rentan kesalahan. Untuk mempermudah pemrograman, **bahasa tingkat tinggi** (*high level languages*) telah dikembangkan. Program tingkat tinggi juga mempermudah programmer untuk memeriksa dan memahami program satu sama lain.

Berikut adalah sebagian kode yang ditulis dalam C++ yang memiliki tujuan yang persis sama:

```cpp
int a, b, sum;
     
cin >> a;
cin >> b;
             
sum = a + b;
cout << sum << endl;
```

Bahkan jika Anda belum benar-benar memahami kode di atas, Anda seharusnya dapat menghargai betapa jauh lebih mudahnya memprogram dalam bahasa C++ dibandingkan dengan bahasa mesin.

Karena komputer hanya bisa mengerti bahasa mesin dan manusia ingin menulis dalam bahasa tingkat tinggi, maka bahasa tingkat tinggi harus ditulis ulang (diterjemahkan) ke dalam bahasa mesin pada suatu titik. Hal ini dilakukan oleh program-program khusus yang disebut **compiler**, **interpreter**, atau **assembler** yang tertanam dalam berbagai aplikasi pemrograman.

C++ dirancang sebagai bahasa yang dikompilasi (*compiled language*), yang berarti umumnya diterjemahkan menjadi bahasa mesin yang dapat dipahami secara langsung oleh sistem, membuat program yang dihasilkan sangat efisien. Untuk itu, seperangkat alat dibutuhkan, yang dikenal sebagai **toolchain pengembangan**, yang intinya adalah sebuah compiler dan *linker*-nya.

## Program Konsol (*Console Programs*)

Program konsol adalah program yang menggunakan teks untuk berkomunikasi dengan pengguna dan lingkungannya, seperti mencetak teks ke layar atau membaca masukan dari keyboard.

Program konsol mudah untuk berinteraksi, dan umumnya memiliki perilaku yang dapat diprediksi dan identik di semua platform. Mereka juga sederhana untuk diimplementasikan dan thus sangat berguna untuk mempelajari dasar-dasar bahasa pemrograman: Contoh-contoh dalam tutorial ini semuanya adalah program konsol.

Cara mengompilasi program konsol bergantung pada alat tertentu yang Anda gunakan.

Cara termudah bagi pemula untuk mengompilasi program C++ adalah dengan menggunakan **Integrated Development Environment (IDE)**. IDE umumnya mengintegrasikan beberapa alat pengembangan, termasuk editor teks dan alat untuk mengompilasi program langsung darinya.

Di sini Anda memiliki instruksi tentang cara mengompilasi dan menjalankan program konsol menggunakan berbagai IDE gratis:

| IDE | Platform | Program Konsol |
| :--- | :--- | :--- |
| **Code::blocks** | Windows/Linux/MacOS | Kompilasi program konsol menggunakan Code::blocks |
| **Visual Studio Express** | Windows | Kompilasi program konsol menggunakan VS Express 2013 |
| **Dev-C++** | Windows | Kompilasi program konsol menggunakan Dev-C++ |

Jika kebetulan Anda memiliki lingkungan Linux atau Mac dengan fitur pengembangan, Anda seharusnya dapat mengompilasi salah satu contoh secara langsung dari terminal hanya dengan menyertakan *flag* C++11 dalam perintah compiler:

| Compiler | Platform | Perintah |
| :--- | :--- | :--- |
| **GCC** | Linux, dan lainnya... | `g++ -std=c++0x example.cpp -o example_program` |
| **Clang** | OS X, dan lainnya... | `clang++ -std=c++11 -stdlib=libc++ example.cpp -o example_program` |