
# 📚 Repositori Belajar C++ (Source Code & Tutorial)

Selamat datang di repository ini! Repository ini berisi kumpulan kode sumber (source code) dan materi pembelajaran bahasa pemrograman C++ yang disusun secara sistematis mulai dari dasar hingga konsep lanjut.

Materi di sini disusun mengikuti kurikulum standar pemrograman C++ modern (mendukung standar C++11).

---

## 1. Persiapan Lingkungan: Compiler & Tools

Sebelum mulai menulis kode, penting untuk memahami alat-alat yang digunakan.

### Compiler

Alat penting yang dibutuhkan untuk mengikuti tutorial ini adalah sebuah komputer dan **compiler toolchain** yang mampu mengompilasi kode C++ dan membangun program untuk dapat dijalankannya.

C++ adalah bahasa yang telah banyak berkembang selama bertahun-tahun. Tutorial ini menjelaskan banyak fitur baru yang ditambahkan ke dalam bahasa tersebut. Oleh karena itu, agar dapat mengikuti tutorial dengan baik, diperlukan compiler yang terbaru yang mendukung (meskipun hanya sebagian) fitur-fitur yang diperkenalkan oleh standar tahun **2011**.

Banyak vendor compiler mendukung fitur-fitur baru ini dalam tingkat yang berbeda. Beberapa compiler di antaranya gratis!

#### Apa itu Compiler?

Komputer hanya memahami satu bahasa: **bahasa mesin**, yang terdiri dari kumpulan instruksi berupa angka 1 dan 0. Sebagai contoh, instruksi mesin terlihat seperti ini:

```text
00000	10011110
```

Programming langsung menggunakan bahasa mesin sangat membosankan dan rentan kesalahan. Untuk mempermudah, manusia menggunakan **bahasa tingkat tinggi** (*high level languages*) seperti C++.

Contoh kode C++ untuk menjumlahkan dua angka:

```cpp
int a, b, sum;
     
cin >> a;
cin >> b;
             
sum = a + b;
cout << sum << endl;
```

Karena komputer hanya mengerti bahasa mesin, kode C++ harus diterjemahkan. Penerjemahan ini dilakukan oleh program khusus yang disebut **Compiler**.

### Program Konsol

Tutorial ini berfokus pada **program konsol** (program berbasis teks). Program ini mudah diimplementasikan dan memiliki perilaku yang konsisten di semua platform, menjadikannya cara terbaik untuk mempelajari sintaks dasar dan logika pemrograman.

### Cara Mengompilasi

Anda bisa menggunakan IDE (Graphics) atau Command Line (Teks).

#### A. Menggunakan IDE (Cara Termudah)

| IDE | Platform | Keterangan |
| :--- | :--- | :--- |
| **Code::Blocks** | Win/Linux/Mac | Gratis dan open-source. |
| **Visual Studio** | Windows | IDE populer dari Microsoft. |
| **Dev-C++** | Windows | Ringan dan sederhana untuk pemula. |

#### B. Menggunakan Terminal / Command Line

Jika Anda menggunakan Linux atau MacOS, Anda dapat mengompilasi contoh langsung dari terminal dengan perintah berikut (pastikan flag C++11 aktif):

| Compiler | Perintah Contoh |
| :--- | :--- |
| **GCC** | `g++ -std=c++0x nama_file.cpp -o nama_program` |
| **Clang** | `clang++ -std=c++11 -stdlib=libc++ nama_file.cpp -o nama_program` |

---

## 2. Struktur Materi & Source Code

Berikut adalah daftar isi (Syllabus) lengkap yang mencakup topik-topik dalam repository ini. Klik pada topik untuk melihat contoh kode sumber dan penjelasannya.

### 📂 Introduction
- Pengenalan dasar bahasa C++.

### 📂 Compilers
- Penjelasan detail tentang compiler (seperti di atas).

### 📂 Basics of C++
Dasar-dasar yang harus dikuasai pertama kali.
- [Structure of a program](./basics/structure/) *(Struktur Program)*
- [Variables and types](./basics/variables/) *(Variabel dan Tipe Data)*
- [Constants](./basics/constants/) *(Konstanta)*
- [Operators](./basics/operators/) *(Operator)*
- [Basic Input/Output](./basics/io/) *(Input Output Dasar)*

### 📂 Control Structures
Struktur kontrol alur program.
- [Statements and flow control](./control/flow/) *(Percabangan & Perulangan)*
- [Arrays](./control/arrays/) *(Array)*
- [Pointers](./control/pointers/) *(Pointer)*
- [Dynamic memory](./control/dynamic_memory/) *(Memori Dinamis)*
- [Data structures](./control/structures/) *(Struktur Data)*

### 📂 Classes
Pemrograman Berorientasi Objek (OOP).
- [Classes (I)](./classes/introduction/) *(Pengenalan Kelas)*
- [Classes (II)](./classes/advanced/) *(Kelas Lanjut)*
- [Special members](./classes/special_members/) *(Member Khusus)*
- [Friendship and inheritance](./classes/inheritance/) *(Friendship & Pewarisan)*
- [Polymorphism](./classes/polymorphism/) *(Polimorfisme)*

### 📂 Other Features
Fitur-fitur lanjutan C++ lainnya.
- [Templates](./advanced/templates/) *(Template)*
- [Namespaces](./advanced/namespaces/) *(Namespace)*
- [Exceptions](./advanced/exceptions/) *(Exception Handling)*
- [Type casting](./advanced/casting/) *(Type Casting)*
- [Preprocessor directives](./advanced/preprocessor/) *(Preprocessor)*

### 📂 Standard Library
Pustaka standar C++.
- [Input/Output](./std_lib/io/) *(I/O Stream)*
- [Strings](./std_lib/strings/) *(String)*
- [Containers](./std_lib/containers/) *(Kontainer - Vector, List, dll)*
- [Algorithms](./std_lib/algorithms/) *(Algoritma)*

---

## 📝 Cara Kontribusi atau Penggunaan

1.  **Clone repository ini:**
    ```bash
    git clone https://github.com/username/repo-anda.git
    ```
2.  Masuk ke folder materi yang ingin dipelajari.
3.  Baca file `.cpp` dan cobalah untuk mengompilasi serta menjalankannya di komputer Anda.

**Happy Coding! 🚀**
```

### Tips Penambahan untuk GitHub:
Karena Anda berencana membagikan banyak source code, saya sarankan Anda membuat **folder** di repository Anda sesuai dengan struktur di atas.

Contoh struktur folder di repo Anda nanti:
```text
.
├── README.md
├── basics/
│   ├── structure/
│   │   └── hello_world.cpp
│   └── variables/
│       └── variables.cpp
├── control/
│   └── arrays/
│       └── arrays_example.cpp
└── classes/
    └── ...
```

Dengan cara ini, link di `README.md` (misalnya: `[Structure of a program](./basics/structure/)`) akan langsung mengarah ke folder tersebut.