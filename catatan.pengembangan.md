# Catatan pengembangan:

## 21/03/2017
### HTML
#### Home page
##### Desain ulang template
- Menambah total kolom di home page menjadi 3 kolom (2 sidebar, 1 home post)
> Kolom pertama **Sidebar1**, kolom kedua **Home post**, kolom ketiga **Sidebar2**. Pengeturan kolom masih menggunakan **Grid system**, fitur andalan _Bootstrap_. lg-4 md-4 sm-6 xs-12.

	>> Sidebar1 memakai 4 grid, jika mode col-md atau col-lg maka letaknya di kolom pertama. Jika lebih kecil (col-sm dan col-xs), maka letaknya di bawah **Home post**.

	> Home post memakai 5 grid, posisi berubah sesuai penjelasan di atas. lg-5 md-5 sm-12 xs-12.

	> Sidebar2 memakai 3 grid, letaknya paling kanan/bawah. Posisi jika mode sm, maka akan berdampingan dengan **Sidebar1** berada di bawah **Home post**. lg-3 md-3 sm-6 xs-12.

- Home post, menggunakan element **List Group** bawaan Bootstrap.
- Sidebar widget menggunakan element **Panel** bawaan Bootstrap.
- Paging di ubah ke Pager, style menggunakan **Pager** bawaan Bootstrap.
## 22/03/2017
### HTML 
#### Detail page
##### Desain ulang template
- Ganti style post-detail menggunakan element _Panel_ bawaan *Bootstrap*.
> Menambahkan font-icon untuk social sharing.
> Ganti style post terkait, menggunakan list-group berupa judul artikel saja.
#### All page
- Fix style widget *Blogroll*, padding panel-body di persempit.
- Membuat style *Pager* untuk page aktif.
- Mengganti font icon dari _Glyphicon_ ke _MMBB-font icon_, jumlah icon tidak lebih dari 50, sudah tersedia social icon. Ukuran font jauh lebih ramping dari _Glyphicon_ karena hanya memasukkan icon yang dibutuhkan. Custom font di fontastic.me
> Begitu juga Bootstrap css, di custom dan dihilangkan element _glyphicon_, jumbotron dan well. Custom langsung di getbootstrap.com
- Mengganti JS bootstrap full, dengan hanya menggunakan collapse.js
## 24/03/2017
### XML
- Convert ke xml, home post, pager, sidebar, post-detail, share button.
## 25/03/2017
### HTML
- Ganti style pager, posisi tidak melebar tapi rata ke tengah. _Style *Pager* tanpa li.class next/prev._
- Fix style _status-msg,_ padding dirapatkan
- Fix style _home post_, padding di rapatkan.
- Fix style _popularpost_, padding _media_ top dan bottom di rapatkan dengan border.
- Ubah background-color body menjadi #f8f8f8, agar lebih nyaman di mata.
### XML
- Convert update-an html ke xml