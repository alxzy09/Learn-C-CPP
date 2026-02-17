# Struktur Program

Cara terbaik untuk mempelajari bahasa pemrograman adalah dengan menulis program. Biasanya, program pertama yang ditulis oleh pemula adalah program yang disebut **"Hello World"**, yang secara sederhana hanya mencetak teks "Hello World" ke layar komputer Anda. Meskipun sangat sederhana, program ini mengandung semua komponen fundamental yang dimiliki program C++:

```cpp
// my first program in C++
#include <iostream>

int main()
{
  std::cout << "Hello World!";
}
```
**Output:**
```text
Hello World!
```

Panel kiri di atas menunjukkan kode C++ untuk program ini. Panel kanan menunjukkan hasil ketika program dieksekusi oleh komputer. Angka abu-abu di sebelah kiri panel adalah nomor baris untuk memudahkan diskusi program dan penelusuran kesalahan (error). Angka-angka tersebut bukan bagian dari program.

Mari kita periksa program ini baris demi baris:

### Baris 1: `// my first program in C++`
Dua tanda garis miring (`//`) menunjukkan bahwa sisa baris tersebut adalah **komentar** yang disisipkan oleh programmer tetapi tidak berpengaruh pada perilaku program. Programmer menggunakannya untuk menyertakan penjelasan singkat atau observasi mengenai kode atau program. Dalam hal ini, ini adalah deskripsi pengantar singkat tentang program.

### Baris 2: `#include <iostream>`
Baris yang diawali dengan tanda pagar (`#`) adalah **direktif** yang dibaca dan diinterpretasikan oleh apa yang dikenal sebagai **preprocessor**. Ini adalah baris khusus yang diinterpretasikan sebelum kompilasi program itu sendiri dimulai. Dalam hal ini, direktif `#include <iostream>`, menginstruksikan preprocessor untuk menyertakan bagian kode standar C++ yang dikenal sebagai *header* **iostream**, yang memungkinkan dilakukannya operasi input dan output standar, seperti menulis output program ini (Hello World) ke layar.

### Baris 3: Baris kosong
Baris kosong tidak berpengaruh pada program. Baris ini hanya meningkatkan keterbacaan kode.

### Baris 4: `int main ()`
Baris ini memulai deklarasi sebuah **fungsi**. Pada dasarnya, fungsi adalah kumpulan pernyataan kode yang diberi nama: dalam hal ini, ini memberikan nama **"main"** pada kumpulan pernyataan kode yang mengikutinya. Fungsi akan dibahas secara rinci di bab selanjutnya, pada dasarnya, definisinya diperkenalkan dengan urutan sebuah tipe (`int`), sebuah nama (`main`), dan sepasang tanda kurung (`()`), yang opsional menyertakan parameter.

Fungsi bernama **main** adalah fungsi khusus di semua program C++; ini adalah fungsi yang dipanggil ketika program dijalankan. Eksekusi semua program C++ dimulai dari fungsi main, terlepas dari di mana fungsi tersebut sebenarnya berada dalam kode.

### Baris 5 dan 7: `{` dan `}`
Tanda kurung kurawal buka (`{`) pada baris 5 menunjukkan awal dari definisi fungsi main, dan tanda kurung kurawal tutup (`}`) pada baris 7, menunjukkan akhirnya. Segala sesuatu di antara tanda kurung kurawal ini adalah **badan fungsi** yang mendefinisikan apa yang terjadi ketika main dipanggil. Semua fungsi menggunakan tanda kurung kurawal untuk menunjukkan awal dan akhir dari definisi mereka.

### Baris 6: `std::cout << "Hello World!";`
Baris ini adalah **pernyataan** (statement) C++. Pernyataan adalah ekspresi yang sebenarnya dapat menghasilkan beberapa efek. Ini adalah "daging" dari program, yang menentukan perilaku aktualnya. Pernyataan dieksekusi dalam urutan yang sama seperti mereka muncul dalam tubuh fungsi.

Pernyataan ini memiliki tiga bagian:
1.  `std::cout`, yang mengidentifikasi perangkat output karakter standar (biasanya, ini adalah layar komputer).
2.  Operator penyisipan (`<<`), yang menunjukkan bahwa apa yang mengikutinya disisipkan ke dalam `std::cout`.
3.  Kalimat dalam tanda kutip (`"Hello world!"`), adalah konten yang disisipkan ke dalam output standar.

Perhatikan bahwa pernyataan berakhir dengan titik koma (`;`). Karakter ini menandai akhir dari pernyataan, sama seperti tanda titik mengakhiri kalimat dalam bahasa Inggris. Semua pernyataan C++ harus diakhiri dengan karakter titik koma. Salah satu kesalahan sintaks paling umum di C++ adalah lupa mengakhiri pernyataan dengan titik koma.

Anda mungkin telah memperhatikan bahwa tidak semua baris program ini melakukan tindakan ketika kode dieksekusi. Ada baris yang berisi komentar (diawali dengan `//`). Ada baris dengan direktif untuk preprocessor (diawali dengan `#`). Ada baris yang mendefinisikan sebuah fungsi (dalam hal ini, fungsi main). Dan, terakhir, baris dengan pernyataan yang diakhiri dengan titik koma (penyisipan ke cout), yang berada di dalam blok yang dibatasi oleh tanda kurung kurawal (`{ }`) dari fungsi main.

Program telah distrukturisasi dalam baris yang berbeda dan memiliki indentasi yang benar, agar lebih mudah dipahami oleh manusia yang membacanya. Tetapi C++ tidak memiliki aturan ketat tentang indentasi atau cara membagi instruksi dalam baris yang berbeda. Sebagai contoh, alih-alih:

```cpp
int main ()
{
  std::cout << " Hello World!";
}
```

