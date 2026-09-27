# KUIS PERSIAPAN UTS
## Mata Kuliah Web Service

**Bentuk:** Esai  
**Jumlah soal:** 5 soal  
**Sifat:** Individu  
**Materi:** Pertemuan 1–7

---

## Petunjuk

1. Jawablah seluruh soal secara argumentatif dan sistematis.
2. Gunakan konsep Web Service yang telah dibahas pada pertemuan 1–7.
3. Untuk soal studi kasus, jawaban tidak hanya dinilai dari pilihan teknologi, tetapi terutama dari alasan dan analisis yang mendasarinya.
4. Gunakan diagram sederhana jika diperlukan untuk menjelaskan rancangan arsitektur.
5. Hindari jawaban yang hanya berupa definisi atau daftar istilah.

---

## Soal 1 — Evolusi Arsitektur dan Distributed System

Sebuah perusahaan awalnya membangun aplikasi penjualan dalam bentuk **monolith**. Setelah jumlah pengguna meningkat, aplikasi tersebut dikembangkan dengan menambahkan modul pembayaran, inventori, pelanggan, dan pengiriman.

Setelah beberapa tahun muncul permasalahan:

- perubahan pada satu modul sering berdampak pada modul lain;
- deployment harus dilakukan terhadap seluruh aplikasi;
- beberapa fungsi membutuhkan waktu respons yang berbeda;
- kegagalan pada salah satu bagian dapat memengaruhi layanan lainnya.

### Pertanyaan

a. Jelaskan mengapa karakteristik arsitektur monolith dapat menimbulkan permasalahan tersebut ketika sistem berkembang.

b. Jelaskan bagaimana pendekatan **distributed system** dapat digunakan untuk mengatasi sebagian permasalahan tersebut.

c. Dalam rancangan distributed system, jelaskan bagaimana **latency, consistency, dan fault tolerance** dapat memengaruhi keputusan desain.

d. Menurut Anda, apakah memecah monolith menjadi beberapa service secara otomatis menyelesaikan seluruh permasalahan? Jelaskan alasan Anda.

---

## Soal 2 — SOAP dan Contract-First

Sebuah perusahaan memiliki sistem **Human Resource** yang harus digunakan oleh beberapa aplikasi internal yang dikembangkan oleh tim berbeda. Perusahaan menginginkan adanya kontrak layanan yang jelas sehingga setiap tim mengetahui operasi dan struktur data yang disediakan oleh service.

Tim pengembang mempertimbangkan penggunaan **SOAP dan WSDL**.

### Pertanyaan

a. Jelaskan bagaimana **WSDL berperan sebagai contract** dalam arsitektur SOAP.

b. Jelaskan keuntungan dan konsekuensi pendekatan **contract-first** bagi client dan service.

c. Bandingkan pendekatan tersebut dengan cara REST API pada umumnya mendefinisikan dan mendokumentasikan kontraknya.

d. Jelaskan kondisi atau karakteristik kebutuhan sistem yang dapat membuat SOAP tetap relevan meskipun REST banyak digunakan dalam pengembangan Web Service modern.

---

## Soal 3 — Analisis REST, Richardson Maturity Model, dan HATEOAS

Sebuah tim pengembang membuat API untuk sistem perpustakaan dengan beberapa endpoint berikut:

- `/books`
- `/books/123`
- `/members/10`
- `/members/10/loans`

Client dapat melakukan operasi untuk mengambil, menambah, mengubah, dan menghapus data menggunakan HTTP method.

Namun, response dari API hanya berisi data dan tidak memberikan informasi mengenai resource atau tindakan lain yang dapat dilakukan client.

### Pertanyaan

a. Analisis sejauh mana rancangan API tersebut menerapkan prinsip REST berdasarkan **Richardson Maturity Model**.

b. Jelaskan bagaimana penggunaan HTTP method dan resource dapat memengaruhi tingkat kematangan REST API tersebut.

c. Jelaskan konsep **HATEOAS** dan bagaimana penerapannya dapat mengubah cara client berinteraksi dengan API.

d. Berikan contoh sederhana response yang menunjukkan bagaimana HATEOAS dapat diterapkan pada kasus peminjaman buku.

---

## Soal 4 — Studi Kasus GraphQL

