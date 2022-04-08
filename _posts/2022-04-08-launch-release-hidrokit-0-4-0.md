---
title: Rilis hidrokit 0.4.0
date: 2022-04-08 10:00 AM
categories: [Pengumuman]
tags: [hidrokit, dokumentasi]
author:
  name: Taruma Sakti Megariansyah
  link: https://taruma.github.io
pin: true
image:
  src: https://hidrokit.github.io/hidrokit/assets/images/presskit/hidrokit-800x200-transparent.png
  width: 800
  height: 200
---

Selamat datang di artikel rilis hidrokit 0.4.0! 🎉 Perkenalkan nama saya Taruma, di artikel ini saya ingin membahas rilisnya hidrokit versi 0.4.0 dan berbagai fitur baru yang telah tersedia.

# Pendahuluan Versi 0.4.0

Bagi yang baru mendengar atau mengenal kata "hidrokit", hidrokit bermula sebagai proyek _open source_ paket _python_ yang dapat digunakan untuk membantu proses analisis hidrologi dimulai dari pengolahan data, analisis data, dan visualisasi data. hidrokit bangkit pada tahun 2019 karena kebutuhan pribadi dalam bereksperimen dengan _data science_ terutama pada topik [_deep learning_ pada kasus _rainfall-runoff_](https://taruma.github.io/vivaldi/). Seiringnya waktu, saya mengalihkan hidrokit yang semula hanya proyek tunggal, menjadi wadah kolaborasi dengan berbagai proyek. Proyek yang saat ini aktif antara lain situs [hidrokit], situs [hidrokit-notebook], dan situs [hidrokit-blog], dimana proyek-proyek tersebut saling berhubungan. Untuk lihat proyek lainnya bisa lihat di [hidrokit.github.io](http://hidrokit.github.io/).

Pada [tulisan sebelumnya](https://medium.com/@taruma/hidrokit-pada-tahun-2020-c00cd8860c0e) di tahun 2020 (hidrokit versi 0.3.5), saya menulis telah mengakhiri pengembangan hidrokit, hal tersebut dikarenakan kesibukan lain yang harus diprioritaskan ataupun motivasi yang sudah meredup. Akan tetapi, pada tahun 2022, hidrokit kembali saya bangkitkan dari masa hiatusnya. Dan hal ini berkat dukungan dari [PT. FIAKO Enjiniring Indonesia](http://www.fiako.co.id/) (FIAKO Engineering) yang percaya bahwa pengembangan hidrokit memiliki potensi untuk merubah atau meningkatkan alir kerja sekarang (yang tentunya tidak terbatas di bidang sumber daya air saja). Dengan kerjasama antara hidrokit dan FIAKO Engineering, saya harap dapat menghasilkan suatu inovasi dan kolaborasi sebagai produk yang dibutuhkan bagi para praktisi ataupun akademisi.  

Dengan hubungan kerjasama tersebut, tentunya hidrokit harus mempersiapkan agenda yang ingin dicapai tahun ini dan pada versi lanjutan berikutnya. Dan dengan tulisan ini, saya harap bisa memberi gambaran apa yang saya rencanakan untuk pengembangan hidrokit selanjutnya. 

# Fitur dan Perubahan Versi 0.4.0

Saat ini, hidrokit versi 0.4.0 sudah dirilis melalui [github](https://github.com/hidrokit/hidrokit/releases/tag/0.4.0) ataupun [pypi](https://pypi.org/project/hidrokit/). Untuk panduan instalasi bisa lihat di [halaman instalasi di hidrokit/hidrokit](https://hidrokit.github.io/hidrokit/panduan/instalasi).

## Pembaruan Logo

![hidrokit-hidrokit-logo](https://hidrokit.github.io/hidrokit/assets/images/presskit/hidrokit-800x200-transparent.png){: w="50%"}
_proyek hidrokit/hidrokit_

Meski ini bukan bagian dari perubahan software, tapi alangkah baiknya untuk menyebut perubahan "tampilan" yang menjadi halaman depannya proyek ini. Logo hidrokit dan variasinya dikembangkan dan dibuat oleh [@firmansennie](https://www.instagram.com/firmansenie/). Berikut variasi lainnya (notebook dan blog).

![hidrokit-notebook-1](https://hidrokit.github.io/notebook/assets/images/hidrokit-nb-800x200.png){: w="50%"}
_proyek hidrokit/notebook_

![hidrokit-blog-1](https://hidrokit.github.io/blog/assets/hidrokit-blog-800x200.png){: w="50%"}
_proyek hidrokit/blog_

## Perubahan Penomoran Versi

Sejak versi 0.4.0, pemberian nomor versi sedikit diubah yang sebelumnya hanya mengubah _patch version_ saat ditambahnya modul/fitur baru di subpaket `.contrib`, menjadi _minor version_ jika tersedia modul/fitur baru. Hal ini terkait bugfix yang mungkin terjadi di versi 0.4.x, sehingga untuk _patch version_ dikhususkan untuk perubahan tersebut. Dengan perubahan ini diharapkan sudah mengikuti pedoman [_semantic versioning 2.0.0_](https://semver.org/)

## Fitur Baru

Pada versi 0.4.0, hidrokit memfokuskan diri pada bagian awal dari setiap analisis hidrologi, yaitu analisis frekuensi dan uji kecocokan distribusi. Bagian tersebut merupakan bagian rutin dari pekerjaan hidrologi. Saat pengembangan juga, saya menemukan beberapa alternatif cara perhitungannya (untuk distribusi log pearson III dan gumbel). Selain itu, saya mengajukan untuk menggunakan beberapa konstanta/nilai yang dibangkitkan langsung menggunakan python (paket [scipy](https://scipy.org/)) dibandingkan dengan cara penggunaan tabel (kecuali untuk distribusi gumbel). Tapi, jika ingin menggunakan tabel, hanya perlu menyatakan di argumen `source` sumber tabel mana yang akan digunakan. Untuk lebih lanjutnya, bisa mengunjungi masing-masing manualnya. Seluruh notebook (gist) bisa dilihat juga melalui halaman [kumpulan notebook](https://hidrokit.github.io/notebook/kumpulan-notebook).

Isu | modul | keterangan | manual
:- | :- | :- | :-
[\#102](https://github.com/hidrokit/hidrokit/issues/102) | `.hk102` | upsampling dataset | [Gist](https://gist.github.com/taruma/96c321175ecac3e51350ef4c94f3d7d4)
[\#151](https://github.com/hidrokit/hidrokit/issues/151) | `.hk151` | uji outlier | [Gist](https://gist.github.com/taruma/7bf2e4e1601ab8390d9919043eb87682)
[\#158](https://github.com/hidrokit/hidrokit/issues/158) | `.hk158` | perhitungan parameter statistik | [Gist](https://gist.github.com/taruma/6a0b0f9dd26359f6832fe12bab30fdc7)
[\#140](https://github.com/hidrokit/hidrokit/issues/140) | `.hk140` | uji kolmogorov-smirnov | [Gist](https://gist.github.com/taruma/5d16baf90016d8a08c6870b674226691)
[\#141](https://github.com/hidrokit/hidrokit/issues/141) | `.hk141` | uji chi-square | [Gist](https://gist.github.com/taruma/e250ab2685ba5b4c8facbf498cfb5cd8)
[\#124](https://github.com/hidrokit/hidrokit/issues/124), [\#179](https://github.com/hidrokit/hidrokit/issues/179) | `.hk124` | distribusi log normal 2 parameter | [Gist](https://gist.github.com/taruma/5d3ab88893e56f895dc3f36ea19c3e60)
[\#126](https://github.com/hidrokit/hidrokit/issues/126), [\#179](https://github.com/hidrokit/hidrokit/issues/179) | `.hk126` | distribusi log pearson tipe III | [Gist](https://gist.github.com/taruma/60725ffca91dc6e741daee9a738a978b)
[\#127](https://github.com/hidrokit/hidrokit/issues/127), [\#179](https://github.com/hidrokit/hidrokit/issues/179) | `.hk127` | distribusi gumbel | [Gist](https://gist.github.com/taruma/ffa77e6f50a19fa5d05ab10e27d3266a)
[\#172](https://github.com/hidrokit/hidrokit/issues/172), [\#179](https://github.com/hidrokit/hidrokit/issues/179) | `.hk172` | distribusi normal | [Gist](https://gist.github.com/taruma/91b9fcd8fb92c12f4ea2639320ead116)

Karena penamaan modul mengikuti nomor isu yang diselesaikan dan untuk mengingat nomor tersebut cukup sulit (termasuk saya sendiri), oleh karena itu perlu juga modul perantara untuk penggunaan fitur baru 0.4.0. Berikut modul tersebut:

modul | keterangan
:- | :-
`.anfrek` | kumpulan modul analisis frekuensi (hk124, hk126, hk127, hk172)
`.ujidist` | kumpulan modul uji distribusi (hk140, hk141)

Seluruh fitur baru di 0.4.0 (kecuali `.hk102`), telah saya peragakan juga di [Laporan Implementasi 5: Analisis Frekuensi dan Uji Kecocokan Distribusi](https://hidrokit.github.io/notebook/kumpulan-notebook#laporan-implementasi).

## Perbaikan

Berikut daftar perbaikan (bugfix) di versi 0.4.0:

isu | modul/fungsi | keterangan | manual
:- | :- | :- | :-
[\#169](https://github.com/hidrokit/hidrokit/issues/169) | `test_prep_excel.test__dataframe_table()` | perbaikan fungsi test | -

## Pembaruan / Perubahan

Berikut daftar pembaruan di versi 0.4.0:

isu | modul/fungsi | keterangan | manual
:- | :- | :- | :-
[\#162](https://github.com/hidrokit/hidrokit/issues/162) | `.contrib.taruma.hk88.read_workbook()` | luaran `as_df=False` berubah dari `list` menjadi `dictionary` | [Gist](https://gist.github.com/taruma/6d48b3ec9d601019c15fb5833ae03730)
[\#162](https://github.com/hidrokit/hidrokit/issues/162) | `.contrib.taruma.hk88.read_workbook()` | pembaruan fungsi untuk membaca seluruh sheet tanpa memasukkan nama stasiun/sheet | [Gist](https://gist.github.com/taruma/6d48b3ec9d601019c15fb5833ae03730) 
[\#115](https://github.com/hidrokit/hidrokit/issues/115) | `.contrib.taruma.hk98.summary_all()` | penambahan argumen `verbose=False` | [Gist](https://gist.github.com/taruma/aca7f90c8fbb0034587809883d0d9e92) 


## Daftar Perubahan 0.3.6 ➡️ 0.4.0

Berikut daftar perubahan detail dari versi 0.3.6 ➡️ 0.4.0 (termasuk nomor _pull request_):

* Fix [\#114](https://github.com/hidrokit/hidrokit/issues/114) Penambahan modul hk102 by [@taruma](https://github.com/taruma) in [\#171](https://github.com/hidrokit/hidrokit/pull/171)
* Fitur [\#151](https://github.com/hidrokit/hidrokit/issues/151) (Uji Outlier) by [@taruma](https://github.com/taruma) in [\#168](https://github.com/hidrokit/hidrokit/pull/168)
* Fitur [\#158](https://github.com/hidrokit/hidrokit/issues/158) (Parameter Statistik) by [@taruma](https://github.com/taruma) in [\#167](https://github.com/hidrokit/hidrokit/pull/167)
* Fitur [\#126](https://github.com/hidrokit/hidrokit/issues/126) Log Pearson 3 by [@taruma](https://github.com/taruma) in [\#170](https://github.com/hidrokit/hidrokit/pull/170)
* Bugfix [\#115](https://github.com/hidrokit/hidrokit/issues/115) verbose mode hk98 by [@taruma](https://github.com/taruma) in [\#173](https://github.com/hidrokit/hidrokit/pull/173)
* Bugfix [\#169](https://github.com/hidrokit/hidrokit/issues/169) Fix assertion frame `test__dataframe_table` by [@taruma](https://github.com/taruma) in [\#174](https://github.com/hidrokit/hidrokit/pull/174)
* Fitur [\#127](https://github.com/hidrokit/hidrokit/issues/127) Analisis Frekuensi Gumbel by [@taruma](https://github.com/taruma) in [\#175](https://github.com/hidrokit/hidrokit/pull/175)
* Fitur [\#124](https://github.com/hidrokit/hidrokit/issues/124) Analisis Frekuensi Log Normal by [@taruma](https://github.com/taruma) in [\#176](https://github.com/hidrokit/hidrokit/pull/176)
* Fitur [\#172](https://github.com/hidrokit/hidrokit/issues/172) Analisis Frekuensi Normal by [@taruma](https://github.com/taruma) in [\#177](https://github.com/hidrokit/hidrokit/pull/177)
* Fitur [\#179](https://github.com/hidrokit/hidrokit/issues/179) CDF untuk anfrek by [@taruma](https://github.com/taruma) in [\#180](https://github.com/hidrokit/hidrokit/pull/180)
* Fitur [\#140](https://github.com/hidrokit/hidrokit/issues/140) Uji Kolmogorov-Smirnov by [@taruma](https://github.com/taruma) in [\#181](https://github.com/hidrokit/hidrokit/pull/181)
* Fitur [\#141](https://github.com/hidrokit/hidrokit/issues/141) Uji Chi-Square by [@taruma](https://github.com/taruma) in [\#183](https://github.com/hidrokit/hidrokit/pull/183)
* Fitur [\#162](https://github.com/hidrokit/hidrokit/issues/162) Pembaruan fungsi read_workbook by [@taruma](https://github.com/taruma) in [\#184](https://github.com/hidrokit/hidrokit/pull/184)
* Memperbarui github issue template dan .github by [@taruma](https://github.com/taruma) in [\#188](https://github.com/hidrokit/hidrokit/pull/188)
* Pembaruan changelog sampai versi 0.3.6 by [@taruma](https://github.com/taruma) in [\#187](https://github.com/hidrokit/hidrokit/pull/187)
* remove ci and checkers by [@taruma](https://github.com/taruma) in [\#190](https://github.com/hidrokit/hidrokit/pull/190)
* perbarui readme dan informasi lainnya by [@taruma](https://github.com/taruma) in [\#191](https://github.com/hidrokit/hidrokit/pull/191)
* Fitur [\#194](https://github.com/hidrokit/hidrokit/issues/194) Rekap Anfrek by [@taruma](https://github.com/taruma) in [\#195](https://github.com/hidrokit/hidrokit/pull/195)
* Fix [\#201](https://github.com/hidrokit/hidrokit/issues/201) Ubah CDF agar sesuai saat tes KS by [@taruma](https://github.com/taruma) in [\#202](https://github.com/hidrokit/hidrokit/pull/202)
* Fix [\#192](https://github.com/hidrokit/hidrokit/issues/192) RD to Github Actions by [@taruma](https://github.com/taruma) in [\#203](https://github.com/hidrokit/hidrokit/pull/203)
* fitur [\#200](https://github.com/hidrokit/hidrokit/issues/200) modul rekap uji kecocokan distribusi by [@taruma](https://github.com/taruma) in [\#204](https://github.com/hidrokit/hidrokit/pull/204)
* penambahan nama index kala ulang by [@taruma](https://github.com/taruma) in [\#205](https://github.com/hidrokit/hidrokit/pull/205)
* tambah arg show_detail untuk fungsi hk158.check_distribution by [@taruma](https://github.com/taruma) in [\#207](https://github.com/hidrokit/hidrokit/pull/207)
* menambahkan github action untuk jekyll by [@taruma](https://github.com/taruma) in [\#208](https://github.com/hidrokit/hidrokit/pull/208)
* tambah pytest-ci by [@taruma](https://github.com/taruma) in [\#212](https://github.com/hidrokit/hidrokit/pull/212)

# Versi 0.5.x

Saat ini, lebih dari [10 isu](https://github.com/hidrokit/hidrokit/issues) yang masih terbuka di github hidrokit, sehingga untuk saat ini, masih ada ide untuk fitur di versi 0.5.x. Rencananya, fitur 0.5.x akan fokus kepada modul HSS (hidrograf satuan sintetik). Untuk durasi dan mulainya pengembangan tidak dapat saya pastikan saat ini (tapi ada rencananya 4-5 bulan setelah versi 0.4.x). Saya juga ingin mengingatkan bahwa hidrokit sendiri merupakan proyek _open source_, jadi siapapun dapat berkontribusi. Dan tentunya jika terdapat fitur baru di hidrokit dari kontributor lain, versi yang dirilis berikutnya adalah 0.5.x. Jika memiliki kontributor baru, mungkin durasi rilis bisa dipersingkat menjadi per 2-3 bulan tergantung masuknya kontribusi orang lain pada subpaket `.contrib`. Untuk pengembangan diluar subpaket `.contrib` dipertimbangkan dialihkan ke versi 1.x.x.

# FIAKO Engineering

![fiako-logo](/assets/fiako-logo-horizontal.png){: w="50%"}
_PT. FIAKO Enjiniring Indonesia (FIAKO ENGINEERING)_

> 
  _PT. FIAKO Enjiniring Indonesia (FIAKO ENGINEERING) is an Avant Garde engineering consultancy firm in Indonesia. We were established in January 2017. Within our first year, we were acquired some outstanding and remarkable infrastructure projects in Indonesia such as Kalikuto Bridge and Semarang - Batang Toll Road bridges design._ <br>
  _Our company is situated in the city of Bandung, West Java. The firm itself comprises young yet well-experienced experts, energetic, multidisciplinary, integrally and holistically way of think in terms of engineering._ <br>
  _Our aim is to deliver the needs of our clients regarding their requirements within design quality, time and budget. We are waiting for your necessity to be fulfilled by us._ <br>
  \- [_fiako.co.id_](https://www.fiako.co.id/)

Untuk mengetahui lebih lanjut mengenai proyek yang dikerjakan oleh FIAKO Engineering bisa mengunjungi situsnya di [fiako.co.id](https://www.fiako.co.id/) atau [galeri proyek FIAKO Engineering](https://wp.fiako.co.id/wp/gallery/). 

# Penutup

Bagi yang memiliki pertanyaan, kritik, komentar bisa dimulai diskusinya melalui [Forum Diskusi hidrokit](https://github.com/hidrokit/hidrokit/discussions). Untuk memulainya bisa [klik disini](https://github.com/hidrokit/hidrokit/discussions/new) (harap login terlebih dahulu). Untuk kontak langsung ke saya bisa melalui email timhidrokit@gmail.com.

---

[hidrokit]: https://hidrokit.github.io/hidrokit
[hidrokit-notebook]: https://hidrokit.github.io/notebook
[hidrokit-blog]: https://hidrokit.github.io/blog