Kita bisa menulisnya:
```cpp
int main () { std::cout << "Hello World!"; }
```

Semuanya dalam satu baris, dan ini akan memiliki arti yang persis sama dengan kode sebelumnya.

Di C++, pemisahan antara pernyataan ditentukan dengan titik koma di akhir (`;`), dengan pemisahan ke baris yang berbeda sama sekali tidak berpengaruh untuk tujuan ini. Banyak pernyataan dapat ditulis dalam satu baris, atau setiap pernyataan bisa berada di barisnya sendiri. Pembagian kode dalam baris yang berbeda hanya berfungsi untuk membuatnya lebih mudah dibaca dan skematis bagi manusia yang mungkin membacanya, tetapi tidak berpengaruh pada perilaku aktual program.

Sekarang, mari kita tambahkan pernyataan tambahan ke program pertama kita:

```cpp
// my second program in C++
#include <iostream>

int main ()
{
  std::cout << "Hello World! ";
  std::cout << "I'm a C++ program";
}
```
**Output:**
```text
Hello World! I'm a C++ program
```

Dalam kasus ini, program melakukan dua penyisipan ke dalam `std::cout` dalam dua pernyataan berbeda. Sekali lagi, pemisahan dalam baris kode yang berbeda hanya memberikan keterbacaan yang lebih besar pada program, karena main bisa didefinisikan dengan cara yang sama validnya seperti ini:

```cpp
int main () { std::cout << " Hello World! "; std::cout << " I'm a C++ program "; }
```

Kode sumber juga bisa dibagi menjadi lebih banyak baris kode, seperti:

```cpp
int main ()
{
  std::cout <<
    "Hello World!";
  std::cout
    << "I'm a C++ program";
}
```

Dan hasilnya akan sama persis dengan contoh sebelumnya.

**Direktif preprocessor** (yang diawali dengan `#`) dikecualikan dari aturan umum ini karena mereka bukan pernyataan. Mereka adalah baris yang dibaca dan diproses oleh preprocessor sebelum kompilasi yang sebenarnya dimulai. Direktif preprocessor harus ditentukan di baris mereka sendiri dan, karena mereka bukan pernyataan, tidak harus diakhiri dengan titik koma (`;`).

## Komentar

Seperti disebutkan di atas, komentar tidak mempengaruhi operasi program; namun, mereka menyediakan alat penting untuk mendokumentasikan langsung dalam kode sumber apa yang dilakukan program dan bagaimana cara kerjanya.

C++ mendukung dua cara untuk memberi komentar pada kode:

```cpp
// line comment
/* block comment */
```

Yang pertama, dikenal sebagai **komentar baris**, membuang semua mulai dari di mana pasangan tanda garis miring (`//`) ditemukan hingga akhir baris yang sama. Yang kedua, dikenal sebagai **komentar blok**, membuang semua antara karakter `/*` dan kemunculan pertama karakter `*/`, dengan kemungkinan menyertakan beberapa baris.

Mari kita tambahkan komentar ke program kedua kita:

```cpp
/* my second program in C++
   with more comments */

#include <iostream>

int main ()
{
  std::cout << "Hello World! ";     // prints Hello World!
  std::cout << "I'm a C++ program"; // prints I'm a C++ program
}
```
**Output:**
```text
Hello World! I'm a C++ program
```

Jika komentar disertakan dalam kode sumber program tanpa menggunakan kombinasi karakter komentar `//`, `/*` atau `*/`, kompiler akan menganggapnya seolah-olah mereka adalah ekspresi C++, kemungkinan besar menyebabkan kompilasi gagal dengan satu, atau beberapa, pesan kesalahan.

## Using namespace std

Jika Anda pernah melihat kode C++ sebelumnya, Anda mungkin pernah melihat `cout` digunakan alih-alih `std::cout`. Keduanya menamai objek yang sama: yang pertama menggunakan nama yang tidak memenuhi syarat (`cout`), sedangkan yang kedua memenuhi syarat langsung dalam namespace `std` (sebagai `std::cout`).

`cout` adalah bagian dari pustaka standar, dan semua elemen di pustaka standar C++ dideklarasikan dalam apa yang disebut **namespace**: namespace `std`.

Agar dapat mengacu pada elemen di namespace `std`, program harus memenuhi syarat setiap penggunaan elemen pustaka (seperti yang telah kita lakukan dengan memberikan awalan `cout` dengan `std::`), atau memperkenalkan visibilitas komponennya. Cara paling khas untuk memperkenalkan visibilitas komponen ini adalah melalui deklarasi `using`:

```cpp
using namespace std;
```

Deklarasi di atas memungkinkan semua elemen di namespace `std` diakses dengan cara yang tidak memenuhi syarat (tanpa awalan `std::`).

Dengan mengingat hal ini, contoh terakhir dapat ditulis ulang untuk membuat penggunaan `cout` yang tidak memenuhi syarat sebagai:

```cpp
// my second program in C++
#include <iostream>
using namespace std;

int main ()
{
  cout << "Hello World! ";
  cout << "I'm a C++ program";
}
```
**Output:**
```text
Hello World! I'm a C++ program
```

Kedua cara mengakses elemen namespace `std` (kualifikasi eksplisit dan deklarasi `using`) valid di C++ dan menghasilkan perilaku yang persis sama. Untuk kesederhanaan, dan untuk meningkatkan keterbacaan, contoh dalam tutorial ini akan lebih sering menggunakan pendekatan terakhir dengan deklarasi `using`, meskipun perlu dicatat bahwa kualifikasi eksplisit adalah satu-satunya cara untuk menjamin bahwa tabrakan nama (name collisions) tidak pernah terjadi. Namespace dijelaskan lebih detail di bab selanjutnya.