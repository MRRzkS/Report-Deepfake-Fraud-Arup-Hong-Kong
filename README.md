# Hacking Reality: Kasus Penipuan *Deepfake* $25 Juta di Arup Hong Kong

> **Laporan Analisis Studi Kasus Kejahatan Siber Era *Generative AI***
> Analisis Tanggung Jawab Pengembang, Literasi Digital, dan Kerangka Deteksi

---

## 🎓 Identitas Laporan

| Keterangan | Detail |
|---|---|
| **Mata Kuliah** | Etika Profesi A |
| **Dosen Pengampu** | Adi Wahyu Pribadi, S.Si., M.Kom |
| **Kelompok** | Kelompok 11 |
| **Institusi** | Universitas Pancasila — Teknik Informatika |
| **Semester** | Genap 2025/2026 |

### 👥 Anggota Kelompok

| NPM | Nama |
|---|---|
| 4524210062 | Muhammad Fariz Fahreza |
| 4524210065 | Muhammad Fikri Ash Shiddiq |
| 4524210066 | Muhammad Hilmi |
| 4524210068 | Muhammad Rienchy Razak Simatupang |
| 4524210074 | Nafero Rafif Alhakim |

---

## 📑 Daftar Isi

1. [Pendahuluan — Penjelasan Studi Kasus](#1-pendahuluan--penjelasan-studi-kasus)
2. [Analisis 1 — Tanggung Jawab Pengembang *Tools Generative AI*](#2-analisis-1--tanggung-jawab-pengembang-tools-generative-ai)
3. [Analisis 2 — Edukasi Literasi Digital terkait *Generative AI*](#3-analisis-2--edukasi-literasi-digital-terkait-generative-ai)
4. [Analisis 3 — Kerangka Deteksi *Generative AI*](#4-analisis-3--kerangka-deteksi-generative-ai)
5. [Kesimpulan — Rangkuman](#5-kesimpulan--rangkuman)

---

# 1. Pendahuluan — Penjelasan Studi Kasus

## 1.1. Pengenalan Kasus

Kasus yang diangkat dalam laporan ini adalah insiden penipuan yang menimpa **Arup**, sebuah perusahaan konsultan teknik multinasional berbasis di Inggris, yang terjadi di kantor cabangnya di Hong Kong pada Februari 2024. Nilai kerugian yang tercatat adalah sebesar **HK$200 juta** atau setara dengan kurang lebih **US$25,6 juta**. Yang membuat kasus ini menarik untuk dibedah bukanlah besaran nominalnya semata, melainkan **cara** uang tersebut berpindah tangan — sebuah modus yang, menurut saya, menandai titik balik dalam sejarah kejahatan siber.

Sebagai mahasiswa Teknik Informatika, ketika pertama kali membaca kasus ini, saya berasumsi akan menemukan jejak eksploitasi teknis yang familiar: celah pada firewall, kerentanan *zero-day*, atau mungkin serangan ransomware. Namun asumsi itu keliru. Tidak ada sistem yang diretas dalam pengertian konvensional. Tidak ada *payload* berbahaya yang disuntikkan, tidak ada kredensial yang dicuri lewat *brute force*, dan tidak ada port yang dieksploitasi. Justru di sinilah letak kegelisahan akademis saya — karena jika tidak ada sistem yang dijebol, maka apa sebenarnya yang diretas?

Jawabannya, dan ini yang menjadi inti analisis saya di bagian ini, adalah **persepsi manusia itu sendiri**. Para penipu menggunakan teknologi *deepfake* — hasil dari *generative AI* — untuk mengkloning wajah dan suara sejumlah eksekutif Arup, termasuk CFO perusahaan, lalu menggelar sebuah rapat video palsu yang tampak sah secara total. Dalam konteks ini, judul laporan kami "**Hacking Reality**" terasa sangat tepat: yang diretas bukanlah mesin, melainkan **realitas** yang diterima oleh indra seorang karyawan.

## 1.2. Anatomi Perampokan Virtual: Bagaimana HK$200 Juta Lenyap Tanpa Sistem Diretas

Untuk memahami kompleksitas serangan ini, saya mencoba memecahnya menjadi empat fase yang saling berurutan. Pendekatan ini membantu saya melihat bahwa serangan tersebut bukan kejadian spontan, melainkan sebuah **operasi yang direncanakan dengan matang** dan sangat memahami psikologi korban.

### 1.2.1. Fase Pancingan (*Baiting*)

Serangan dimulai dengan email yang diterima seorang karyawan bagian keuangan di cabang Hong Kong. Email ini dibuat seolah-olah berasal dari **CFO Arup yang berbasis di Inggris**, dengan konten berupa permintaan transaksi yang bersifat rahasia.

Menurut analisis saya, fase ini adalah bentuk *spear phishing* klasik, namun ada satu detail yang layak dicermati: sang karyawan sebenarnya *sempat curiga* terhadap email tersebut. Dalam banyak kasus *phishing* tradisional, kecurigaan ini biasanya cukup untuk menggagalkan serangan. Tapi tidak di sini. Justru kecurigaan itu yang dimanfaatkan oleh para pelaku sebagai **umpan untuk fase berikutnya** — mereka tahu karyawan akan meminta verifikasi, dan mereka telah menyiapkan verifikasi palsu yang tampak lebih meyakinkan daripada email aslinya.

### 1.2.2. Fase Ilusi Realitas

Untuk "meyakinkan" karyawan yang ragu tadi, pelaku mengundangnya ke sebuah **panggilan video grup**. Di dalam panggilan tersebut, hadir CFO dan beberapa eksekutif senior lainnya — atau setidaknya, begitulah yang terlihat di layar. Wajah dan suara mereka **dipalsukan secara sempurna oleh AI**.

Ini adalah fase yang paling krusial dalam analisis saya. Karena secara psikologis, ketika seseorang meminta verifikasi, ekspektasi bawah sadarnya adalah bertemu dengan "realitas yang lebih tinggi" — misalnya suara langsung, atau lebih baik lagi, video langsung dengan wajah yang dikenal. Para pelaku memahami betul hierarki kepercayaan ini, lalu **membalikkannya menjadi senjata**. Karyawan yang tadinya curiga justru menjadi semakin yakin setelah melihat "wajah atasan" di layar, karena dalam benaknya, video *live* adalah bukti otentikasi yang jauh lebih kuat daripada teks.

### 1.2.3. Fase Eksekusi

Dengan keraguan yang telah terkikis habis, karyawan tersebut kemudian mengeksekusi instruksi yang diberikan dalam rapat palsu itu. Tercatat ada **15 transaksi finansial ke 5 rekening milik pelaku**, dengan total nilai HK$200 juta.

Apa yang menarik perhatian saya di fase ini adalah **struktur transaksinya**. Angka 15 transaksi ke 5 rekening menurut saya bukan kebetulan — ini mengindikasikan pelaku sudah merancang pola *layering* dana sejak awal, kemungkinan untuk mempersulit pelacakan dan mengaburkan jejak uang setelah dana masuk. Artinya, lapisan kejahatannya bukan hanya penipuan berbasis AI, tapi juga disertai strategi pencucian uang yang terstruktur.

### 1.2.4. Fase Sadar Tertipu

Yang paling ironis, menurut pandangan saya, adalah bahwa penipuan ini **baru disadari beberapa hari kemudian**, ketika karyawan tersebut melakukan konfirmasi langsung ke kantor pusat. Jeda waktu ini adalah celah kritis yang menunjukkan satu hal: **prosedur verifikasi internal Arup saat itu tidak dirancang untuk menghadapi ancaman berbasis media sintetis**.

Bagi saya, jeda beberapa hari sebelum penipuan disadari adalah pelajaran terpenting dari fase ini. Di dunia siber tradisional, deteksi intrusi bisa berjalan dalam hitungan detik karena ada *log*, *alert*, dan *anomaly detection*. Tapi dalam serangan rekayasa sosial berbasis AI, tidak ada *log* yang bisa dibaca — karena yang "diretas" adalah keputusan manusia, dan keputusan manusia tidak mencatat dirinya sendiri.

## 1.3. Pergeseran Ancaman: Meretas Manusia, Bukan Mesin

Bagian ini adalah inti dari argumen yang ingin saya sampaikan sebagai penulis: bahwa kasus Arup menandai **pergeseran paradigma** dalam dunia keamanan siber. Untuk memperjelas pergeseran ini, saya menyusun perbandingan antara serangan siber tradisional dengan pendekatan *social engineering via AI* seperti yang dialami Arup.

### 1.3.1. Tabel Komparasi Paradigma Ancaman

| Aspek | Serangan Siber Tradisional | *Social Engineering via* AI |
|---|---|---|
| **Target Utama** | Jaringan komputer, *password*, dan *server* data | Psikologi, kepercayaan, dan persepsi visual manusia |
| **Senjata Serangan** | *Malware*, *ransomware*, dan injeksi kode berbahaya | Manipulasi realitas (kloning suara & video *deepfake*) |
| **Status Sistem Internal** | *Firewall* dan keamanan perimeter berhasil dijebol | Sistem keamanan 100% aman dan sama sekali tidak tersentuh |

### 1.3.2. Analisis Pergeseran

Membaca tabel di atas, saya menarik beberapa kesimpulan yang cukup mengusik pemahaman saya sebelumnya tentang keamanan siber:

**Pertama**, paradigma pertahanan tradisional menjadi kurang relevan bila diterapkan sendirian. Selama ini, perusahaan banyak berinvestasi pada *firewall*, sistem deteksi intrusi, enkripsi, dan *endpoint protection*. Semua itu penting, tapi dalam kasus Arup, **semua sistem itu bekerja dengan sempurna** — dan perusahaan tetap kehilangan HK$200 juta. Ini menurut saya adalah paradoks yang harus dijawab oleh industri keamanan siber: bagaimana mempertahankan sesuatu yang tidak pernah diserang?

**Kedua**, vektor serangan telah berpindah dari **lapisan teknis** ke **lapisan kognitif**. Jika dulu seorang *attacker* harus memiliki kemampuan pemrograman tinggi untuk mengeksploitasi kerentanan sistem, hari ini ia cukup memiliki akses ke *tools generative AI* yang tersedia bebas di internet, ditambah kemampuan menyusun skenario sosial yang meyakinkan. Barrier teknis kejahatan siber menurun, sementara *damage potential*-nya meningkat drastis.

**Ketiga**, dan ini yang paling penting menurut saya, **"sistem keamanan" perlu diredefinisikan**. Keamanan siber modern tidak bisa lagi didefinisikan sebatas integritas infrastruktur teknis. Ia harus mencakup **integritas informasi yang masuk ke indra karyawan** — artinya, pertahanan harus dirancang untuk mengasumsikan bahwa apa yang dilihat dan didengar dalam rapat virtual **mungkin saja palsu**.

### 1.3.3. Kutipan Reflektif

Untuk menutup bagian ini, kelompok kami memilih kutipan dari **Rob Greig, CIO Arup**, yang menurut saya merangkum seluruh pergeseran paradigma ini dalam satu kalimat:

> *"Penipu tidak perlu merusak tembok keamanan perusahaan jika mereka bisa meyakinkan karyawan untuk membukakan pintunya."*
> — **Rob Greig, CIO Arup**

Kutipan ini, bagi saya pribadi, terasa seperti peringatan yang jauh melampaui kasus Arup sendiri. Ia berlaku untuk setiap organisasi yang masih percaya bahwa investasi keamanan siber cukup berhenti di lapisan perimeter teknis.

## 1.4. Ringkasan Bagian Pendahuluan

Kasus penipuan *deepfake* Arup bukanlah sekadar "kasus besar" karena nominalnya, melainkan **kasus penting** karena menjadi bukti empiris pertama dalam skala korporasi besar bahwa *generative AI* telah mengubah **definisi dasar dari apa yang disebut "peretasan"**. Bagian pendahuluan ini berfungsi sebagai fondasi konseptual untuk tiga analisis berikutnya — mulai dari **tanggung jawab pengembang AI di hulu**, **edukasi literasi digital di sisi pengguna**, hingga **kerangka deteksi teknis** yang dapat diterapkan sebagai pertahanan.

---

# 2. Analisis 1 — Tanggung Jawab Pengembang *Tools Generative AI*

> **Penulis Bagian**: *(diisi oleh penulis bagian ini — NPM & Nama)*
> **Cakupan Slide**: Slide 4 (*Analisis Hulu: Beban Moral Pembuat AI Generatif*)

## 2.1. Pengantar Analisis

> 📝 **PLACEHOLDER — Silakan diisi**
>
> Bagian ini membahas **dari sudut pandang hulu**: siapa yang harus bertanggung jawab ketika teknologi *generative AI* disalahgunakan? Mulailah dengan paragraf pembuka yang menjelaskan mengapa pencegahan harus dimulai dari tingkat **kode dan etika pengembang teknologi**, bukan dari sisi pengguna.
>
> *Gaya penulisan: tulis seperti pendapat/analisis mahasiswa langsung (gunakan kata "saya", "menurut analisis saya", "bagi saya pribadi", dsb.).*

## 2.2. Empat Pilar Tanggung Jawab Pengembang

Berdasarkan slide presentasi kami, ada empat pilar utama yang menjadi **beban moral** bagi para pengembang *tools generative AI*.

### 2.2.1. *Ethics by Design*

> 📝 **PLACEHOLDER — Silakan diisi**
>
> Poin inti: *Guardrails* (batasan keamanan) wajib ditanamkan di dalam kode dasar. Teknologi dilarang rilis tanpa filter pencegah peniruan identitas.
>
> **Yang bisa dianalisis di sini:**
> - Apa artinya "*ethics by design*" dalam konteks pengembangan model AI generatif?
> - Contoh konkret *guardrails* yang sudah diterapkan di industri (misal: content filter OpenAI, voice cloning consent pada ElevenLabs).
> - Apa yang menurut Anda kurang, dan bagaimana seharusnya?

### 2.2.2. Kendali Akses Ketat

> 📝 **PLACEHOLDER — Silakan diisi**
>
> Poin inti: Akses ke model AI berkualitas tinggi harus dibatasi secara ketat agar tidak jatuh ke tangan sindikat kriminal terorganisir.
>
> **Yang bisa dianalisis di sini:**
> - Dilema antara *open source* vs *closed source* model AI.
> - Kasus model yang bocor (misal: LLaMA weights leak, Stable Diffusion untuk *deepfake*).
> - Bagaimana menyeimbangkan demokratisasi AI dengan pencegahan penyalahgunaan.

### 2.2.3. Sistem *Watermarking*

> 📝 **PLACEHOLDER — Silakan diisi**
>
> Poin inti: Pengembang wajib menyisipkan tanda air digital (*digital watermark*) permanen yang menandai secara transparan bahwa konten tersebut adalah buatan AI.
>
> **Yang bisa dianalisis di sini:**
> - Bagaimana watermarking bekerja secara teknis (misal: SynthID dari Google DeepMind, C2PA standard).
> - Tantangan teknis: watermark bisa dihapus atau rusak saat kompresi/editing.
> - Apakah watermarking wajib diatur dalam regulasi pemerintah?

### 2.2.4. Prinsip *Do No Harm*

> 📝 **PLACEHOLDER — Silakan diisi**
>
> Poin inti: Inovasi tidak boleh mengorbankan keamanan publik. Pengembang wajib menciptakan alat pendeteksi yang setara dengan kecanggihan AI ciptaannya.
>
> **Yang bisa dianalisis di sini:**
> - Analogi dengan prinsip *Hippocratic Oath* di dunia kedokteran.
> - Apakah wajar kalau pengembang AI generatif juga wajib merilis alat deteksinya?
> - Bagaimana kasus Arup menunjukkan bahwa asimetri antara AI *generator* dan AI *detector* menjadi masalah serius?

## 2.3. Refleksi dan Keterkaitan dengan Kasus Arup

> 📝 **PLACEHOLDER — Silakan diisi**
>
> Tulis 2–3 paragraf yang mengaitkan keempat pilar di atas secara spesifik dengan kasus Arup. Pertanyaan pemantik:
> - Jika empat pilar ini sudah diterapkan sejak awal, apakah kasus Arup bisa dicegah?
> - Siapa yang paling bertanggung jawab secara moral: pengembang, regulator, atau pengguna?
> - Apa pelajaran yang bisa diambil untuk industri AI di Indonesia?

---

# 3. Analisis 2 — Edukasi Literasi Digital terkait *Generative AI*

> **Penulis Bagian**: *(diisi oleh penulis bagian ini — NPM & Nama)*
> **Cakupan Slide**: *(sesuaikan dengan slide terkait, kemungkinan Slide 5–6)*

## 3.1. Pengantar Analisis

> 📝 **PLACEHOLDER — Silakan diisi**
>
> Bagian ini membahas **sisi pengguna / korban**: bagaimana edukasi literasi digital dapat menjadi benteng pertahanan paling fundamental terhadap serangan berbasis *generative AI*. Mulailah dengan mengapa pelatihan keamanan siber konvensional **tidak cukup lagi** di era sekarang.
>
> *Gaya penulisan: tulis seperti pendapat/analisis mahasiswa langsung agar konsisten dengan bagian sebelumnya.*

## 3.2. Pokok Bahasan Edukasi Literasi Digital

> 📝 **PLACEHOLDER — Silakan isi sub-poin sesuai slide kelompok**
>
> Contoh sub-bahasan yang bisa dikembangkan (silakan sesuaikan dengan slide asli):

### 3.2.1. *(Sub-judul sesuai slide)*

> 📝 **PLACEHOLDER** — Uraikan isi sub-poin ini dengan gaya analisis mahasiswa.
> Misalnya bisa tentang: **Kesadaran akan ancaman *deepfake***, pengenalan ciri-ciri video/suara sintetis, atau contoh latihan simulasi *phishing* modern.

### 3.2.2. *(Sub-judul sesuai slide)*

> 📝 **PLACEHOLDER** — Uraikan isi sub-poin ini dengan gaya analisis mahasiswa.
> Misalnya bisa tentang: **Protokol verifikasi berlapis** (*multi-channel verification*), aturan "jangan pernah mentransfer dana hanya berdasarkan instruksi video call", atau budaya "*trust but verify*" di lingkungan kerja.

### 3.2.3. *(Sub-judul sesuai slide)*

> 📝 **PLACEHOLDER** — Uraikan isi sub-poin ini dengan gaya analisis mahasiswa.
> Misalnya bisa tentang: **Peran institusi pendidikan** dalam mengintegrasikan literasi AI ke kurikulum, atau **tanggung jawab perusahaan** dalam rutinitas pelatihan karyawan.

## 3.3. Refleksi dan Keterkaitan dengan Kasus Arup

> 📝 **PLACEHOLDER — Silakan diisi**
>
> Tulis 2–3 paragraf refleksi. Pertanyaan pemantik:
> - Seandainya karyawan Arup sudah dilatih untuk mengenali *deepfake*, apakah ia akan tetap tertipu?
> - Apa bentuk literasi digital yang paling efektif: pelatihan formal, simulasi, atau budaya organisasi?
> - Bagaimana kondisi literasi digital di Indonesia saat ini, dan apa yang perlu diperbaiki?

---

# 4. Analisis 3 — Kerangka Deteksi *Generative AI*

> **Penulis Bagian**: *(diisi oleh penulis bagian ini — NPM & Nama)*
> **Cakupan Slide**: *(sesuaikan dengan slide terkait, kemungkinan Slide 7–8)*

## 4.1. Pengantar Analisis

> 📝 **PLACEHOLDER — Silakan diisi**
>
> Bagian ini membahas **sisi teknis pertahanan**: bagaimana teknologi dapat digunakan untuk mendeteksi konten sintetis buatan *generative AI*. Mulailah dengan menjelaskan mengapa pendekatan deteksi teknis **harus melengkapi** dua pendekatan sebelumnya (tanggung jawab pengembang + literasi digital).
>
> *Gaya penulisan: tulis seperti pendapat/analisis mahasiswa langsung, dengan sedikit kedalaman teknis karena penulis adalah mahasiswa Teknik Informatika.*

## 4.2. Komponen Kerangka Deteksi

> 📝 **PLACEHOLDER — Silakan isi sub-poin sesuai slide kelompok**

### 4.2.1. *(Sub-judul sesuai slide)*

> 📝 **PLACEHOLDER** — Uraikan isi sub-poin ini dengan gaya analisis mahasiswa.
> Contoh arah pembahasan:
> - **Deteksi berbasis AI** (menggunakan model klasifikasi untuk membedakan konten asli vs sintetis).
> - **Analisis forensik** pada artefak visual/audio (misal: inkonsistensi pencahayaan, *lip-sync mismatch*, pola pernapasan).
> - Model deteksi yang sudah tersedia: Microsoft Video Authenticator, Intel FakeCatcher, dsb.

### 4.2.2. *(Sub-judul sesuai slide)*

> 📝 **PLACEHOLDER** — Uraikan isi sub-poin ini dengan gaya analisis mahasiswa.
> Contoh arah pembahasan:
> - **Verifikasi berbasis identitas kriptografis** (*digital signature*, *C2PA content credentials*).
> - **Protokol *liveness detection*** untuk video call perusahaan.
> - Penerapan *zero-trust* pada komunikasi internal.

### 4.2.3. *(Sub-judul sesuai slide)*

> 📝 **PLACEHOLDER** — Uraikan isi sub-poin ini dengan gaya analisis mahasiswa.
> Contoh arah pembahasan:
> - **Kolaborasi lintas-sektor** (pemerintah + industri + akademisi).
> - **Regulasi** pendukung (misal: EU AI Act, UU PDP di Indonesia).
> - Roadmap implementasi di level organisasi.

## 4.3. Refleksi dan Keterkaitan dengan Kasus Arup

> 📝 **PLACEHOLDER — Silakan diisi**
>
> Tulis 2–3 paragraf refleksi. Pertanyaan pemantik:
> - Kerangka deteksi mana yang **paling realistis** diterapkan oleh perusahaan skala Arup?
> - Mengapa bahkan dengan teknologi deteksi, kasus seperti Arup tetap bisa terjadi?
> - Bagaimana peran mahasiswa informatika dalam mengembangkan alat deteksi *deepfake* di masa depan?

---

# 5. Kesimpulan — Rangkuman

> **Penulis Bagian**: *(diisi oleh penulis bagian ini — NPM & Nama)*
> **Cakupan Slide**: Slide 9 (Kesimpulan/Penutup)

## 5.1. Rangkuman Temuan

> 📝 **PLACEHOLDER — Silakan diisi**
>
> Rangkum **inti dari keempat bagian sebelumnya** dalam 3–4 paragraf padat. Struktur yang disarankan:
>
> 1. **Paragraf 1** — Rekap studi kasus Arup: apa yang terjadi, nilai kerugian, dan mengapa kasus ini signifikan.
> 2. **Paragraf 2** — Rangkuman tiga analisis: tanggung jawab pengembang (hulu), literasi digital (tengah), dan kerangka deteksi (teknis).
> 3. **Paragraf 3** — Benang merah ketiganya: mengapa pendekatan berlapis (*defense in depth*) adalah satu-satunya cara menghadapi ancaman AI generatif.

## 5.2. Pelajaran Kunci

> 📝 **PLACEHOLDER — Silakan diisi**
>
> Sajikan 3–5 pelajaran kunci (*key takeaways*) dalam bentuk daftar. Contoh format:
>
> 1. **Pergeseran vektor serangan** — dari mesin ke manusia, menuntut redefinisi "keamanan siber".
> 2. **Tanggung jawab berlapis** — pengembang, perusahaan, dan pengguna sama-sama punya peran.
> 3. **(diisi)**
> 4. **(diisi)**

## 5.3. Rekomendasi dan Penutup

> 📝 **PLACEHOLDER — Silakan diisi**
>
> Tulis rekomendasi konkret (untuk industri, pemerintah, institusi pendidikan, dan/atau mahasiswa), lalu tutup dengan paragraf penutup yang merefleksikan **posisi Anda sebagai calon profesional informatika** dalam menghadapi era *generative AI*.
