
# Variabel dan Tipe Data

Kegunaan program "Hello World" yang ditunjukkan pada bab sebelumnya cukup dipertanyakan. Kita harus menulis beberapa baris kode, mengompilasinya, lalu mengeksekusi program yang dihasilkan, hanya untuk mendapatkan hasil dari kalimat sederhana yang ditulis di layar. Tentu saja akan jauh lebih cepat jika kita mengetik kalimat output itu sendiri.

Namun, pemrograman tidak terbatas hanya pada mencetak teks sederhana di layar. Agar bisa melangkah lebih jauh dan mampu menulis program yang melakukan tugas-tugas berguna yang benar-benar menghemat pekerjaan kita, kita perlu memperkenalkan konsep **variabel**.

Bayangkan jika saya meminta Anda mengingat angka 5, lalu saya meminta Anda juga untuk menghafal angka 2 pada saat yang bersamaan. Anda baru saja menyimpan dua nilai berbeda dalam memori Anda (5 dan 2). Sekarang, jika saya meminta Anda menambahkan 1 ke angka pertama yang saya sebutkan, Anda seharusnya mempertahankan angka 6 (yaitu 5+1) dan 2 dalam memori Anda. Kemudian kita bisa, misalnya, mengurangi nilai-nilai ini dan mendapatkan 4 sebagai hasil.

Seluruh proses yang dijelaskan di atas adalah sebuah metafora dari apa yang dapat dilakukan komputer dengan dua variabel. Proses yang sama dapat diekspresikan dalam C++ dengan kumpulan pernyataan berikut:

```cpp
a = 5;
b = 2;
a = a + 1;
result = a - b;
```

Jelas, ini adalah contoh yang sangat sederhana, karena kita hanya menggunakan dua nilai bilangan bulat kecil, tetapi bayangkan bahwa komputer Anda dapat menyimpan jutaan angka seperti ini secara bersamaan dan melakukan operasi matematika yang canggih dengannya.

Kita sekarang dapat mendefinisikan variabel sebagai **sebagian kecil memori untuk menyimpan sebuah nilai**.

Setiap variabel memerlukan **nama** yang mengidentifikasinya dan membedakannya dari yang lain. Misalnya, pada kode sebelumnya nama variabelnya adalah `a`, `b`, dan `result`, tetapi kita bisa memberi nama variabel apa pun yang kita bisa buat, selama merupakan **identifier C++ yang valid**.

## Pengidentifikasi (Identifiers)

Pengidentifikasi yang valid adalah rangkaian satu atau lebih huruf, digit, atau karakter garis bawah (`_`). Spasi, tanda baca, dan simbol tidak boleh menjadi bagian dari pengidentifikasi. Selain itu, pengidentifikasi harus selalu dimulai dengan huruf. Mereka juga bisa dimulai dengan karakter garis bawah (`_`), tetapi pengidentifikasi seperti itu -dalam kebanyakan kasus- dianggap dicadangkan untuk kata kunci khusus kompiler atau pengidentifikasi eksternal, serta pengidentifikasi yang mengandung dua karakter garis bawah berturut-turut di mana saja. Dalam tidak ada keadaan pun mereka boleh dimulai dengan digit.

C++ menggunakan sejumlah kata kunci untuk mengidentifikasi operasi dan deskripsi data; oleh karena itu, pengidentifikasi yang dibuat oleh programmer tidak boleh sama dengan kata kunci ini. Kata kunci reserved standar yang tidak dapat digunakan untuk pengidentifikasi buatan programmer adalah:

`alignas`, `alignof`, `and`, `and_eq`, `asm`, `auto`, `bitand`, `bitor`, `bool`, `break`, `case`, `catch`, `char`, `char16_t`, `char32_t`, `class`, `compl`, `const`, `constexpr`, `const_cast`, `continue`, `decltype`, `default`, `delete`, `do`, `double`, `dynamic_cast`, `else`, `enum`, `explicit`, `export`, `extern`, `false`, `float`, `for`, `friend`, `goto`, `if`, `inline`, `int`, `long`, `mutable`, `namespace`, `new`, `noexcept`, `not`, `not_eq`, `nullptr`, `operator`, `or`, `or_eq`, `private`, `protected`, `public`, `register`, `reinterpret_cast`, `return`, `short`, `signed`, `sizeof`, `static`, `static_assert`, `static_cast`, `struct`, `switch`, `template`, `this`, `thread_local`, `throw`, `true`, `try`, `typedef`, `typeid`, `typename`, `union`, `unsigned`, `using`, `virtual`, `void`, `volatile`, `wchar_t`, `while`, `xor`, `xor_eq`

