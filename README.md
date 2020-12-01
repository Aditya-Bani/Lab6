_________________________________________________________________________________

# LAB 6

![Latihan 1](https://github.com/HamdanAlWahidan/TUGAS_PERTEMUAN_10-LAB-6/blob/main/Pertemuan%2010%20LAB%206%20-%20SS/00.png) <br>



Pada tugas LAB 6, saya diminta untuk membuat sebuah program menambahkan data ke sebuah list dengan sistem library root yang nantinya akan seperti ini.

## Langkah - Langkah

* Disini saya membuat file library root nya terlebih dahulu dengan nama folder yaitu data:

![Latihan 1.1](https://github.com/HamdanAlWahidan/TUGAS_PERTEMUAN_10-LAB-6/blob/main/Pertemuan%2010%20LAB%206%20-%20SS/0.png) <br>

![Latihan 1.2](https://github.com/HamdanAlWahidan/TUGAS_PERTEMUAN_10-LAB-6/blob/main/Pertemuan%2010%20LAB%206%20-%20SS/1.png) <br>

* Setelah itu buat lah file python nya dengan nama (lab6.py) tapi itu terserah kalian mau menggunakan nama apa

![Latihan 1.3](https://github.com/HamdanAlWahidan/TUGAS_PERTEMUAN_10-LAB-6/blob/main/Pertemuan%2010%20LAB%206%20-%20SS/3.png) <br>

Lalu mari kita mengcoding file tersebut dengan syntax seperti di bawah ini

```
data = []
data = {}

def tambah():
        print("=======Tambah Data=======")
        nama    =input("Nama                :  ")
        nim     =input("Nim                 :  ")
        tugas   =int(input("Masukan Nilai Tugas :  "))
        uts     =int(input("Masukan Nilai UTS   :  "))
        uas     =int(input("Masukan Nilai UAS   :  "))
        akhir   = (0.30 * tugas) + (0.35 * uts) + (0.35 * uas)
        data[nama] = nim ,tugas, uts, uas, akhir

def lihat():
    if data.items():
        print("=======Daftar Nilai Mahasiswa=======")
        print("================================================================================================")
        print(" |NO   |     NAMA      |    NIM    |     TUGAS    |     UTS     |       UAS    |    AKHIR     | ")
        print("================================================================================================")
        i=0
        for x in data.items():
            i+=1
            print(" | {6:2}  |  {0:12s} | {1:9s} | {2:11}  | {3:11} | {4:11}  |  {5:11} |".format(x[0], x[1][0], x[1][1], x[1][2], x[1][3], x[1][4], i))
            print("============================================================================================")
    else:
        print("=======Daftar Nilai Mahasiswa======")
        print("================================================================================================")
        print(" |NO   |     NAMA      |    NIM    |     TUGAS    |     UTS     |       UAS    |    AKHIR     | ")
        print("================================================================================================")
        print("|                                      TIDAK ADA DATA                                         |")
        print("===============================================================================================")

def ubah():
        print('=======Ubah Data Mahasiswa=======')
        nama = input('Nama                :  ')
        if nama in data.keys():
            nim     =input('Nim                 :  ')
            tugas   =int(input("Masukan Nilai Tugas :  "))
            uts     =int(input("Masukan Nilai UTS   :  "))
            uas     =int(input("Masukan Nilai UAS   :  "))
            akhir   =(0.30 * tugas) + (0.35 * uts) + (0.35 * uas)
            data[nama] = nim, tugas, uts, uas, akhir
        else:
            print("Data Nilai Tidak Ada".format(nama))

def hapus():
        print("=======Hapus Data Mahasiswa=======")
        nama=input("Nama :  ")
        if nama in data.keys():
            del data[nama]
        else:
            print("Data Nilai Tidak Ada".format(nama))

```
Jika sudah memasukan semua syntax diatas jangan di run terlebih dahulu nanti file tersebut akan rusak/tidak dapat dijalankan nanti hasilnya akan error.

* Selanjutnya kita bikin file pythonnya tetapi di luar folder data untuk menjalankan file yang barusan di coding oleh kita. File yang kita akan bikin berilah nama (main.py) karna itu akan menjadi file yang akan menjalankan file library root yang telah kita bikin sebelumnya.

![Foto Lat1](https://github.com/HamdanAlWahidan/TUGAS_PERTEMUAN_10-LAB-6/blob/main/Pertemuan%2010%20LAB%206%20-%20SS/4.png) <br>

* Jika sudah mari kita coding lagi file ini mari kita skuylah. Seperti biasa mengikuti syntax nya oke.

```
from data import lab6

print("PROGRAM MENAMPILKAN DAFATR NILAI MAHASISWA")
while True:
    print("")
    c =input("(L)lihat, (T)ambah, (U)bah, (H)apus, (K)eluar : ")
    if c.lower() == 't':
        lab6.tambah()

    elif c.lower() == 'u':
        lab6.ubah()

    elif c.lower() == 'l':
        lab6.lihat()

    elif c.lower() == 'h':
        lab6.hapus()

    elif c.lower() == 'k':
        print("Keluar")
        break

```

Nah disini di awal terdapat syntax ini:
```
from data import lab6
```
Fungsi nya ini untuk menjalankan file library root nya yaitu dari folder bernama (data) untuk membuka file (lab6.py). Itu penjelasan singkatnya, kalau sudah langsung run aja tapi sebelum di run save dulu nanti kalau hilang nangis :v udah langsung skuy ajalah. Nanti akan jadi seperti di bawah ini.

![Foto Lat1](https://github.com/HamdanAlWahidan/TUGAS_PERTEMUAN_10-LAB-6/blob/main/Pertemuan%2010%20LAB%206%20-%20SS/9.png) <br>

Cukup sekian tugas dari saya jika ada kesalahan saya mohon maaf yang sebesar besar.

# TERIMA KASIH
___________________________________________________________________________________________________
