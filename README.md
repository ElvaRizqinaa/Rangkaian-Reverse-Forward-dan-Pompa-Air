# Sistem Kontrol Reverse-Forward & Pompa Air Otomatis

Repositori ini berisi materi, skema rangkaian, serta file simulasi **CADESIMU** untuk **Reverse Forward dan Pompa Air** pada mata kuliah Praktikum Mesin-Mesin Listrik. Fokus utama dari modul ini adalah perancangan rangkaian daya dan rangkaian kontrol untuk sistem kendali elektromagnetik serta otomatisasi dasar di industri.

---

## Daftar Materi

### 1. Sistem Kontrol Motor Reverse-Forward
Sistem kendali yang dirancang untuk mengatur putaran motor induksi 3 fasa agar dapat beroperasi ke dua arah yang berlawanan: maju (*Forward*) dan mundur (*Reverse*).
* **Aplikasi Industri:** Konveyor dua arah, *crane* / *hoist*, lift, dan mesin perkakas.
* **Prinsip Rangkaian Daya:** Mengubah arah putaran motor 3 fasa dengan cara menukar dua dari tiga fasa sumber tegangan (misal: fasa L1 dan L3 ditukar, sedangkan L2 tetap) menggunakan dua buah kontaktor utama (`KF` untuk *Forward* dan `KR` untuk *Reverse*).
* **Prinsip Rangkaian Kontrol & Sistem Pengaman:**
  * **Interlock (Saling Kunci):** Menggunakan kontak bantu *Normally Closed* (NC) dari masing-masing kontaktor yang dipasang secara bersilangan. Hal ini memastikan kontaktor `KF` dan `KR` tidak dapat aktif bersamaan untuk mencegah hubung singkat (korsleting) antar fasa.
  * **Proteksi Beban Lebih:** Dilengkapi dengan *Emergency Stop* (`EMS`) dan *Thermal Overload Relay* (`OL`) yang akan memutus arus kontrol secara otomatis serta menyalakan lampu indikator `TRIP` saat terjadi gangguan beban lebih.
  * **Indikator Visual:** Dilengkapi lampu indikator status operasional untuk kondisi `FOR` (Maju), `REV` (Mundur), `OFF` (Standby/Berhenti), dan `TRIP` (Gangguan).

### 2. Sistem Kontrol Pompa Air Otomatis
Sistem kendali otomatis untuk mengatur pengisian tangki/tandon air secara mandiri tanpa pengawasan manual berdasarkan level ketinggian air dan tekanan.
* **Prinsip Kerja Sistem:**
  * Menggunakan relai bantu (`R`) sebagai pengunci (*latching*) saat tombol `START` ditekan, sehingga sistem masuk ke dalam mode *standby* otomatis.
  * **Kondisi Mengisi (Pompa ON):** Ketika air berada di batas bawah, kontak sensor pelampung (`FLOAT`) dan sensor tekanan (`PRESS`) berada dalam posisi tertutup (*Normally Closed*), sehingga arus mengalir ke kontaktor utama (`K`) dan menyalakan motor pompa.
  * **Kondisi Penuh (Pompa OFF):** Ketika air mencapai batas maksimal di dalam tandon, sensor `FLOAT` atau `PRESS` akan terpicu (kontak terbuka), memutus aliran arus ke kontaktor `K`, dan menghentikan pompa secara otomatis agar air tidak meluap. Relai `R` tetap aktif menjaga mode otomatis hingga siklus pengisian berikutnya.
* **Sistem Keamanan:** Dilengkapi dengan tombol `STOP` untuk mematikan mode otomatis secara manual, tombol *Emergency* (`EMERG`), dan *Thermal Overload Relay* (`TOL`) untuk memproteksi motor pompa dari panas berlebih.

---

## Perangkat Lunak yang Digunakan
* **CADESIMU** — Digunakan untuk merancang skema kelistrikan (rangkaian daya & kontrol) serta melakukan simulasi aliran arus dan uji logika kontaktor secara *real-time*.

---

## Informasi Akademik

**Mata Kuliah:** Praktikum Mesin-Mesin Listrik  
**Dosen Pengampu:**
* Rofiq Cahyo Prayogo, S.T., M.T.
* Priyo Sasmoko, S.T., M.Eng.

**Disusun Oleh:**
* **Nama:** Elva Rizqina Khoirun Nisa
* **NIM:** 40040325650031
* **Program Studi:** Teknologi Rekayasa Otomasi
* **Departemen:** Teknologi Industri
* **Fakultas:** Sekolah Vokasi - Universitas Diponegoro
   git clone [https://github.com/ElvaRizqinaa/Dasar-Mesin-Mesin-Listrik.git](https://github.com/ElvaRizqinaa/Dasar-Mesin-Mesin-Listrik.git)
