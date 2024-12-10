NAMA : Afnan Dika Ramadhan

NIM : 312410518

KELAS : TI24.A5

# LAB08 OOP

**1.CLASS `MAHASISWA`**

Class ini merepresentasikan setiap mahasiswa dengan atribut nama dan nilai

```python
class Mahasiswa:
    def __init__(self, nama, nilai):
        self.nama = nama  # Nama mahasiswa
        self.nilai = nilai  # Nilai mahasiswa
```
`__init__`: Constructor untuk inisialisasi objek mahasiswa. Setiap mahasiswa memiliki nama dan nilai.

**2. Class `DaftarNilaiMahasiswa`**

Class ini digunakan untuk mengelola daftar mahasiswa. Class ini berisi beberapa method untuk operasi pada daftar mahasiswa.

**Atribute**
```python
self.mahasiswa_list = []

```
`mahasiswa_list`: List untuk menyimpan objek mahasiswa.

**Method**

1.tambah_mahasiswa(nama, nilai)
Digunakan untuk menambahkan objek Mahasiswa ke dalam mahasiswa_list.
```python
def tambah_mahasiswa(self, nama, nilai):
    mahasiswa = Mahasiswa(nama, nilai)  # Membuat objek Mahasiswa
    self.mahasiswa_list.append(mahasiswa)  # Menambahkannya ke list

```
2.tampilkan_daftar()
Menampilkan semua data mahasiswa dalam mahasiswa_list.
Jika list kosong, pesan akan muncul bahwa daftar kosong.
```python
def tampilkan_daftar(self):
    if not self.mahasiswa_list:
        print("Daftar mahasiswa kosong.")
        return

    for idx, mahasiswa in enumerate(self.mahasiswa_list, start=1):
        print(f"{idx}. {mahasiswa.nama} - Nilai: {mahasiswa.nilai}")

```
3.hapus_mahasiswa(nama)
Menghapus mahasiswa berdasarkan nama.
Jika ditemukan, mahasiswa akan dihapus dari mahasiswa_list. Jika tidak ditemukan, akan muncul pesan error.
```python
def hapus_mahasiswa(self, nama):
    for mahasiswa in self.mahasiswa_list:
        if mahasiswa.nama == nama:
            self.mahasiswa_list.remove(mahasiswa)
            print(f"Mahasiswa dengan nama '{nama}' berhasil dihapus.")
            return
    print(f"Mahasiswa dengan nama '{nama}' tidak ditemukan.")

```
4.ubah_nilai(nama, nilai_baru)
Mengubah nilai mahasiswa berdasarkan nama.
Jika ditemukan, nilai akan diperbarui. Jika tidak, muncul pesan error.
```python
def ubah_nilai(self, nama, nilai_baru):
    for mahasiswa in self.mahasiswa_list:
        if mahasiswa.nama == nama:
            mahasiswa.nilai = nilai_baru
            print(f"Nilai mahasiswa '{nama}' berhasil diubah menjadi {nilai_baru}.")
            return
    print(f"Mahasiswa dengan nama '{nama}' tidak ditemukan.")

```
**3.Program Utama**

Bagian ini menyediakan antarmuka interaktif untuk pengguna menggunakan class DaftarNilaiMahasiswa.

1Inisialisasi Objek
```python
daftar_nilai = DaftarNilaiMahasiswa()

```
Membuat objek daftar_nilai dari class DaftarNilaiMahasiswa.

2.Menu Interaktif Menu berisi 5 opsi:

-Tambah mahasiswa

-Tampilkan daftar mahasiswa

-Hapus mahasiswa

-Ubah nilai mahasiswa

-Keluar.

```python
while True:
    print("\nMenu:")
    print("1. Tambah Mahasiswa")
    print("2. Tampilkan Daftar Mahasiswa")
    print("3. Hapus Mahasiswa")
    print("4. Ubah Nilai Mahasiswa")
    print("5. Keluar")
    ...

```
3.Pilihan Menu Berdasarkan input pengguna, program akan menjalankan method tertentu pada objek daftar_nilai.

**Tambah Mahasiswa:** Mengambil nama dan nilai, memanggil tambah_mahasiswa.
```python
nama = input("Masukkan nama mahasiswa: ")
nilai = float(input("Masukkan nilai mahasiswa: "))
daftar_nilai.tambah_mahasiswa(nama, nilai)

```
**Tampilkan Daftar Mahasiswa:** Memanggil tampilkan_daftar.
```python
daftar_nilai.tampilkan_daftar()

```
**Hapus Mahasiswa:** Mengambil nama dan memanggil hapus_mahasiswa.
```python
nama = input("Masukkan nama mahasiswa yang akan dihapus: ")
daftar_nilai.hapus_mahasiswa(nama)

```
**Ubah Nilai Mahasiswa:** Mengambil nama dan nilai baru, memanggil ubah_nilai.
```python
nama = input("Masukkan nama mahasiswa yang nilainya akan diubah: ")
nilai_baru = float(input("Masukkan nilai baru: "))
daftar_nilai.ubah_nilai(nama, nilai_baru)

```
**Keluar:** Menghentikan program.
```python
print("Program selesai. Terima kasih!")
break

```
**4.Cara Kerja Program**

Program terus berjalan hingga pengguna memilih opsi keluar (5).

Setiap input pengguna dievaluasi dan operasi yang sesuai dilakukan pada daftar_nilai.


# Flowchart
![](https://github.com/nanafnan09/labpy08/blob/ef9ddf902858e01db9cd96424c9f496a51b8e381/flowchart%20labpy08.png)

# Hasil
![](https://github.com/nanafnan09/labpy08/blob/f99571fb941ddec0080b7265246ddc0084ece6cc/OPSI%20TAMBAH%20DATA%20LAB%20PY08.png)

![](https://github.com/nanafnan09/labpy08/blob/465c87c369d1b7ce5168803edef13f67af855e14/opsi%20hapus%20data%20labpy08.png)

![](https://github.com/nanafnan09/labpy08/blob/10b960106e6e622f1f23b743face049e6aac1817/opsi%20ubah%20data%20labpy08.png)

![](https://github.com/nanafnan09/labpy08/blob/6153f9d742fee0fe9cbe32b857e83ed7f69c0137/Keluar%20data%20labpy08.png)

# DIAGRAM
![]()