Kompiler tertentu mungkin juga memiliki kata kunci reserved tambahan yang spesifik.

**Sangat penting:** Bahasa C++ adalah bahasa yang "sensitif terhadap huruf besar-kecil" (*case sensitive*). Artinya, pengidentifikasi yang ditulis dengan huruf kapital tidak setara dengan pengidentifikasi lain dengan nama yang sama tetapi ditulis dengan huruf kecil. Dengan demikian, misalnya, variabel `RESULT` tidak sama dengan variabel `result` atau variabel `Result`. Ini adalah tiga pengidentifikasi berbeda yang mengidentifikasi tiga variabel berbeda.

## Tipe Data Dasar (Fundamental Data Types)

Nilai variabel disimpan di suatu tempat di lokasi yang tidak ditentukan dalam memori komputer sebagai nol dan satu. Program kita tidak perlu tahu lokasi pasti di mana variabel disimpan; program cukup merujuknya dengan namanya. Yang perlu diketahui program adalah jenis data yang disimpan dalam variabel tersebut. Menyimpan bilangan bulat sederhana tidak sama dengan menyimpan huruf atau bilangan titik mengambang (*floating-point*) yang besar; meskipun semuanya direpresentasikan menggunakan nol dan satu, mereka tidak diinterpretasikan dengan cara yang sama, dan dalam banyak kasus, mereka tidak menempati jumlah memori yang sama.

Tipe data dasar adalah tipe dasar yang diimplementasikan langsung oleh bahasa yang mewakili unit penyimpanan dasar yang didukung secara native oleh sebagian besar sistem. Mereka terutama dapat diklasifikasikan menjadi:
*   **Tipe Karakter:** Dapat merepresentasikan satu karakter, seperti `'A'` atau `'$'`. Tipe paling dasar adalah `char`, yang merupakan karakter satu byte. Tipe lain juga disediakan untuk karakter yang lebih lebar.
*   **Tipe Bilangan Bulat (Integer):** Dapat menyimpan nilai bilangan bulat, seperti `7` atau `1024`. Mereka ada dalam berbagai ukuran, dan dapat berupa *signed* (bertanda) atau *unsigned* (tidak bertanda), tergantung pada apakah mereka mendukung nilai negatif atau tidak.
*   **Tipe Titik Mengambang (Floating-point):** Dapat merepresentasikan nilai nyata (real), seperti `3.14` atau `0.01`, dengan tingkat presisi yang berbeda, tergantung pada mana dari ketiga tipe titik mengambang yang digunakan.
*   **Tipe Boolean:** Tipe boolean, dikenal di C++ sebagai `bool`, hanya dapat merepresentasikan salah satu dari dua keadaan, `true` (benar) atau `false` (salah).

Berikut adalah daftar lengkap tipe dasar di C++:

| Grup | Nama Tipe* | Catatan pada ukuran / presisi |
| :--- | :--- | :--- |
| **Tipe Karakter** | `char` | Tepat satu byte ukurannya. Setidaknya 8 bit. |
| | `char16_t` | Tidak lebih kecil dari char. Setidaknya 16 bit. |
| | `char32_t` | Tidak lebih kecil dari char16_t. Setidaknya 32 bit. |
| | `wchar_t` | Dapat merepresentasikan set karakter terbesar yang didukung. |
| **Tipe Integer (Signed)** | `signed char` | Ukuran sama dengan char. Setidaknya 8 bit. |
| | `signed short int` | Tidak lebih kecil dari char. Setidaknya 16 bit. |
| | `signed int` | Tidak lebih kecil dari short. Setidaknya 16 bit. |
| | `signed long int` | Tidak lebih kecil dari int. Setidaknya 32 bit. |
| | `signed long long int` | Tidak lebih kecil dari long. Setidaknya 64 bit. |
| **Tipe Integer (Unsigned)** | `unsigned char` | (ukuran sama dengan rekanan signed-nya) |
| | `unsigned short int` | |
| | `unsigned int` | |
| | `unsigned long int` | |
| | `unsigned long long int` | |
| **Tipe Floating-point** | `float` | |
| | `double` | Presisi tidak kurang dari float |
| | `long double` | Presisi tidak kurang dari double |
| **Tipe Boolean** | `bool` | |
| **Tipe Void** | `void` | tidak ada penyimpanan |
| **Pointer Null** | `decltype(nullptr)` | |

