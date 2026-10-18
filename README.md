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

Karena `insertFirst` menempatkan setiap elemen baru di posisi paling depan (`First`), maka urutan elemen dalam list menjadi: First → [9] → [12] → [8] → [0] → [2] → Nil

4. Output Soal No. 2 (Gamb5-2):
   
9 12 8 0 2

   



