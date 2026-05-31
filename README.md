# Pelatihan Spatial Econometrics

## Ringkasan

Pelatihan *Spatial Econometrics* dirancang untuk membekali peneliti, dosen, mahasiswa pascasarjana, dan analis kebijakan dengan kemampuan menganalisis data yang memiliki dimensi keruangan (*spatial data*). Banyak fenomena ekonomi—pertumbuhan regional, produktivitas perusahaan, harga properti, kemiskinan, hingga aglomerasi industri—tidak berdiri sendiri di setiap unit observasi, melainkan saling memengaruhi antarwilayah yang berdekatan. Asumsi independensi observasi yang menjadi landasan metode OLS klasik menjadi tidak memadai ketika terdapat *spatial dependence* dan *spatial heterogeneity*. Pelatihan ini menjawab kebutuhan tersebut dengan pendekatan terapan, menekankan praktik estimasi langsung menggunakan perangkat lunak Stata.

## Latar Belakang dan Urgensi

Data ekonomi regional pada hakikatnya melanggar hukum pertama geografi Tobler: "segala sesuatu berhubungan dengan segala sesuatu yang lain, tetapi hal-hal yang dekat lebih berhubungan daripada yang jauh." Mengabaikan ketergantungan spasial menimbulkan dua konsekuensi serius. Pertama, jika model sebenarnya mengandung *spatial lag* pada variabel dependen, estimasi OLS menjadi bias dan tidak konsisten. Kedua, jika ketergantungan terletak pada error, OLS tetap tidak bias namun menghasilkan estimasi varians yang keliru sehingga uji statistik menjadi tidak valid. Pelatihan ini memberi peserta kerangka diagnostik dan pemodelan untuk menangani kedua persoalan tersebut secara sistematis.

## Tujuan Pelatihan

Setelah menyelesaikan pelatihan, peserta diharapkan mampu:

1. Memahami konsep dasar ketergantungan dan heterogenitas spasial serta implikasinya terhadap inferensi ekonometrik.
2. Membangun dan mengevaluasi matriks bobot spasial (*spatial weights matrix*) yang sesuai dengan struktur data.
3. Melakukan uji dependensi spasial menggunakan statistik Moran's I dan uji pengganda Lagrange (LM).
4. Mengestimasi dan menafsirkan model spasial utama: *Spatial Autoregressive* (SAR), *Spatial Error Model* (SEM), *Spatial Durbin Model* (SDM), serta model gabungan (SARAR/SAC).
5. Menghitung dan menginterpretasikan efek langsung, tidak langsung (*spillover*), dan total.
6. Menerapkan seluruh prosedur menggunakan Stata pada data cross-section maupun data panel spasial.

## Sasaran Peserta

Pelatihan ditujukan bagi peneliti bidang ekonomi regional dan perkotaan, dosen, mahasiswa S2/S3, ekonom di lembaga pemerintah dan badan statistik, serta analis kebijakan yang bekerja dengan data antarwilayah. Peserta diharapkan telah memiliki dasar ekonometrika (regresi linier, asumsi klasik, inferensi) dan pengalaman dasar menggunakan Stata. Pengetahuan tentang aljabar matriks akan membantu, namun materi disajikan secara bertahap sehingga tetap dapat diikuti.

## Materi Pelatihan

### Modul 1 — Fondasi Ekonometrika Spasial
Pengantar konsep *spatial dependence* dan *spatial heterogeneity*; perbedaan antara efek substantif (model lag) dan efek nuisance (model error); tinjauan singkat keterbatasan OLS dalam konteks spasial; serta gambaran umum tipologi model spasial (taksonomi Anselin dan LeSage-Pace).

### Modul 2 — Matriks Bobot Spasial
Pembentukan matriks bobot berbasis kontiguitas (*rook* dan *queen*), berbasis jarak (*inverse distance*, *k-nearest neighbors*), dan berbasis ambang batas jarak. Pembahasan proses *row-standardization*, sensitivitas hasil terhadap pilihan matriks, serta praktik membangun matriks dari *shapefile* dan koordinat menggunakan perintah `spmatrix` dan paket `spmat` di Stata.