\* Nama tipe integer tertentu dapat disingkat tanpa komponen `signed` dan `int`-nya - hanya bagian yang tidak miring yang diperlukan untuk mengidentifikasi tipe, bagian yang miring adalah opsional. Yaitu, `signed short int` dapat disingkat menjadi `signed short`, `short int`, atau cukup `short`; semuanya mengidentifikasi tipe dasar yang sama.

Dalam masing-masing grup di atas, perbedaan antara tipe hanyalah ukurannya (yaitu, seberapa banyak mereka menempati di memori): tipe pertama di setiap grup adalah yang terkecil, dan yang terakhir adalah yang terbesar, dengan setiap tipe setidaknya sebesar tipe sebelumnya dalam grup yang sama. Selain itu, tipe dalam satu grup memiliki properti yang sama.

Perhatikan pada panel di atas bahwa selain `char` (yang memiliki ukuran tepat satu byte), tidak ada dari tipe dasar yang memiliki ukuran standar yang ditentukan (tetapi ukuran minimum, paling banyak). Oleh karena itu, tipe tidak diwajibkan (dan dalam banyak kasus tidak) persis ukuran minimum ini. Ini tidak berarti bahwa tipe-tipe ini memiliki ukuran yang tidak ditentukan, tetapi bahwa tidak ada ukuran standar di seluruh kompiler dan mesin; setiap implementasi kompiler dapat menentukan ukuran untuk tipe-tipe ini yang paling pas dengan arsitektur tempat program akan berjalan. Spesifikasi ukuran yang cukup generik untuk tipe ini memberi bahasa C++ banyak fleksibilitas untuk beradaptasi agar bekerja secara optimal di semua jenis platform, baik sekarang maupun di masa depan.

Ukuran tipe di atas dinyatakan dalam bit; semakin banyak bit yang dimiliki tipe, semakin banyak nilai berbeda yang dapat direpresentasikannya, tetapi pada saat yang sama, juga mengonsumsi lebih banyak ruang di memori:

| Ukuran | Nilai yang dapat direpresentasikan | Catatan |
| :--- | :--- | :--- |
| 8-bit | 256 | = 2^8 |
| 16-bit | 65 536 | = 2^16 |
| 32-bit | 4 294 967 296 | = 2^32 (~4 miliar) |
| 64-bit | 18 446 744 073 709 551 616 | = 2^64 (~18 miliar miliar) |

Untuk tipe integer, memiliki lebih banyak nilai yang dapat direpresentasikan berarti bahwa rentang nilai yang dapat mereka wakili lebih besar; misalnya, integer unsigned 16-bit akan dapat merepresentasikan 65.536 nilai berbeda dalam rentang 0 hingga 65.535, sedangkan rekanan signed-nya akan dapat merepresentasikan, dalam kebanyakan kasus, nilai antara -32.768 dan 32.767. Perhatikan bahwa rentang nilai positif kira-kira setengahnya dalam tipe signed dibandingkan dengan tipe unsigned, karena fakta bahwa satu dari 16 bit digunakan untuk tanda (plus/minus); ini adalah perbedaan rentang yang relatif sederhana, dan jarang membenarkan penggunaan tipe unsigned hanya berdasarkan rentang nilai positif yang dapat mereka wakili.

Untuk tipe titik mengambang, ukuran mempengaruhi presisi mereka, dengan memiliki lebih atau sedikit bit untuk signifikan dan eksponen.

Jika ukuran atau presisi tipe bukan menjadi masalah, maka `char`, `int`, dan `double` biasanya dipilih untuk mewakili karakter, bilangan bulat, dan nilai titik mengambang, masing-masing. Tipe lain dalam grup masing-masing hanya digunakan dalam kasus yang sangat khusus.

Properti tipe dasar dalam sistem dan implementasi kompiler tertentu dapat diperoleh dengan menggunakan kelas `numeric_limits` (lihat header standar `<limits>`). Jika karena suatu alasan, tipe dengan ukuran spesifik dibutuhkan, pustaka mendefinisikan alias tipe ukuran tetap tertentu di header `<cstdint>`.

Tipe-tipe yang dijelaskan di atas (karakter, integer, titik mengambang, dan boolean) secara kolektif dikenal sebagai **tipe aritmatika**. Tetapi ada dua tipe dasar tambahan: `void`, yang mengidentifikasi ketiadaan tipe; dan tipe `nullptr`, yang merupakan tipe pointer khusus. Kedua tipe ini akan dibahas lebih lanjut dalam bab mendatang tentang pointer.

