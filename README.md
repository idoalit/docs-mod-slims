# Modifikasi SLiMS

Berikut merupakan panduan singkat memodifikasi [SLiMS][slims]. Panduan ini ditulis berdasarkan SLiMS versi 8 (Akasia). Pastikan anda memiliki dasar pemprograman minimum HTML.

```
DISCLAIMER.
-----------
Penulis tidak bertanggungjawab dengan efek samping yang mungkin muncul, seperti syntax error!
```

## Template

Di dalam [SLiMS][slims] terdapat 2 jenis template, yaitu template public dan template admin.

#### Template Public

Template public ini tampil pada halaman OPAC. Jika mengambil _source code_ dari [GitHub][github] terdapat beberapa template public yang bisa dipilih sesuai selera.
Untuk menganti template public ikuti langkah berikut:

- Login sebagai administrator
- Buka menu **System > Theme**
- Kemudian aktifkan salah satu template yang diinginkan

Kita dapat memodifikasi atau menambahkan template public baru dengan menulis sendiri kode sumbernya atau mendownload kode sumber dari hasil karya orang lain seperti yang ada di [GoSLiMS][goslims].

Beberapa _stuff_ yang bisa dicoba:

<details>
<summary>Mengganti logo pada template <b>Default</b></summary>

- Cari berkas **logo.png** pada folder _/template/default/img_
- Ganti berkas tersebut dengan logo yang anda inginkan, dengan nama file & _extension_ yang sama serta resolusi yang sama.
- Refresh browser untuk melihat perubahan, jika logo masih tidak berubah silahkan cek kembali dari langkah pertama serta hapus _cache browser_ anda.

</details>

<details>
<summary>Mengganti gambar background pada template <b>Default</b></summary>

- Sama seperti megganti logo, kali ini kita hanya perlu mereplace berkas yang sudah ada.
- Cari berkas **1.jpg, 2.jpg, 3.jpg dan 4.jpg** pada folder _/template/default/img_
- Ganti berkas tersebut dengan gambar yang anda inginkan, dengan nama file & _extension_ yang sama.
- Refresh browser untuk melihat perubahan, jika gambar background masih tidak berubah silahkan cek kembali dari langkah pertama serta hapus _cache browser_ anda.

</details>

<details>
<summary>Menambahkan template baru dari <b>GoSLiMS</b></summary>

- Sebagai contoh silahkan unduh salah satu template dari sini [Template OPAC - GoSLiMS](https://slims.web.id/goslims/?page_id=25&wpdmc=template-opac)
- Ekstrak berkas template yang telah diunduh tersebut.
- Cek apakah terdapat file **README.txt** atau **Cara install**, jika ada silahkan baca petunjuk installasinya.
- Jika tidak ada, pastikan terdapat file **index_template.inc.php** di dalam folder tersebut, dan letaknya bukan di dalam subfolder.
- Kemudian pindahkan folder tersebut ke dalam folder _/template/_.
- Aktifkan template yang baru diinstal lewat menu **System > Theme**

</details>

<details>
<summary>Menghapus & menambahkan item menu template Default</summary>

- Buka berkas _/template/default/partials/nav.php_
- Maka anda akan menemukan kode berikut:

```
...
<li><a href="index.php"><?php echo __('Home'); ?></a></li>
<li><a href="index.php?p=news"><?php echo __('Library News'); ?></a></li>
<li><a href="index.php?p=libinfo"><?php echo __('Library Information'); ?></a></li>
...
```

- Anda dapat menghapus, menyunting, atau menambahkan item menu tersebut.
- Contoh menambahkan item menu:

```
<li><a href="https://google.com"><?php echo __('Cari di google'); ?></a></li>
```

</details>

#### Template Admin

Untuk memodifikasi template admin dapat dilakukan dengan memodifikasi _source code_ yang terdapat pada folder _/admin/admin_template_

## Plugins

- goslims

## Module

- membership
  - kartu anggota

## Contents

- hardcode

[slims]: slims.web.id
[github]: github.com/slims/slims8_akasia
[goslims]: slims.web.id/goslims
