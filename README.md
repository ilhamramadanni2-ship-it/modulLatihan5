# Modul 5: Singly Linked List (Bagian Kedua) - 5.2 Latihan

Implementasi ADT Singly Linked List dalam C++ untuk praktikum Struktur Data, Modul 5 (Singly Linked List Bagian Kedua) - Subbab 5.2 Latihan.

## Daftar File

| File | Deskripsi |
| :--- | :--- |
| `boolean.h` | Header definisi boolean (`boolean`, `true`, `false`) untuk komparabilitas standar modul praktikum. |
| `Singlylist.h` | Header file yang berisi pendefinisian tipe bentukan (`infotype`, `address`, `ElmList`, `List`) dan prototype seluruh fungsi/prosedur. |
| `Singlylist.cpp` | Implementasi dari seluruh fungsi dan prosedur ADT Singly Linked List. |
| `main.cpp` | Program utama (*driver*) untuk menjalankan dan menguji Soal No. 2, 3, dan 4. |

## Rincian Pengerjaan Soal 5.2 Latihan

### Soal No. 2: Pembentukan ADT Singly Linked List & Pengisian Data

1. **Definisi Tipe Data:**
   - `infotype` : bertipe `int`
   - `address` : pointer ke `ElmList` (`ElmList*`)
   - `ElmList` : record dengan field `info` (`infotype`) dan `next` (`address`)
   - `List` : record dengan field `First` (`address`)

2. **Primitif yang Dibuat:**
   - `void CreateList(List &L)` : Menginisialisasi list kosong (`L.First = Nil`).
   - `address alokasi(infotype x)` : Mengalokasikan memori untuk elemen baru dengan nilai `x`.
   - `void dealokasi(address &P)` : Membebaskan memori yang digunakan oleh elemen `P`.
   - `void insertFirst(List &L, address P)` : Menyisipkan elemen `P` di awal list.
   - `void printInfo(List L)` : Menampilkan seluruh nilai elemen dalam list.

3. **Pengisian Data:**
   Elemen dialokasikan dan dimasukkan berturut-turut dengan `insertFirst`:
   ```cpp
   P1 = alokasi(2);  insertFirst(L, P1);
   P2 = alokasi(0);  insertFirst(L, P2);
   P3 = alokasi(8);  insertFirst(L, P3);
   P4 = alokasi(12); insertFirst(L, P4);
   P5 = alokasi(9);  insertFirst(L, P5);

Karena `insertFirst` menempatkan setiap elemen baru di posisi paling depan (`First`), maka urutan elemen dalam list menjadi: First → [9] → [12] → [8] → [0] → [2] → Nil[cite: 15].

4. Output Soal No. 2 (Gambar 5-2)[cite: 15]:

```text
9 12 8 0 2
```[cite: 15]

### Soal No. 3: Pencarian Elemen dengan Info 8[cite: 15]

1. **Spesifikasi Fungsi:**[cite: 15]
   ```cpp
   address findElm(List L, infotype x);
   ```[cite: 15]

2. **Cara Kerja:**[cite: 15]
   * Menelusuri list mulai dari `L.First`.[cite: 15]
   * Memeriksa apakah nilai `P->info == x`.[cite: 15]
   * Jika ditemukan, mengembalikan alamat/pointer `P`.[cite: 15]
   * Jika penelusuran sampai akhir list (`Nil`) tidak menemukan nilai yang cocok, mengembalikan `Nil`.[cite: 15]

3. **Pemanggilan & Output Soal No. 3 (Gambar 5-3):**[cite: 15]
   ```cpp
   address P_cari = findElm(L, 8);
   if (P_cari != Nil) {
       cout << P_cari->info << " ditemukan dalam list" << endl;
   }
   ```[cite: 15]

**Output:**[cite: 15]
```text
8 ditemukan dalam list
```[cite: 15]

### Soal No. 4: Menghitung Jumlah Total Info Seluruh Elemen[cite: 16]

1. **Spesifikasi Fungsi:**[cite: 16]
   ```cpp
   int totalInfo(List L);
   ```[cite: 16]

2. **Cara Kerja:**[cite: 16]
   * Menelusuri list mulai dari elemen pertama hingga elemen terakhir.[cite: 16]
   * Menjumlahkan nilai `info` setiap simpul: `9 + 12 + 8 + 0 + 2 = 31`.[cite: 16]
   * Mengembalikan nilai total akumulasi.[cite: 16]

3. **Pemanggilan & Output Soal No. 4 (Gambar 5-4):**[cite: 16]
   ```cpp
   int total = totalInfo(L);
   cout << "Total info dari kelima elemen adalah " << total << endl;
   ```[cite: 16]

**Output:**[cite: 16]
```text
Total info dari kelima elemen adalah 31
```[cite: 16]

## Cara Kompilasi dan Menjalankan[cite: 17]

### Melalui Terminal / Command Line (g++)[cite: 17]

```bash
cd cpp/pertemuan5
g++ main.cpp Singlylist.cpp -o main.exe
./main.exe
```[cite: 17]

### Melalui Code::Blocks IDE[cite: 17]

1. Buka Code::Blocks.[cite: 17]
2. Buat project baru: **File > New > Project > Console Application > C++**.[cite: 17]
3. Tambahkan file `Singlylist.h`, `Singlylist.cpp`, dan `main.cpp` ke dalam project (centang target Debug dan Release).[cite: 17]
4. Tekan **F9** (*Build and Run*).[cite: 17]

## Hasil Eksekusi Program Lengkap[cite: 17]

```text
9 12 8 0 2
8 ditemukan dalam list
Total info dari kelima elemen adalah 31
```[cite: 17]