C++ mendukung berbagai macam tipe berdasarkan tipe dasar yang dibahas di atas; tipe lain ini dikenal sebagai **tipe data majemuk** (*compound data types*), dan merupakan salah satu kekuatan utama bahasa C++. Kita juga akan melihatnya lebih detail di bab-bab selanjutnya.

## Deklarasi Variabel

C++ adalah bahasa yang **bertipe kuat** (*strongly-typed*), dan mengharuskan setiap variabel dideklarasikan dengan tipenya sebelum penggunaan pertamanya. Ini memberi tahu kompiler ukuran yang akan dicadangkan di memori untuk variabel tersebut dan cara menginterpretasikan nilainya. Sintaks untuk mendeklarasikan variabel baru di C++ sangat mudah: kita cukup menulis tipe diikuti dengan nama variabel (yaitu, pengidentifikasinya). Sebagai contoh:

```cpp
int a;
float mynumber;
```

Ini adalah dua deklarasi variabel yang valid. Yang pertama mendeklarasikan variabel bertipe `int` dengan pengidentifikasi `a`. Yang kedua mendeklarasikan variabel bertipe `float` dengan pengidentifikasi `mynumber`. Setelah dideklarasikan, variabel `a` dan `mynumber` dapat digunakan di dalam sisa *scope* (lingkup) mereka dalam program.

Jika mendeklarasikan lebih dari satu variabel dengan tipe yang sama, mereka semua dapat dideklarasikan dalam satu pernyataan dengan memisahkan pengidentifikasi mereka dengan koma. Sebagai contoh:

```cpp
int a, b, c;
```

Ini mendeklarasikan tiga variabel (`a`, `b` dan `c`), semuanya bertipe `int`, dan memiliki arti yang persis sama dengan:

```cpp
int a;
int b;
int c;
```

Untuk melihat bagaimana bentuk deklarasi variabel dalam aksi dalam sebuah program, mari kita lihat seluruh kode C++ dari contoh tentang memori mental yang diusulkan di awal bab ini:

```cpp
// operating with variables
#include <iostream>
using namespace std;

int main ()
{
  // declaring variables:
  int a, b;
  int result;

  // process:
  a = 5;
  b = 2;
  a = a + 1;
  result = a - b;

  // print out the result:
  cout << result;

  // terminate the program:
  return 0;
}
```
**Output:**
```text
4
```

Jangan khawatir jika selain deklarasi variabel sendiri terlihat sedikit aneh bagi Anda. Sebagian besar akan dijelaskan lebih rinci di bab-bab mendatang.

## Inisialisasi Variabel

Ketika variabel dalam contoh di atas dideklarasikan, mereka memiliki nilai yang tidak ditentukan sampai mereka diberi nilai untuk pertama kalinya. Tetapi dimungkinkan bagi sebuah variabel untuk memiliki nilai spesifik sejak saat ia dideklarasikan. Ini disebut **inisialisasi variabel**.

Di C++, ada tiga cara untuk menginisialisasi variabel. Ketiganya setara dan mengingatkan pada evolusi bahasa selama bertahun-tahun:

1.  **Inisialisasi gaya C** (karena diwarisi dari bahasa C), terdiri dari menambahkan tanda sama dengan diikuti dengan nilai di mana variabel diinisialisasi:
    ```cpp
    type identifier = initial_value;
    ```
    Misalnya, untuk mendeklarasikan variabel bertipe `int` bernama `x` dan menginisialisasinya ke nilai nol dari saat yang sama saat ia dideklarasikan, kita dapat menulis:
    ```cpp
    int x = 0;
    ```

2.  **Inisialisasi konstruktor** (diperkenalkan oleh bahasa C++), menyertakan nilai awal di antara tanda kurung `(())`:
    ```cpp
    type identifier (initial_value);
    ```
    Misalnya:
    ```cpp
    int x (0);
    ```

3.  **Inisialisasi seragam** (*uniform initialization*), mirip dengan di atas, tetapi menggunakan kurung kurawal (`{}`) alih-alih tanda kurung (ini diperkenalkan oleh revisi standar C++, pada tahun 2011):
    ```cpp
    type identifier {initial_value};
    ```
    Misalnya:
    ```cpp
    int x {0};
    ```

