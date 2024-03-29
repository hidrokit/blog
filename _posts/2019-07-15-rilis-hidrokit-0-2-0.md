---
title: Rilis hidrokit 0.2.0
date: 2019-07-15
categories: [Pengumuman]
tags: [hidrokit, dokumentasi]
author:
  name: Taruma Sakti Megariansyah
  link: https://taruma.github.io
---

[Enam bulan yang lalu](https://medium.com/@taruma/hidrokit-analisis-hidrologi-dengan-python-bdcad9e5865d), saya merilis hidrokit 0.1.0. Pada saat itu, banyak sekali kekurangan dari segi dokumentasi maupun teknis sehingga cukup sulit untuk memulai berkontribusi bagi yang tertarik untuk ikut serta dalam proyek _open-source_ ini. Dengan rilis 0.2.0, saya mencoba menjawab permasalahan tersebut dengan menyertai berbagai fitur untuk paket python hidrokit maupun dokumentasi sehingga memudahkan berkontribusi bagi yang tertarik dengan proyek ini. 

## Pengenalan

Hidrokit merupakan proyek _open-source_ paket/_package_ python yang dapat digunakan untuk membantu proses analisis hidrologi berupa pengolahan data, analisis data, dan visualisasi data. Saat ini, proyek ini masih **dalam tahap pengembangan**, sehingga untuk penggunaan praktis belum memadai. Proyek ini cocok bagi yang tertarik untuk ikut serta dalam proyek _open-source_ karena masih dalam tahap awal pengembangan. Dengan proyek ini, hidrokit juga bertujuan membangun komunitas pengguna python (jupyter notebook) dan para praktisi atau akademisi yang memanfaatkan python dalam bidang hidrologi.  

Baca [abstrak dan tujuan hidrokit](https://taruma.github.io/hidrokit/tentang-hidrokit) untuk informasi lebih lanjut.

Jika ingin langsung melihat kegunaan hidrokit (python dan jupyter notebook) bisa lihat contoh notebook berikut:
- **Prediksi Kualitas Air menggunakan Metode _Artificial Neural Networks_ oleh taruma**. [Lihat melalui NBViewer](https://nbviewer.jupyter.org/github/taruma/hidrokit-nb/blob/master/notebook/taruma_demo_ann_ka_2_0_0.ipynb).
- **Daftar tutorial fungsi/modul pada hidrokit dapat dilihat di** [**halaman ini**](https://notebook.hidrokit.online/kumpulan-notebook#hidrokit-).

Jika Anda tertarik berkontribusi pada proyek ini, baca bagian [kontribusi](#berkontribusi). Proyek ini terbuka untuk berbagai latar belakang dan tingkat keahlian. Saya juga telah membuat tanya jawab seputar proyek ini pada bagian [FAQ](#frequently-asked-questions).

-----
## Apa yang baru di hidrokit 0.2.0?

Pada hidrokit 0.2.0, pengembangan python diusahakan untuk mengikuti standar yang ada dimulai dari _packaging_, _versioning_, _testing_, dan _continous integration_. Hal tersebut mengakibatkan hidrokit 0.2.0 tidak _backward-compatibility_ dengan hidrokit 0.1.x. Diharapkan dengan struktur sekarang, hidrokit 0.2.0 memiliki kapasitas untuk _forward-compatibility_ dan memudahkan bagi _developer_ mengembangkan fitur baru atau memperbaiki fitur.

Dengan rilisnya hidrokit 0.2.0, diperkenalkan **tiga** situs utama yang berhubungan dengan proyek ini. 
- [hidrokit.online]\: Situs resmi proyek hidrokit yang berisikan dokumentasi berupa tentang hidrokit (tujuan/abstrak), tutorial/panduan berkontribusi, dll. 
- [notebook.hidrokit.online]\: Situs pelengkap yang berisikan kumpulan jupyter notebook mengenai penggunaan hidrokit dan pemanfaatan python dalam bidang hidrologi.
- [hidrokit.readthedocs.io]\: Situs berbahasa inggris yang digunakan sebagai dokumentasi teknis berisikan daftar lengkap _Application Programming Interface_ (API) yang tersedia di proyek hidrokit. Situs ini ditujukan untuk pengembang / _developer_.

Dibuatnya situs agar memudahkan akses informasi melalui berbagai media (komputer, telepon genggam). Navigasi dan tampilan pada situs juga lebih mudah dibandingkan melalui halaman github karena halaman github lebih ditujukan untuk _developer_. 

<div align="center" markdown="1">
**Berikut daftar perubahan di hidrokit 0.2.0**
</div>

-----
## hidrokit 0.2.0

Perubahan berikut ditujukan untuk membuat proyek hidrokit lebih terstruktur dan lebih mudah untuk dikembangkan lebih lanjut.  Berikut perubahan penting hidrokit 0.1.x ke 0.2.0:

**Baru**
- Paket dibagi menjadi tiga subpaket (_subpackage_) utama yaitu persiapan (`hidrokit.prep`), analisis (`hidrokit.analysis`), dan visualisasi (`hidrokit.viz`). 
- Integrasi [travis-ci], [codecov], [codacy].
- Testing menggunakan [pytest] dengan 90%+ _coverage_.
- Situs khusus untuk dokumentasi teknis di [hidrokit.readthedocs.io](https://hidrokit.readthedocs.io) yang berisikan daftar API hidrokit dibangkitkan menggunakan _docstring_.

**Perubahan**
- Penamaan modul dan fungsi diubah dan disesuaikan dengan [standar PEP8](https://www.python.org/dev/peps/pep-0008/).
- Fungsi pada modul berikut digantikan dengan modul baru dibawah subpaket baru.

| Modul di 0.1.x  | 0.2.0 |
| :-- | :-- |
| `dlkit` | `prep.timeseries` dan `viz.graph` |
| `viewkit` | `viz.table` |
| `prepkit` | `prep.excel` |
| `datakit` | `prep.read` |

- Perubahan nama fungsi agar lebih jelas dan mengubah fungsi yang bukan ditujukan untuk penggunaan menjadi _private function_.
  - Seluruh fungsi pada `prepkit` yang berfungsi membaca berkas _excel_, untuk sementara menjadi _private function_.
  - Perubahan nama fungsi pada `dlkit` dan `datakit`.

| Nama Fungsi di 0.1.x  | 0.2.0 |
| :-------------------------------- | :------------------------------- |
| `dlkit.plot_dataset`              | `viz.graph.subplots`             |
| `datakit.dict_null_data`          | `prep.read.missing_row`          |
| Fungsi column timesteps           | `prep.timeseries.timestep_table` |
| - `dlkit.single_column_timesteps` | _private_                        |
| - `dlkit.multi_column_timesteps`  | _private_                        |

**Penghilangan**
- Modul `bmkgkit` dihapuskan dan tidak digantikan.
- Modul berikut ini telah dihapus/digantikan sehingga tidak dapat digunakan lagi:
  - `dlkit`, `viewkit`, `bmkgkit`, `prepkit`, `datakit`.

<!-- LINK -->
[travis-ci]: https://travis-ci.org/taruma/hidrokit
[codecov]: https://codecov.io/gh/taruma/hidrokit
[codacy]: https://app.codacy.com/project/taruma/hidrokit/dashboard
[pytest]: https://pytest.org/

-----
## Situs hidrokit

<img src="https://github.com/taruma/hidrokit/blob/gh-pages/assets/images/presskit/hidrokit-pages.png?raw=true" class="figure-img img-fluid rounded" height="50%" width="50%" alt="Logo Hidrokit">

Situs hidrokit digunakan sebagai situs utama untuk memperoleh informasi mengenai proyek ini. Situs ini dibuat menggunakan [Jekyll](https://jekyllrb.com/) dan [Github Pages](https://pages.github.com/) _hosting_. _Repository_ situs dapat diakses di [cabang gh-pages](https://github.com/taruma/hidrokit/tree/gh-pages).

Berikut halaman penting yang tersedia pada situs hidrokit:

| Halaman | Keterangan |
| :---------------- | :----- |
| [tentang-hidrokit] | Abstrak dan Tujuan hidrokit. Dorongan untuk berkontribusi. |
| [berkontribusi] | Informasi umum untuk memulai berkontribusi. |
| [kode-etik] | Kode etik dalam proyek. |
| [instalasi] | Pemasangan/instalasi paket hidrokit. |
| [penggunaan] | Penggunaan paket hidrokit. |
| [sumber] | Daftar sumber yang digunakan dalam proyek. |

<!-- LINK -->
[tentang-hidrokit]: https://hidrokit.online/tentang-hidrokit
[berkontribusi]: https://hidrokit.online/berkontribusi
[kode-etik]: https://hidrokit.online/berkontribusi/kode-etik
[instalasi]: https://hidrokit.online/panduan/instalasi
[penggunaan]: https://hidrokit.online/panduan/penggunaan
[sumber]: https://hidrokit.online/serbaneka/sumber

-----
## Situs Hidrokit Notebook

<img src="https://github.com/taruma/hidrokit-nb/blob/master/docs/assets/images/hidrokit-nb-pages.png?raw=true" class="figure-img img-fluid rounded" height="50%" width="50%" alt="Logo Hidrokit Notebook">


Situs Hidrokit digunakan sebagai situs pelengkap yang berisikan kumpulan jupyter notebook mengenai penggunaan hidrokit dan pemanfaatan python dalam bidang hidrologi. Situs ini dibuat menggunakan [Jekyll](https://jekyllrb.com/) dan [Github Pages](https://pages.github.com/) _hosting_. _Repository_ situs dapat diakses di [hidrokit-nb](https://github.com/taruma/hidrokit-nb/tree/master/docs).

Berikut halaman penting yang tersedia pada situs Hidrokit Notebook:

| Halaman | Keterangan |
| :---------------- | :----- |
| [kumpulan-notebook] | Daftar kumpulan notebook yang telah dikategorikan dan tersedia. |
| [mengunggah-notebook] | Panduan _upload_/mengunggah notebook. |
| [lisensi-notebook] | Keterangan lisensi notebook. |
| [pull-request] | Panduan lanjutan untuk memperbarui repo dan melakukan _pull request_ berikutnya. |
| [tambah-notebook] | Panduan menambah notebook ke halaman [kumpulan-notebook]. |
| [unduh-notebook] | Panduan mengunduh notebook. |

<!-- LINK -->
[kumpulan-notebook]: https://notebook.hidrokit.online/kumpulan-notebook
[mengunggah-notebook]: https://notebook.hidrokit.online/panduan/mengunggah-notebook
[lisensi-notebook]: https://notebook.hidrokit.online/panduan/lisensi-notebook 
[pull-request]: https://notebook.hidrokit.online/panduan/pull-request
[tambah-notebook]: https://notebook.hidrokit.online/panduan/tambah-notebook
[unduh-notebook]: https://notebook.hidrokit.online/panduan/unduh-notebook

-----
## Berkontribusi

Seluruh yang disebutkan pada proyek ini berupa paket python hidrokit, situs hidrokit, situs Hidrokit Notebook, situs readthedocs bersifat _open-source_ sehingga Anda bisa mengajukan perubahan, berkontribusi, atau bahkan Anda bisa mengembangkannya sebagai proyek Anda sendiri. Karena seluruh proyek ini menggunakan [**MIT License**](https://choosealicense.com/licenses/mit/) dan [**CC-BY-4.0**](https://choosealicense.com/licenses/cc-by-4.0/) kecuali disebutkan secara terpisah seperti pada [notebook](https://notebook.hidrokit.online/panduan/lisensi-notebook).

Panduan umum untuk berkontribusi dapat dibaca pada halaman [berkontribusi](https://hidrokit.online/berkontribusi).

Proyek ini berusaha memberi wadah bagi individu yang tertarik berkontribusi di proyek open-source dari berbagai latar belakang. Seperti yang dijelaskan pada halaman [how to contribute](https://opensource.guide/how-to-contribute/), Anda dapat berkontribusi pada proyek selain implementasi kode. Proyek ini juga memberi kesempatan dari berbagai tingkat keahlian. Ilustrasi berkontribusi di Github:

<div align="center">
<iframe width="420" height="315" src="http://www.youtube.com/embed/w3jLJU7DT5E" frameborder="0" allowfullscreen></iframe>
</div>

- Jika Anda seorang **_praktisi/akademisi di bidang hidrologi_**, Anda bisa menyampaikan ide/fitur yang cocok disertakan di proyek ini, berdiskusi tentang impelementasi pada python, dll.
- Jika Anda tetarik pada pengembangan **_web_**, Anda bisa memberikan ide desain situs, menyarankan tema yang sesuai, mengembangkan tema Jekyll yang sesuai dengan proyek ini, bereksperimen dengan Jekyll dan Github Pages. Ada dua situs yaitu [hidrokit] dan [hidrokit-notebook], jadi ada wadah bereksperimen atau berkontribusi pada proyek ini bagi yang tertarik. 
- Jika Anda tertarik pada pengembangan **_python_**, Anda bisa mengevaluasi implementasi kode, menerapkan fitur, _refactoring_ kode, dll.
- Jika Anda tertarik pada **dokumentasi**, Anda bisa menyunting penulisan situs, memperbaiki penulisan agar lebih jelas, menerjemahkan, dll.
- Jika Anda tertarik pada **memperkenalkan/pengajaran**, Anda bisa membuat tutorial dengan python/jupyter notebook dan mengunggahnya di [hidrokit-notebook].
- Jika Anda **memiliki kode python** yang cocok dengan proyek ini, Anda bisa menguploadnya pada github Anda dan menyarankan untuk diimplementasikan dalam proyek ini.
- Jika Anda tertarik **merancang** logo, jangan ragu untuk menyampaikannya di proyek ini. 
- Jika Anda tertarik pada aspek **komunitas**, Anda bisa mengajak acara _meet-up_ komunitas hidrokit.
- Jika Anda menyukai **mengorganisir**, Anda bisa membantu mengorganisasikan isu/diskusi di github.
- Jika Anda **baru belajar**/mengenal python/jupyter/proyek ini, Anda bisa bertanya, berdiskusi, dan berbagi pengalaman Anda di proyek ini.
- Jika Anda **memiliki pengalaman** terkait proyek ini, Anda bisa berbagi pengalaman Anda.
- Jika Anda **hanya menggunakan** proyek/situs ini, Anda juga bisa berkontribusi dengan melaporkan kerusakan/kekeliruan/koreksi. 

Intinya, kalau ada ide jangan dibiarkan terbang, buat isu/diskusi di github [sekarang juga](https://github.com/taruma/hidrokit/issues/new/choose).

-----
## Frequently Asked Questions

Saya akan berusaha menjawab pertanyaan yang mungkin menjadi perhatian/pertimbangan.

**Siapa dibalik proyek hidrokit?**

> Proyek hidrokit dibuat dan dimulai oleh [Taruma Sakti Megariansyah](https://taruma.info) (saya sendiri. 😁). Saya merupakan lulusan sarjana teknik sipil dari Universitas Katolik Parahyangan, Bandung angkatan 2008. Saya tidak memiliki pengalaman kerja baik di bidang hidrologi atau bidang komputer (python), jadi proyek ini akan jauh dari sempurna atau tepat sasaran. 😅. 

**Apakah proyek ini bagian dari tugas/kerjaan?**

> Proyek hidrokit, _murni_ merupakan **proyek hobi** dan **pribadi**. 
> 
> **Proyek ini bukan**:
> - Bagian dari pekerjaan (yang tidak saya miliki 😉)
> - Untuk menyelesaikan kewajiban akademis (tugas akhir/tesis)
> - Permintaan dari perusahaan / konsultan / praktisi / akademisi / individu. 

**Keuntungan apa yang segera didapatkan jika menggunakan hidrokit?**

> hidrokit **bukan** program yang berfungsi memasukkan _input data_ kemudian langsung memperoleh _output data_ atau laporan. Sehingga tidak bisa "segera" diuntungkan saat beralih ke penggunaan hidrokit/python.
> 
> Jika Anda telah menggunakan python dan jupyter notebook pada alur kerja Anda, kemungkinan paket hidrokit bisa mempersingkat/mempercepat alur kerja tersebut. Jadi, sebelum menggunakan hidrokit, **diasumsikan sudah terbiasa** menggunakan python dan jupyter notebook. 
> 
> Bagi yang belum tahu python dan jupyter notebook, proyek ini memperkenalkan keuntungan hal tersebut dan membantu Anda memulai petualangan tersebut. Saat tulisan ini dipublikasi, belum ada halaman panduannya, tapi jika Anda membutuhkan bantuan, buat isu/diskusi [disini](https://github.com/taruma/hidrokit/issues/new/choose).
> 
> Proyek ini hanya **memperkenalkan** python + jupyter notebook pada umumnya, dan bukan memaksakan untuk beralih dari _spreadsheet_. Pandangan pribadi saya adalah lebih praktis dan intuitif menggunakan python + jupyter notebook + hidrokit dibandingkan menggunakan _spreadsheet_. 
> 
> Sebagai informasi, saya belum memiliki pengalaman kerja di bidang hidrologi atau _python/data science_. Jadi, saya tidak bisa menjawab dengan tepat dampak positif/negatif proyek ini.

Anda bisa membaca FAQ lanjutannya di halaman [Tanya Jawab Rilis Hidrokit 0.2.0]({% link _posts/2019-07-18-tanya-jawab-hidrokit-0-2-0.md %}).

-----

Terima kasih atas perhatiannya, jika Anda memiliki pertanyaan/kritik/saran mengenai proyek ini Anda bisa membuat isu/diskusi di [halaman github](https://github.com/taruma/hidrokit/issues/new/choose). Anda bisa menghubungi saya melalui email di __hi@taruma.info__ (Jika terkait proyek hidrokit, dianjurkan untuk melalui github).

Mengakhiri tulisan ini dengan video inspiratif dari Github.

<div align="center">
<iframe width="420" height="315" src="http://www.youtube.com/embed/HzZxcfVn_08" frameborder="0" allowfullscreen></iframe>
</div>

<div align="center">
<small class="text-muted mb-2">
"This project is dedicated to '<i>my younger me</i>'. Good luck! ♥"
</small>
</div>

<!-- LINK -->
[hidrokit]: https://taruma.github.io/hidrokit
[hidrokit-notebook]: https://taruma.github.io/hidrokit-nb
[hidrokit.online]: https://taruma.github.io/hidrokit
[notebook.hidrokit.online]: https://taruma.github.io/hidrokit-nb
[hidrokit.readthedocs.io]: https://hidrokit.readthedocs.io