[Android Room with a View - Kotlin codelab](https://developer.android.com/codelabs/android-room-with-a-view-kotlin)

#Rangkuman materi

dalam pembelajaran Android Room dengan View ini ada beberapa poin tahapan yaitu :

1. Membuat aplikasi
2. Memperbarui gradle module dan gradle project / setup project
3. Membuat Entity
4. Membuat DAO (Database Access Object)
5. Mengamati perubahan database
6. Menambahkan database ROOM
7. Membuat repositori
8. Membuat view model
9. Menambahkan tataletak XML
10. Menambahkan Recycler View
11. Membuat Instance repositori dan database
12. Mengisi database
13. Menambahkan NewWordActivity
14. Terhubung dengan data

dalam pembelajaran ini ada beberapa komponen activity yang dipelajari yaitu :

MainActivity: menampilkan kata dalam daftar menggunakan RecyclerView dan WordListAdapter. Di MainActivity, terdapat Observer yang mengamati kata dari database dan menerima notifikasi jika ada perubahan.
NewWordActivity: menambahkan kata baru ke dalam daftar.
WordViewModel: menyediakan metode untuk mengakses lapisan data, dan menghasilkan LiveData sehingga MainActivity dapat menyiapkan hubungan pengamat.*
LiveData<List<Word>>: Memungkinkan update otomatis di komponen UI. Anda dapat melakukan konversi dari Flow ke LiveData dengan memanggil flow.toLiveData().
Repository: mengelola satu atau beberapa sumber data. Repository mengekspos metode untuk ViewModel guna berinteraksi dengan penyedia data yang mendasarinya. Di aplikasi ini, backend tersebut adalah database Room.
Room: adalah wrapper di sekitar dan mengimplementasikan database SQLite. Room melakukan banyak tugas untuk Anda yang sebelumnya harus Anda lakukan sendiri.
DAO: memetakan panggilan metode ke kueri database, sehingga saat Repositori memanggil metode seperti getAlphabetizedWords(), Room dapat mengeksekusi SELECT * FROM word_table ORDER BY word ASC**.**
DAO dapat mengekspos kueri suspend untuk satu permintaan singkat dan kueri Flow saat Anda ingin mendapatkan notifikasi tentang perubahan dalam database.
Word: adalah class entity yang berisi satu kata.
Views dan Activities (serta Fragments) hanya berinteraksi dengan data melalui ViewModel. Dengan demikian, tidak masalah dari mana data berasal.
