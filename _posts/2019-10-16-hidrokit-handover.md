---
layout: post
title: hidrokit Handover (2019)
author: "Taruma"
---

Tidak terasa bahwa proyek hidrokit sudah berumur lebih dari satu tahun dari _initial commit_ pada tanggal 20 Agustus 2018. Pada tanggal 9 Januari 2019, saya merilis hidrokit versi 0.1.x, dan enam bulan kemudian pada tanggal 11 Juli 2019, saya merilis hidrokit versi 0.2.x dengan perombakan proyek yang cukup signifikan. Dan pada tanggal 15 Oktober 2019, saya merilis hidrokit versi 0.3.x dengan tambahan fitur kontributor.

Dengan umur lebih dari satu tahun, pribadi, saya ingin meluluskan diri saya dari proyek ini dengan harapan membuat/ikut serta proyek menarik yang baru/sudah ada di masa mendatang. Fokus saya akan mengacu pada proyek mendatang, sehingga proyek ini akan bergerak tergantung keaktifan kontributor yang masih tertarik berkontribusi dalam proyek ini. Saya tidak dapat menjanjikan akan ada versi `MINOR` terbaru di masa mendatang untuk proyek ini. Sejauh ini, dengan tenaga satu orang saja, proyek ini akan lambat berkembang dan membebani saya pribadi. 

Oleh karena itu, saya membuat tulisan ini sebagai bentuk serah terima (_handover_) proyek hidrokit. Tujuan tulisan ini agar memudahkan untuk para pengembang melanjutkan proyek ini ataupun mengembangkan proyek yang baru/serupa. Meski proyek ini terkesan "berakhir" bukan berarti tidak ada yang bisa dipelajari dari pengembangan proyek ini.

Saya juga ingin mengucapkan terima kasih bagi yang terlibat dalam proyek ini. Terima kasih untuk meluangkan waktu untuk membaca, bertanya, membagikan proyek ini. Semoga ada yang bisa dipelajari dari proyek ini.

----

# Serah terima proyek hidrokit / hidrokit _handover_

Serah terima hanya berlaku untuk proyek paket python hidrokit, proyek hidrokit-nb dan hidrokit-blog akan tetap dilanjutkan.

## Pengenalan hidrokit

