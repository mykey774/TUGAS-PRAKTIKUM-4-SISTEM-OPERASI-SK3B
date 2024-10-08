# TUGAS-PRAKTIKUM-4-SISTEM-OPERASI-SK3B

**NAMA : Miki Purnawan**

**NIM : 09011282328122**

**KELAS : SK3B**

**PROSES INPUT OUTPUT I/0**

1. Lihat daftar secara lengkap pada direktori aktif, belokkan tampilan standard output ke file baru 

![tugascl1](https://github.com/user-attachments/assets/22013706-ca4a-4da5-891c-c4d490016f80)

Untuk melakukan tugas di nomor 1, kita gunakan command ls -al untuk menampilkan secara lengkap direktori yang aktif kemudian agar output dari ls -al bisa dimasukkan ke dalam file bernama filebaru.txt kita gunakan command seperti ini : ls - al > filebaru.txt dan untuk mengecek apakah output dari ls -al tersimpan ke filebaru.txt kita cukup gunakan command cat filebaru.txt

2. Lihat daftar secara lengkap pada direktori /etc/paswd, belokkan tampilan standard output 
ke file baru tanpa menghapus file baru sebelumnya.

![tugascl2(1)](https://github.com/user-attachments/assets/ad2dec3a-5742-4806-a872-d3d30a026472)

![tugascl2](https://github.com/user-attachments/assets/7456ddd2-df15-44f5-b35c-1b4558530b61)

Dikarenakan passwd bukanlah sebuah direktori jadi kita gunakan command cat /etc/passwd kemudian enter untuk melihat isinya, bisa juga langsung simpan output nya ke filebaru.txt dengan menambahkan >> filebaru.txt setelah command cat (note : dikarenakan kita ingin menyimpan output passwd ke filebaru.txt tanpa menghapus isi file lama, maka kita harus menggunakan ">>" jangan ">" karena jika ">" maka isi file lama akan diganti dengan isi file yang baru)

3. Urutkan file baru dengan cara membelokkan standard input. 

![tugascl3](https://github.com/user-attachments/assets/a8e29811-a24d-4b8c-ad0c-1e52586da67c)

Setelah kita berhasil menyimpan output passwd ke filebaru.txt langkah selanjutnya adalah mengurutkan isi file nya sesuai abjad dengan membelokkan standar input, jika sebelumnya kita membelokkan standar output menggunakan >> sekarang kita gunakan << untuk membelokkan standar input, jadi command nya adalah sort < filebaru.txt lalu enter maka isi file dari flebaru.txt akan terurutkan.

4. Urutkan file baru dengan cara membelokkan standard input dan standard output ke file baru.urut.

![tugascl4](https://github.com/user-attachments/assets/748a3eec-cf65-42e2-96aa-2e0fcdee5f1d)

Di bagian ini, hasil dari pengurutan isi filebaru.txt berhasil dilakukan, kita lakukan penyimpanan dari output nya itu ke file yang bernama filebaru.urut menggunakan command sort < filebaru.txt > filebaru.urut, bisa juga pakai command sort filebaru.txt > filebaru.urut

5. Buatlah direktori latihan6 sebanyak 2 kali dan belokkan standard error ke file rmdirerror.txt.

![tugascl5](https://github.com/user-attachments/assets/addf0a10-05b8-4b0e-8445-7cd433a10f65)

Pertama-tama kita buat direktori bernama latihan6 dan berhasil, lalu kita buat lagi direktori dengan nama yang sama dan sudah pasti tidak berhasil karena nama yang digunakan itu sama, output dari error itu kita masukkan ke file yang bernama filedirerror.txt dengan cara mkdir latihan6 2> filedirerror.txt, "2>" itu adalah command untuk membelokkan standar output error ke sebuah file)

6. Urutkan kalimat berikut : 

Jakarta 

Bandung 

Surabaya 

Padang 

Palembang 

Lampung 

Dengan menggunakan notasi here document (<@@@ …@@@) 

![tugascl6](https://github.com/user-attachments/assets/30b8ef13-c573-400e-9f9f-88895bf9244c)

Untuk mengurutkan suatu inputan secara langsung, bukan dari file biasa, maka kita gunakan command sort <<@@@ kemudian enter dan ketik nama kota seperti Jakarta, Bandung dll setelah sudah selesai ketik @@@ maka inputan data yang kita ketik tadi akan terurut dan otomatis ditampilkan (command "<<@@@" ini adalah notasi yang berfungsi untuk menyelesaikan/menghentikan input ketika kita sudah selesai menginput data yang ingin diurutkan) 

7. Hitung jumlah baris, kata dan karakter dari file baru.urut dengan menggunakan filter dan tambahkan data tersebut ke file baru

![tugascl7](https://github.com/user-attachments/assets/de3ceb82-b354-41e9-9fac-519269e9c4b8)

untuk melakukan itu kita cukup gunakan command wc "nama file yang ingin dihitung jumlah barisnya" contohnya wc filebaru.urut lalu enter maka akan muncul output "74 308 4575 filebaru.urut" angka angka itu mewakilkan jumlah baris, kata dan karakter (74 = jumlah baris, 308 = jumlah kata, 4575 = jumlah karakter)

8. Gunakan perintah di bawah ini dan perhatikan hasilnya.

$ cat /etc/passwd | sort | pr –n | grep tty03 

$ find /etc –print | head 

$ head /etc/passwd | tail –5 | sort 

![tugascl8](https://github.com/user-attachments/assets/57de21eb-c4cc-411f-b567-fffe198b1013)

Saya akan jelaskan maksud dari command di setiap barisnya :

**A. cat /etc/passwd | sort | pr -n | grep tty03**

Penjelasan : pada baris kode ini berfungsi untuk mencari entri dalam file /etc/passwd yang berisi informasi terkait dengan "tty03", setelah isi file tersebut diurutkan dan diberi nomor baris. Namun, dikarenakan tidak ada entry di tty03 di dalam /etc/passwd maka tidak ada output yang muncul (cat /etc/passwd untuk menampilkan isi passwd, sort untuk mengurutkan nya, pr -n untuk memberi nomor pada setiap baris)

**B. find /etc –print | head** 

Penjelasan : pada baris kode ini berfungsi untuk mencari semua file dan direktori pada /etc kemudian di tampilkan, tapi karena saya menggunakan command head maka yang tampil hanya 10 baris pertama saja

**C. head /etc/passwd | tail –5 | sort**

Penjelasan : pada baris kode ini berfungsi untuk menampilkan 10 baris pertama dari isi passwd kemudian diambil 5 baris terakhir lalu di urutkan kemudian ditampilkan sebagai output 

9. Gunakan perintah $ who | cat | cat | sort | pr | head | cat | tail dan perhatikan hasilnya

![tugascl9](https://github.com/user-attachments/assets/d60eaab3-5166-4ed1-b656-787a886a5c5c)

Command ini berfungsi untuk mengurutkan daftar pengguna yang sedang login, lalu memformat tampilannya menjadi beberapa kolom dengan header halaman. Setelah itu, perintah hanya menampilkan 10 baris pertama, dan hasil akhirnya tidak berubah karena penggunaan cat | tail hanya meneruskan output dari head tanpa ada perubahan apa pun.