Ketiga cara menginisialisasi variabel tersebut valid dan setara di C++.

```cpp
// initialization of variables
#include <iostream>
using namespace std;

int main ()
{
  int a=5;               // initial value: 5
  int b(3);              // initial value: 3
  int c{2};              // initial value: 2
  int result;            // initial value undetermined

  a = a + b;
  result = a - c;
  cout << result;

  return 0;
}
```
**Output:**
```text
6
```

## Deduksi Tipe: auto dan decltype

Ketika variabel baru diinisialisasi, kompiler dapat mengetahui apa tipe variabel tersebut secara otomatis dari penginisialisasinya. Untuk ini, cukup gunakan `auto` sebagai penentu tipe untuk variabel:

```cpp
int foo = 0;
auto bar = foo;  // sama dengan: int bar = foo; 
```

Di sini, `bar` dideklarasikan sebagai memiliki tipe `auto`; oleh karena itu, tipe `bar` adalah tipe dari nilai yang digunakan untuk menginisialisasinya: dalam hal ini menggunakan tipe `foo`, yaitu `int`.

Variabel yang tidak diinisialisasi juga dapat memanfaatkan deduksi tipe dengan penentu `decltype`:

```cpp
int foo = 0;
decltype(foo) bar;  // sama dengan: int bar; 
```

Di sini, `bar` dideklarasikan memiliki tipe yang sama dengan `foo`.

`auto` dan `decltype` adalah fitur canggih yang baru-baru ini ditambahkan ke bahasa ini. Tetapi fitur deduksi tipe yang mereka perkenalkan dimaksudkan untuk digunakan baik ketika tipe tidak dapat diperoleh dengan cara lain atau ketika menggunakannya meningkatkan keterbacaan kode. Dua contoh di atas mungkin bukan salah satu kasus penggunaan ini. Bahkan mereka mungkin menurunkan keterbacaan, karena, saat membaca kode, seseorang harus mencari tipe `foo` untuk benar-benar mengetahui tipe `bar`.

## Pengantar String

Tipe dasar mewakili tipe paling dasar yang ditangani oleh mesin tempat kode mungkin dijalankan. Tetapi salah satu kekuatan utama bahasa C++ adalah kumpulan tipe majemuknya yang kaya, di mana tipe dasar hanyalah blok bangunan.

Contoh tipe majemuk adalah kelas **`string`**. Variabel dari tipe ini mampu menyimpan urutan karakter, seperti kata atau kalimat. Fitur yang sangat berguna!

Perbedaan pertama dengan tipe data dasar adalah bahwa untuk mendeklarasikan dan menggunakan objek (variabel) dari tipe ini, program perlu menyertakan header di mana tipe tersebut didefinisikan dalam pustaka standar (header `<string>`):

```cpp
// my first string
#include <iostream>
#include <string>
using namespace std;

int main ()
{
  string mystring;
  mystring = "This is a string";
  cout << mystring;
  return 0;
}
```
**Output:**
```text
This is a string
```

Seperti yang Anda lihat pada contoh sebelumnya, string dapat diinisialisasi dengan *string literal* apa pun yang valid, sama seperti variabel tipe numerik dapat diinisialisasi ke *literal* numerik apa pun yang valid. Seperti halnya tipe dasar, semua format inisialisasi valid dengan string:

```cpp
string mystring = "This is a string";
string mystring ("This is a string");
string mystring {"This is a string"};
```

String juga dapat melakukan semua operasi dasar lain yang dapat dilakukan tipe data dasar, seperti dideklarasikan tanpa nilai awal dan mengubah nilainya selama eksekusi:

```cpp
// my first string
#include <iostream>
#include <string>
using namespace std;

int main ()
{
  string mystring;
  mystring = "This is the initial string content";
  cout << mystring << endl;
  mystring = "This is a different string content";
  cout << mystring << endl;
  return 0;
}
```
**Output:**
```text
This is the initial string content
This is a different string content
```

> **Catatan:** memasukkan manipulator `endl` mengakhiri baris (mencetak karakter baris baru dan membersihkan *stream*).

Kelas `string` adalah tipe majemuk. Seperti yang Anda lihat pada contoh di atas, tipe majemuk digunakan dengan cara yang sama seperti tipe dasar: sintaks yang sama digunakan untuk mendeklarasikan variabel dan menginisialisasinya.

Untuk lebih detail tentang string C++ standar, lihat referensi kelas `string`.
