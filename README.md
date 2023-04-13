# Prak_Python_UTS_Semester-2

Script tersebut merupakan program Python yang menggunakan library mysql.connector untuk menghubungkan dan memanipulasi database MySQL. Script tersebut mengakses database dengan nama 'db_sales_V3922006' di server localhost, menggunakan user 'root' tanpa password.

Kemudian di program ini ada beberapa fungsi, anatar lain :

Insert data: untuk menambahkan data baru ke tabel 'data_stok_barang'.

Show data: untuk menampilkan seluruh data yang ada di tabel 'data_stok_barang'.

Update data: untuk mengubah data yang sudah ada di tabel 'data_stok_barang'.

Hapus data: untuk menghapus data yang sudah ada di tabel 'data_stok_barang'.

Cari data: untuk mencari data berdasarkan Id_Barang di tabel 'data_stok_barang'.

Keluar: untuk keluar dari program.

Setelah itu di program selanjutnya ada bebrapa menu yaitu :
1.	Insert Data if menu == "1": Id_Barang = input("Masukkan id barang : ") Nama_Barang = input("Masukkan nama barang : ") Harga_Barang = int(input("Masukkan harga barang : ")) Stok_Awal = int(input("Masukkan stok awal : ")) Barang_Masuk = int(input("Masukkan barang masuk : ")) Barang_Keluar = int(input("Masukkan barang keluar : "))

          #Rumus untuk mencari stok_akhir
          stok_akhir = stok_awal + barang_masuk - barang_keluar
 
          #mencetak Stok_Akhir dari rumus sebelumnya
          print("stok akhir : ", stok_akhir)
 
          insert_data(id_barang, nama_barang, harga_barang, stok_awal, barang_masuk, barang_keluar, stok_akhir)

2.	Show Data elif menu == "2": show_data()
3.	Update Data (update data berdasarkan id_barang) elif menu == "3": id_barang = input("Masukkan id barang yang akan diupdate : ") nama_barang = input("Masukkan nama barang baru : ") harga_barang = int(input("Masukkan harga barang baru : ")) stok_awal = int(input("Masukkan stok awal baru : ")) barang_masuk = int(input("Masukkan barang masuk baru : ")) barang_keluar = int(input("Masukkan barang keluar baru : "))

          stok_akhir = stok_awal + barang_masuk - barang_keluar
          print("stok akhir setelah diupdate : ", stok_akhir)
 
          update_data(id_barang, nama_barang, harga_barang, stok_awal, barang_masuk, barang_keluar, stok_akhir)

4.	Hapus Data (hapus data berdasarkan id_barang) elif menu == "4": id_barang = input("Masukkan id barang yang ingin dihapus : ")

          delete_data(id_barang)

5.	Cari Data (mencari data berdasarkan id_barang) elif menu == "5": id_barang = input("Masukkan id barang yang ingin dicari : ")

          search_data(id_barang)

6.	Keluar elif menu == "6": print("Terima kasih sudah menggunakan Aplikasi i") break

Program menggunakan True while loop sehingga pengguna dapat memilih menu yang diinginkan hingga program selesai (menu 6).
Setelah pengguna memilih menu, program meminta input berdasarkan fungsi yang dipilih dan kemudian menjalankan fungsi yang diinginkan. 
Setiap fungsi menggunakan database MySQL yang terhubung ke program menggunakan pustaka mysql.connector dan menjalankan fungsi yang diinginkan.
Saat fungsi selesai, program akan melaporkan keberhasilan fungsi tersebut
