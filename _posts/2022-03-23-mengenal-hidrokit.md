---
title: Mengenal hidrokit
date: 2022-03-20
categories: [Pengumuman]
tags: [hidrokit, dokumentasi]
author:
  name: Taruma Sakti Megariansyah
  link: https://taruma.github.io
pin: false
---

hidrokit adalah proyek _open source_ paket _python_ yang dapat digunakan untuk membantu proses analisis hidrologi dimulai dari pengolahan data, analisis data, dan visualisasi data.

Saat ini, hidrokit masih dalam tahap aktif pengembangan dan pembelajaran. Akan tetapi, fitur yang tersedia di hidrokit sudah bisa digunakan untuk penggunaan praktis atau akademis. 

## Laporan Implementasi
Saya telah membuat contoh implementasi hidrokit dalam kasus hidrologi ataupun _machine learning_. Topik _machine learning_ dikarenakan kebetulan merupakan fokus saya saat menyusun tesis terkait pemodelan curah hujan-limpasan. Untuk laporan yang fokus pada hidrologi bisa melihat pada **LI-03**.

no laporan | tanggal | versi hidrokit | judul | lihat (nbviewer) | pdf
:- | :- | :- | :- | :- | :-
**LI-04** | 11 Februari 2020 | `0.3.5` | Perbandingan Model Variasi _Recurrent Neural Networks_ Pada Kasus Prediksi Debit Aliran | [nbviewer](https://nbviewer.org/gist/taruma/9d1ef5c6d629c792bed0c3f68b324675) | [pdf](https://1drv.ms/b/s!AmxSTa4UunElhoVm7i0EuKdPkPlzVg?e=rjXNpf) 
**LI-03** | 16 Januari 2020 | `0.3.5` | Analisis Hidrologi Menggunakan hidrokit | [nbviewer](https://nbviewer.jupyter.org/gist/taruma/4c1ed1212290965ecda056f45d7aaea2) | [pdf](https://1drv.ms/b/s!AmxSTa4UunElhoU3ehyoy45_RG6hjA?e=5wUb8d)
**LI-02** | 22 Oktober 2019 | `0.3.2` | Prediksi Debit Aliran Menggunakan Long Short-Term Memory (LSTM) | [nbviewer](https://nbviewer.jupyter.org/gist/taruma/8186dba212875f6b3f1677a5e2f9a70f) | [pdf](https://1drv.ms/b/s!AmxSTa4UunElhoU1sISX0gc4BammwQ?e=MGHcwT)
**LI-01** | 13 Juli 2019 | `0.2.0` | Prediksi Kualitas Air Menggunakan Artificial Neural Networks | [nbviewer](https://nbviewer.jupyter.org/gist/taruma/12bf06ab7307340525eecf5b3c8beb9c) | [pdf](https://1drv.ms/b/s!AmxSTa4UunElhoU27FZ3pMHVvWeMsA?e=ouC2KK)

Daftar ini bisa lihat di situs dokumentasi saya bernama [vivaldi](https://taruma.github.io/vivaldi/laporan-implementasi) atau di [academia.edu](https://independent.academia.edu/TarumaMegariansyah).

## Daftar Fitur hidrokit (`0.3.6`)

**Daftar modul `.contrib.taruma`**

Isu | Modul | Versi | Keterangan | Manual
:- | :- | :- | :- | :-
#106 | `.hk106` | `0.3.5` | Perhitungan evapotranspirasi | [Gist](https://gist.github.com/taruma/7f81cf0fea5250cfe47942b4e16a8a65)
#102 | `.hk102` | `0.3.5` | Upsampling dataset | [Gist](https://gist.github.com/taruma/96c321175ecac3e51350ef4c94f3d7d4)
#96 | `.hk96` | `0.3.5` | Pemodelan F.J. Mock | [Gist](https://gist.github.com/taruma/ae5c0209ef19b088e3cd9dd22508af5c)
#98 | `.hk98` | `0.3.5` | Rekap dataset deret waktu | [Gist](https://gist.github.com/taruma/aca7f90c8fbb0034587809883d0d9e92)
#99 | `.hk99` | `0.3.5` | Perhitungan curah hujan dengan metode poligon Thiessen | [Gist](https://gist.github.com/taruma/8dd920bee9fa95cf6eba39cc9d694953)
#90 | `.hk90` | `0.3.5` | Kalibrasi Model (NRECA/FJ_MOCK) | [Gist](https://gist.github.com/taruma/906e1577111208291e0725229c7d0a76)
#89 | `.hk89` | `0.3.5` | Pemodelan NRECA | [Gist](https://gist.github.com/taruma/1502a7aa67cf074969d806cd3ffdf35c)
#87 | `.hk87` | `0.3.5` | Perhitungan debit andalan menggunakan kurva durasi debit | [Gist](https://gist.github.com/taruma/0b0ebf3ba12d4acf7cf11df905d2ec9c)
#88 | `.hk88` | `0.3.5` | Ambil dataset hujan harian dari excel | [Gist](https://gist.github.com/taruma/6d48b3ec9d601019c15fb5833ae03730)
#84 | `.hk84` | `0.3.4` | Meringkas informasi data hujan jam-jaman | [Gist](https://gist.github.com/taruma/cad07f29ffc025ba9e7801e752be3444)
#79 | `.hk79` | `0.3.3` | Mengekstrak informasi data jam-jaman dari excel | [Gist](https://gist.github.com/taruma/05dab67fac8313a94134ac02d0398897)
#43 | `.hk43` | `0.3.2` | Mengubah pivot table ke dataframe | [Gist](https://gist.github.com/taruma/a9dd4ea61db2526853b99600909e9c50)
#53 | `.hk53` | `0.3.2` | Membuat tensor input untuk pemodelan LSTM/RNN | [Gist](https://gist.github.com/taruma/50460ebfaab5a30c41e7f1a1ac0853e2)
#73 | `.hk73` | `0.3.2` | Mengolah berkas dari BMKG | [Gist](https://gist.github.com/taruma/b00880905f297013f046dad95dc2e284)

Untuk modul/fungsi selain subpaket `.contrib` bisa dilihat di [hidrokit documentation](https://hidrokit.readthedocs.io). Dengan catatan bahwa pengembangan dialihkan ke `.contrib` terlebih dahulu untuk saat ini. 

## Sejarah hidrokit
Saya memulai proyek hidrokit dengan membuat _repository_ di github pada tanggal 20 Oktober 2018. Pada saat itu, hidrokit hanya muncul sebagai ide dari perjalanan saya belajar python dan _data science_. Pada tanggal 9 Januari 2019, saya merilis versi `0.1.0`. Saya telah mengimplementasikan instalasi menggunakan `pip` dan perencanaan penggunaan _semantic versioning_ (meski ujung-ujungnya tidak begitu konsisten). Saya juga pada versi `0.1.0`, mulai mengajak bagi yang tertarik dengan penggunaan python di bidang hidrologi dengan [tulisan ini](https://medium.com/@taruma/hidrokit-analisis-hidrologi-dengan-python-bdcad9e5865d) (tautannya sudah banyak yang tidak aktif lagi). Saat itu, versi tersebut tidak begitu praktis gunakan. Tujuan waktu itu hanya ingin melihat _engagement_ terkait penggunaan python di pekerjaan hidrologi (yang memiliki porsi signifikan dalam pengolahan _spreadsheet_).

Enam bulan berlalu, saya merilis versi `0.2.0` pada 11 Juli 2019, dan ini merupakan rilis menurut saya layak dipublikasikan atau disebarkan ke banyak orang melalui [tulisan ini](https://taruma.github.io/articles/rilis-hidrokit-0-2-0). Pada rilisnya versi tersebut saya telah membuat situs/website untuk [hidrokit](https://hidrokit.github.io/hidrokit), situs untuk kumpulan notebook yang menggunakan python+hidrologi bernama [hidrokit notebook](https://hidrokit.github.io/notebook). Tujuan membuat situs tersebut dengan harapan meningkatkan _engagement_, tapi sejauh ini yang berkontribusi hanya saya sendiri 🤣. Pada versi tersebut, saya mulai merekonstruksi struktur paket hidrokit agar lebih konsisten kedepannya. Membagi menjadi 3 subpaket utama yaitu `.prep`, `.viz`, dan `.analysis`.  Sejauh ini, hidrokit bisa digunakan untuk melakukan pemodelan ANN sederhana seperti [contoh ini](https://nbviewer.org/github/taruma/hidrokit-nb/blob/master/notebook/taruma_demo_ann_ka_2_0_0.ipynb).

Setelah versi `0.2.0`, saya sadari bahwa untuk membuat suatu _software_ yang layak _publish_ itu cukup merepotkan. Selain harus mengikuti standar yang biasa diterapkan di _software developement_, saya juga tidak mau melakukan kesalahan seperti _breaking changes_ dari versi `0.1.x` ke `0.2.0`. Maka dari itu, saya mulai berpikir untuk mencari solusi dimana saya bisa terus bereksperimen dan mengembangkan hidrokit tanpa melakukan perubahan yang merusak versi-versi sebelumnya. 

Dan solusi yang saya temukan saat itu, membuat subpaket `.contrib` untuk melakukan pengembangan mandiri tanpa mempengaruhi paket utama hidrokit. Hal ini, memberi waktu dan ruang untuk saya belajar bagaimana pengembangan paket python dan modul-modul yang dapat membantu proses analisis hidrologi. 

Sekitar 3 bulan berlalu, saya merilis versi `0.3.2` pada tanggal 15 Oktober 2019, yang seharusnya versi 0.3.0, tapi karena sayanya melakukan kesalahan dalam mengintegrasikannya dengan zenodo, kekeliruan tersebut terjadi dan saya terpaksa untuk meningkatkan versinya. Yah, bagian dari pengalaman dan pembelajaran lah ya 😁. Pada versi `0.3.2`, saya rasanya tidak mempublikasikan dalam bentuk tulisan. Tapi pada versi ini, saya mulai bereksperimen dengan membuat _laporan implementasi_, yaitu _notebook_ yang berisikan implementasi penggunaan hidrokit dan hidrologi/_data science_. Bagi yang penasaran laporan implementasi saya bisa lihat di situs [vivaldi (proyek dokumentasi implementasi)](https://taruma.github.io/vivaldi/laporan-implementasi) atau bisa melalui [academia.edu](https://independent.academia.edu/TarumaMegariansyah).

Dari versi `0.3.2` hingga `0.3.5` saya menambahkan beberapa modul yang menurut saya menarik untuk dicoba dalam _workflow_ analisis hidrologi. Untuk daftar modul yang dikembangkan sampai versi `0.3.5` bisa dilihat [di sini](https://taruma.github.io/articles/hidrokit-contrib-taruma).  Pada versi `0.3.5` yang saya rilis pada 15 Januari 2020, saya memutuskan untuk membuat proyek hidrokit dalam status hiatus (sempat terpikirkan untuk diarsip). Versi `0.3.5` ini membantu saya dalam beberapa penyelesaian kasus dalam menyelesaikan tesis (meski sejak versi `0.3.2` sudah mulai membantu). Saat itu saya sudah menuliskan kabar buruk tersebut [disini](https://medium.com/@taruma/hidrokit-pada-tahun-2020-c00cd8860c0e) . Saat saya bereksperimen dengan hidrokit, terutama  `hidrokit.timeseries.timestep_table()` saya menemukan bug yang kritis, sehingga mau tidak mau saya harus publish _bugfix_ secepatnya. Dan rilislah versi `0.3.6` yang tidak direncanakan pada 13 Juli 2020. 

Dan dua tahun berlalu (ditambah isu pandemi), kembali ke masa sekarang, tahun 2022, saya mulai membangkitkan lagi hidrokit. Hal ini karena dukungan dari [PT. FIAKO Enjiniring Indonesia](http://www.fiako.co.id/) (FIAKO Engineering). Dengan dukungan tersebut, saya mulai bisa membuat hidrokit dalam status aktif pengembangan. Dan bulan April 2022 sudah direncanakan untuk merilis versi 0.3.7. Saya juga akan mulai memperkenalkan hidrokit melalui media seperti _livestream_ atau _zoom_ rencananya.  

Dengan kerjasama dan dukungan tersebut. bisa jadi, setelah hidrokit ada paket python lainnya lagi untuk bidang sipil lainnya🤞.