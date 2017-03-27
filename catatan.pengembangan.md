# Catatan pengembangan:

## 21/03/2017
### HTML
#### Home page
##### Desain ulang template
- Menambah total kolom di home page menjadi 3 kolom (2 sidebar, 1 home post)
> Kolom pertama **Sidebar1**, kolom kedua **Home post**, kolom ketiga **Sidebar2**. Pengeturan kolom masih menggunakan **Grid system**, fitur andalan _Bootstrap_. `lg-4 md-4 sm-6 xs-12`.

	>> Sidebar1 memakai 4 grid, jika mode col-md atau col-lg maka letaknya di kolom pertama. Jika lebih kecil (`col-sm dan col-xs`), maka letaknya di bawah **Home post**.

	> Home post memakai 5 grid, posisi berubah sesuai penjelasan di atas. `lg-5 md-5 sm-12 xs-12`.

	> Sidebar2 memakai 3 grid, letaknya paling kanan/bawah. Posisi jika mode sm, maka akan berdampingan dengan **Sidebar1** berada di bawah **Home post**. `lg-3 md-3 sm-6 xs-12`.

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
- Fix style widget **Blogroll**, padding panel-body di persempit.
- Membuat style *Pager* untuk page aktif.
- Mengganti font icon dari _Glyphicon_ ke _MMBB-font icon_, jumlah icon tidak lebih dari 50, sudah tersedia social icon. Ukuran font jauh lebih ramping dari _Glyphicon_ karena hanya memasukkan icon yang dibutuhkan. Custom font di fontastic.me.
> Begitu juga Bootstrap css, di custom dan dihilangkan element _glyphicon_, jumbotron dan well. Custom langsung di getbootstrap.com.
- Mengganti JS bootstrap full, dengan hanya menggunakan collapse.js.
## 24/03/2017
### XML
- Convert ke xml, home post, pager, sidebar, post-detail, share button.
## 25/03/2017
### HTML
- Ganti style pager, posisi tidak melebar tapi rata ke tengah. _Style **Pager** tanpa `li.class next/prev`._
- Fix style _status-msg,_ padding dirapatkan.
- Fix style _home post_, padding di rapatkan.
- Fix style _popularpost_, padding _media_ top dan bottom di rapatkan dengan border.
- Ubah background-color body menjadi #f8f8f8, agar lebih nyaman di mata.
- Fix style _popularpost_, padding _media_ dikembalikan ke semula, yg dirapatkan 
itu _media-body_ > p.
- Fix jarak _status-msg_ dgn pager, jika ada di halaman _error page not found_.
### XML
- Convert update-an html ke xml.
## 26/03/2017
### HTML
- Fix _pager_.
> style di kembalikan ke class next/previous , yaitu melebar penuh halaman.
> mengganti teks ke icon.
> memberi jarak dengan disqus comment form.
### XML
- Convert update-an html ke xml.
- Remove _post related_.
- Menerapkan _Disqus_ comment plugin.
- Fix posisi form _Disqus_ dengan _Pager_ dan _widget_ .
- Remove CSS dan JS bawaan Blogger.
> Karena menggunakan _Disqus_ comment plugin, jadi di remove lah CSS dan JS itu.
> Berdampak akan tidak bisa menggunakan _widget_ yang membutuhkan _CSS dan JS Blogger_.
> seperti Archive dan lainnya.
- Fix _pager_ yang tampil double di _static page_.
## 27/03/2017
### ALL
- Ubah default *image thumb* jika gambar kosong untuk *popular post* dan *home post* menggunakan holder.js.
- Fix posisi _popular post_ juga kode di **xml**.
- Menambahkan default `text-align:justify` /`.text-justify` *untuk post-detail*.
- Menambahkan image thumb jika gambar *widget profile saya/about me* kosong.
- Menambahkan 1 label ke *breadcrumb*, total ada 2 label aktif di *breadcrumb*. Urutannya: **Home** / **label pertama** / **label kedua** / **Judul postingan**.
- Merubah `font-size` *popular post*, jika di akses oleh **tablet** atau **desktop** maka `font-size` menjadi `90%`, jika **mobile** maka `100%`. 
## 28/03/2017
### HTML
- Ubah style dan posisi *footer*, menggunakan *grid system* dan menambahkan icon ke sebelah kanan *footer* `text-align:right` /`.pull-right`.
- Menambahkan icon *blogger* ke setiap footer `.panel` selain *post-detail* menggunakan javascript `mmbb.js`. Jika ada *.panel- footer*, maka akan di replace oleh icon *blogger* tersebut.
- Memindahkan kode untuk gambar thumb kosong (popular post, home post, profile), dari *blogger* ke `mmbb.js`.
- Memindahkan kode untuk add style disable di *pager* ke `mmbb.js`.
- Merubah `font-size` dan `padding` category, jika di akses melalui **desktop** atau **tablet** maka default `.btn-xs`, jika **mobile** maka `font-size:100%` dan padding disesuaikan.
- Memindahkan kode untuk active *label* di **widget category**, ke `mmbb.js`.
- Menambahkan style active page untuk **Header Menu**, kode berada di `mmbb.js`.
- Menambahkan style active page untuk **Popular Post**, kode berada di `mmbb.js`.
- Fix style *breadcrumb* untuk tampilan di **mobile**, jarak elemen `li` terakhir terlalu jauh dari kiri, karena menggunakan `padding-left`. Mengurangi `line-height` menjadi `1.3em` khusus tampilan di **mobile**.