### Apa itu paket hidrokit?
Paket hidrokit merupakan proyek *open-source* paket *python* yang dapat digunakan untuk membantu proses analisis hidrologi berupa pengolahan data, analisis data, dan visualisasi data. Saat tulisan ini dibuat, hidrokit baru mampu membantu proses dalam pemodelan _Deep Learning_ seperti implementasi _Multi Layer Perceptron_ (MLP) dan _Recurrent Neural Networks_ (RNN) dengan fokus _Long Short-Term Memory_ (LSTM) dalam tahap prapemrosesan data. Untuk lebih jelasnya, lihat [demo hidrokit](#demo-hidrokit).

### Apa makna 'hidrokit'?
Kata `hidrokit` digunakan sebagai penyampaian ide/gagasan: 
- Ajakan penggunaan python, baik dalam lingkungan akademis ataupun industri. Ide ini terwujud dalam proyek `hidrokit` (**hidrokit**) berupa paket python.
- Ajakan untuk membagikan hasil karyanya demi mewujudkan kemajuan teknologi dan kolaborasi. Ide ini terwujud dalam proyek `hidrokit-nb` (**Hidrokit Notebook**) berupa situs kumpulan _jupyter notebook_.
- Ajakan untuk membuat sumber informasi yang bersifat transparan dan kolaboratif. Ide ini terwujud dalam proyek `hidrokit-blog` (**Hidrokit Blog**) berupa blog mengenai hidrokit ataupun sumber pengetahuan terkait sumberdaya air.

### Apa lisensi hidrokit?
Paket hidrokit menggunakan lisensi MIT, lisensi dapat dibaca di [halaman ini](https://github.com/taruma/hidrokit/blob/master/LICENSE.txt). Proyek hidrokit mengikuti panduan definisi _Open Source_ yang dibuat oleh _Open Source Initiative_ (OSI). Definisi _Open Source_ bisa dibaca pada [halaman ini](https://opensource.org/docs/osd).

### Siapa dibalik proyek hidrokit?
Proyek hidrokit dimulai dan dikembangkan oleh [Taruma](https://taruma.github.io) yang berasal dari proyek hobi dan pribadi. 

### Tujuan proyek hidrokit?
Berikut beberapa tujuan hidrokit:
- Mengembangkan alat yang sederhana untuk membantu analisis hidrologi.
- Memperkenalkan alternatif pengolahan data dari berbasis spreadsheet ke notebook (*literate programming*).
- Membangun komunitas pengguna python dan para praktisi atau akademisi yang memanfaatkan python dalam bidang hidrologi.
- Memperkenalkan dan memahami keuntungan proyek open source dan Github.
- Wadah kreativitas dan membuka kesempatan untuk berkolaborasi atau berdiskusi dari berbagai latar belakang.

----

## Perkembangan hidrokit

Tanggal | Versi | Keterangan
:- | :- | :-
20 Agustus 2018 | - | Pembuatan repository
9 Januari 2019 | v0.1.0 | [Halaman Github](https://github.com/taruma/hidrokit/releases/tag/v0.1.0) \| [Tulisan Blog](https://medium.com/@taruma/hidrokit-analisis-hidrologi-dengan-python-bdcad9e5865d)
8 Juni 2019 | v0.1.1 | [Halaman Github](https://github.com/taruma/hidrokit/releases/tag/v0.1.1)
10 Juni 2019 | v0.1.2 | [Halaman Github](https://github.com/taruma/hidrokit/releases/tag/v0.1.2)
25 Juni 2019 | v0.1.3 | [Halaman Github](https://github.com/taruma/hidrokit/releases/tag/v0.1.3)
11 Juli 2019 | v0.2.0 | [Halaman Github](https://github.com/taruma/hidrokit/releases/tag/v0.2.0) \| [Tulisan Blog](https://taruma.github.io/articles/rilis-hidrokit-0-2-0)
26 Juli 2019 | v0.2.1 | [Halaman Github](https://github.com/taruma/hidrokit/releases/tag/v0.2.1)
15 Oktober 2019 | v0.3.2 | [Halaman Github](https://github.com/taruma/hidrokit/releases/tag/0.3.2)

----

## Fitur hidrokit

Saat ini, hidrokit memiliki dua dari tiga sub-paket utama yang dapat digunakan yaitu `.prep` dan `.viz`. Pada versi 0.3.x, hidrokit menambahkan sub-paket bernama `.contrib` yang digunakan sebagai kumpulan _script_ yang dapat diimplementasikan ke hidrokit.

### Sub-paket `.prep`

Terdapat modul:
- `.excel` ([daftar fungsi](https://hidrokit.readthedocs.io/en/stable/prep.html#module-prep.excel)): Digunakan sebagai modul untuk membaca berkas excel.
- `.read` ([daftar fungsi](https://hidrokit.readthedocs.io/en/stable/prep.html#module-prep.read)): Digunakan sebagai modul untuk membaca dataframe.
- `.timeseries` ([daftar fungsi](https://hidrokit.readthedocs.io/en/stable/prep.html#module-prep.timeseries)): Digunakan sebagai modul untuk memanipulasi data _time-series_ (digunakan untuk persiapan ANN).

### Sub-paket `.viz`

Terdapat modul:
- `.graph` ([daftar fungsi](https://hidrokit.readthedocs.io/en/stable/viz.html#module-viz.graph)): Digunakan sebagai modul untuk menampilkan data menggunakan grafik.
- `.table` ([daftar fungsi](https://hidrokit.readthedocs.io/en/stable/viz.html#module-viz.table)): Digunakan sebagai modul untuk menampilkan data dalam bentuk tabel (pivot)

----

## Demo hidrokit

Saat tulisan ini dibuat, terdapat dua _jupyter notebook_ yang mendemonstrasikan penggunaan `hidrokit`. Demo yang tersedia fokus terhadap topik pemodelan menggunakan _deep learning_ di bidang sumber daya air (kualitas air dan curah hujan-limpasan).

- Prediksi Kualitas Air menggunakan Metode _Artificial Neural Networks_ oleh taruma (v2.0.0) \| `hidrokit 0.2.x` \| [Kode](https://github.com/taruma/hidrokit-nb/blob/master/notebook/taruma_demo_ann_ka_2_0_0.ipynb) \| [Lihat melalui NBViewer](https://nbviewer.jupyter.org/github/taruma/hidrokit-nb/blob/master/notebook/taruma_demo_ann_ka_2_0_0.ipynb)
- (Work In Progress) Prediksi Debit Aliran menggunakan _Long Short-Term Memory_ (LSTM) oleh taruma (v1.0.0) \| `hidrokit 0.3.x` \| Kode \| Lihat melalui NBViewer

## Catatan

- Domain hidrokit.online (termasuk subdomain seperti notebook.hidrokit.online dan blog.hidrokit.online) berakhir pada 3 Juli 2021.
- Seluruh proyek disimpan pada situs Github.com.
- Jika tertarik dalam mengambil alih proyek ini (akses repo ini) dapat menghubungi saya di hi@taruma.info.
- Terima kasih untuk semuanya yang terlibat dalam proyek ini. Thank you.