### Modul 3 — Diagnostik Ketergantungan Spasial
Statistik Moran's I global dan interpretasinya melalui *Moran scatterplot*; indikator asosiasi spasial lokal (LISA) untuk mendeteksi *cluster* dan *outlier*; serta uji LM-lag, LM-error, dan versi robustnya sebagai dasar pemilihan spesifikasi model yang tepat.

### Modul 4 — Model Spasial Cross-Section
Estimasi *Maximum Likelihood* dan *Generalized Method of Moments* untuk model SAR, SEM, SDM, dan SARAR. Strategi pemilihan model (pendekatan *specific-to-general* dan *general-to-specific*); uji rasio likelihood; serta penekanan kuat pada interpretasi efek marginal. Peserta akan dilatih membedakan efek langsung, tidak langsung, dan total karena koefisien dalam model SAR tidak dapat ditafsirkan secara langsung seperti pada OLS.

### Modul 5 — Data Panel Spasial
Perluasan ke model panel dengan efek tetap (*fixed effects*) dan efek acak (*random effects*) berdimensi spasial; model dinamis spasial; serta penanganan persoalan endogenitas. Implementasi praktis menggunakan perintah `xsmle` dan keluarga perintah `sp` pada Stata 16 ke atas.

### Modul 6 — Studi Kasus dan Aplikasi Kebijakan
Aplikasi pada data riil Indonesia, misalnya konvergensi pendapatan antarprovinsi, *spillover* produktivitas, atau efek aglomerasi terhadap pertumbuhan kota. Peserta diajak menghubungkan hasil estimasi dengan rekomendasi kebijakan pembangunan wilayah yang berbasis bukti.

## Metode Pelatihan

Pelatihan menggunakan pendekatan *learning by doing* dengan komposisi sekitar 40 persen pemaparan konsep dan 60 persen praktik langsung. Setiap modul diakhiri dengan sesi *hands-on* menggunakan data latih yang disediakan, sehingga peserta dapat segera menerjemahkan teori menjadi *do-file* yang dapat direplikasi. Diskusi kelompok dan klinik analisis disediakan agar peserta dapat membawa dan membahas data penelitian mereka sendiri.

## Perangkat dan Persyaratan Teknis

Peserta diharapkan membawa laptop dengan Stata versi 16 atau lebih baru yang sudah terpasang, karena perintah `sp` bawaan tersedia mulai versi tersebut. Untuk versi lebih lama, paket komunitas seperti `spmat`, `spreg`, dan `xsmle` akan digunakan dan dapat diinstal melalui `ssc install`. Materi, data latih, dan kumpulan *do-file* akan dibagikan kepada seluruh peserta sebagai bahan rujukan pascapelatihan.

## Luaran yang Diharapkan

Pada akhir pelatihan, peserta akan memiliki: (i) pemahaman konseptual yang kokoh mengenai kapan dan mengapa model spasial diperlukan; (ii) keterampilan teknis membangun matriks bobot, mendiagnosis dependensi spasial, dan mengestimasi model spasial di Stata; serta (iii) kemampuan menafsirkan efek *spillover* secara benar untuk keperluan publikasi ilmiah maupun analisis kebijakan. Luaran ini diharapkan langsung dapat diterapkan pada riset disertasi, artikel jurnal, maupun kajian lembaga.

## Durasi dan Jadwal

Pelatihan diselenggarakan selama tiga hari penuh (sekitar 18–21 jam efektif), dengan pembagian: hari pertama untuk Modul 1–2, hari kedua untuk Modul 3–4, dan hari ketiga untuk Modul 5–6 serta klinik analisis. Format ini dapat disesuaikan menjadi versi intensif dua hari atau versi diperpanjang dengan sesi pendampingan tambahan, bergantung pada kebutuhan dan tingkat pengalaman peserta.

## Penutup

Ekonometrika spasial telah menjadi instrumen yang semakin penting dalam riset ekonomi regional dan perkotaan, terutama ketika pertanyaan penelitian menyangkut interaksi antarwilayah dan efek limpahan. Dengan menggabungkan landasan teori yang ringkas dan praktik Stata yang intensif, pelatihan ini dirancang agar peserta tidak sekadar memahami metode, tetapi mampu menerapkannya secara mandiri dan menafsirkan hasilnya dengan benar dalam konteks penelitian mereka masing-masing.