Sebuah universitas memiliki aplikasi akademik yang digunakan melalui website dan aplikasi mobile.

Halaman dashboard mahasiswa membutuhkan:

- nama mahasiswa;
- program studi;
- tiga mata kuliah yang sedang ditempuh;
- nilai terakhir;
- jumlah SKS;
- jadwal kuliah hari tersebut.

Permasalahan yang muncul adalah kebutuhan website dan mobile berbeda. Website membutuhkan data yang lebih lengkap, sedangkan aplikasi mobile hanya membutuhkan sebagian data.

Tim pengembang mempertimbangkan **GraphQL**.

### Pertanyaan

a. Identifikasi permasalahan yang mungkin terjadi jika seluruh kebutuhan tersebut dilayani menggunakan API REST dengan response yang sama untuk semua client.

b. Jelaskan bagaimana konsep **schema, query, dan resolver** pada GraphQL dapat digunakan untuk menangani kebutuhan tersebut.

c. Buat contoh rancangan query GraphQL untuk kebutuhan dashboard mahasiswa. Tidak perlu membuat implementasi resolver.

d. Jelaskan minimal **dua trade-off** yang perlu dipertimbangkan jika universitas memilih GraphQL.

---

## Soal 5 — Studi Kasus Pemilihan Arsitektur

Sebuah perusahaan teknologi sedang membangun platform yang terdiri dari beberapa komponen:

1. **Website pelanggan** membutuhkan API untuk mengakses produk dan pesanan.
2. **Aplikasi mobile** sering membutuhkan kombinasi data yang berbeda untuk setiap halaman.
3. **Service pembayaran** harus berkomunikasi dengan service lain menggunakan komunikasi internal yang terstruktur.
4. Perusahaan masih memiliki **sistem legacy** yang hanya menyediakan layanan melalui SOAP.
5. Tim pengembang ingin setiap service dapat dikembangkan secara independen.

Pilihan teknologi yang sedang dipertimbangkan adalah:

- SOAP
- REST
- GraphQL
- gRPC

### Pertanyaan

a. Analisis karakteristik kebutuhan dari keempat jenis komunikasi tersebut.

b. Tentukan pendekatan Web Service yang Anda gunakan untuk masing-masing kebutuhan dan jelaskan **alasan teknisnya**.

c. Jelaskan mengapa memilih satu teknologi yang sama untuk seluruh komunikasi belum tentu menjadi solusi yang tepat.

d. Gambarkan rancangan arsitektur sederhana yang menunjukkan hubungan antara **client, service, dan pendekatan komunikasi** yang Anda pilih.

e. Jelaskan minimal **tiga trade-off arsitektur** yang muncul dari keputusan Anda.

---

# Fokus Penilaian

Dalam mengerjakan kuis ini, perhatikan bahwa jawaban yang baik harus menunjukkan:

| Aspek | Yang Diharapkan |
|---|---|
| Pemahaman konsep | Mampu menjelaskan konsep dengan istilah yang tepat |
| Analisis | Mampu menghubungkan konsep dengan permasalahan |
| Pemilihan teknologi | Mampu memberikan alasan berdasarkan kebutuhan |
| Perbandingan | Mampu menjelaskan perbedaan dan konsekuensi pendekatan |
| Arsitektur | Mampu menggambarkan hubungan antar komponen |
| Trade-off | Mampu menjelaskan keuntungan dan konsekuensi keputusan |
| Argumentasi | Tidak sekadar menyebutkan teknologi atau definisi |

---

## Hubungan dengan UTS

Kuis ini dirancang sebagai **simulasi persiapan UTS**.

Pola kemampuan yang dilatih sama dengan UTS:

- **Soal 1:** analisis konsep arsitektur dan distributed system.
- **Soal 2:** analisis SOAP, WSDL, dan contract-first.
- **Soal 3:** analisis REST, Richardson Maturity Model, dan HATEOAS.
- **Soal 4:** penerapan GraphQL pada studi kasus.
- **Soal 5:** pemilihan dan perancangan arsitektur Web Service.

Namun, **kasus dan pertanyaan berbeda dengan soal UTS**, sehingga mahasiswa tidak cukup hanya menghafalkan jawaban UTS.
