# Gree® Labs

Portal warta digital, dokumentasi rekayasa tata udara, dan edukasi teknologi pendingin Gree Indonesia. Dibangun menggunakan **Hugo** dengan modifikasi tema minimalis **Bear Blog**, mengutamakan performa pemuatan instan tanpa dependensi pustaka JavaScript berat.

Situs live: **[greelabs.pages.dev](https://greelabs.pages.dev)**

---

## ⚡ Karakteristik & Arsitektur

* **Performa Edge**: Bobot halaman di bawah 40 KB, terdistribusi melalui jaringan global Cloudflare Pages.
* **Tipografi Presisi**: Menggunakan font `Inter` untuk naskah warta panjang dan `IBM Plex Mono` untuk spesifikasi teknis mesin (BTU/h, Watt, kode error).
* **Pola Selective Override**: Folder `layouts/` root hanya menimpa file yang dimodifikasi (`custom_head.html`, `footer.html`, `post_navigator.html`, `style.html`) tanpa memutus sinkronisasi modul tema.
* **Navigasi Bersih**: Menu atas ringkas satu kata (`Beranda`, `Berita`, `Tentang`, `Kontak`) serta navigasi linear *Prev / Next* di setiap kaki artikel.

---

## 📂 Struktur Kanal Warta (`/blog/`)

Mengadopsi taksonomi dan arsitektur publikasi warta resmi `gree.id/news`:

| Kanal | Cakupan Konten & Topik |
| :--- | :--- |
| **Article** | Edukasi teknis instalasi (SOP vakum R32, ketebalan pipa, aturan 3 meter), kalkulasi BTU/h beban pendinginan, arsitektur multi-split *Free Match*, dan diagnosa kode error mandiri. |
| **Event** | Siaran pers produk flagship (Airy AI Inverter, F5S), pameran industri (RHVAC, IndoBuildTech), peresmian jaringan Gree Proshop, sertifikasi teknisi nasional, dan CSR vokasi HVAC. |
| **Promotion** | Standar kebijakan Garansi Platinum 1+5+10 dan program subsidi tukar tambah (*trade-in*) unit hemat energi. |

---

## 🛠️ Struktur Repositori

```text
├── content/
│   ├── blog/              # Berkas warta Markdown (Article, Event, Promotion)
│   ├── _index.md          # Laman beranda
│   ├── kontak.md          # Informasi narahubung resmi
│   └── tentang-kami.md    # Profil Gree® Labs
├── layouts/
│   ├── _default/          # Template single artikel
│   └── partials/          # Selective override (post_navigator, style, dll.)
├── themes/hugo-bearblog/  # Sub
