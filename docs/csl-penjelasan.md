# Penjelasan Struktur dan Fungsi CSL (Citation Style Language)

Dokumen ini menjelaskan elemen-elemen utama dalam file CSL, khususnya untuk style skripsi Amikom Purwokerto.

---

## 1. Tag Utama CSL

- `<style>`: Tag utama yang membungkus seluruh file CSL.
- `<info>`: Metadata style (judul, penulis, lisensi, dsb).
- `<locale>`: Definisi istilah lokal (misal: "dan", "dkk.").
- `<macro>`: Fungsi/makro yang dapat dipanggil berulang di bagian lain.
- `<citation>`: Aturan format sitasi dalam teks.
- `<bibliography>`: Aturan format daftar pustaka.

---

## 2. Type (Tipe Sumber)

- `article-journal`: Artikel jurnal ilmiah.
- `book`: Buku.
- `paper-conference`: Prosiding/Conference paper.
- `webpage`, `post-weblog`: Sumber dari web/blog.
- `generic`: Tipe umum jika tidak dikategorikan.
- Tipe lain: `thesis`, `report`, `chapter`, dll.

---

## 3. Macro (Makro)

Makro adalah blok reusable untuk format tertentu, misal:

- `author`: Format nama penulis.
- `issued`: Format tahun terbit.
- `title`: Format judul.
- `container`: Info sumber induk (jurnal, buku, dsb).
- `access`: Format akses (URL, DOI, tanggal akses).
- `locators`: Info volume, nomor, halaman.
- `publisher`: Format penerbit.

Makro dipanggil dengan `<text macro="nama-makro"/>`.

---

## 4. Fungsi & Atribut Penting

- `text-case="title"`: Judul otomatis Title Case (jika metadata mendukung).
- `font-style="italic"`: Huruf miring.
- `delimiter=", "`: Pemisah antar elemen.
- `et-al-min`, `et-al-use-first`: Aturan "dkk." jika penulis banyak.
- `and="symbol"`/`and="text"`: Format penghubung antar penulis ("dan", "&").
- `match="any"/"none"`: Logika pemilihan tipe.
- `prefix`, `suffix`: Tambahan karakter sebelum/sesudah elemen.

---

## 5. Contoh Penggunaan

```xml
<macro name="author">
  <names variable="author" delimiter=", ">
    <name and="text" et-al-min="3" et-al-use-first="1"/>
  </names>
</macro>
```

---

## 6. Tips

- Edit metadata di reference manager agar hasil sesuai.
- Gunakan tipe sumber yang tepat (journal, book, dll).
- Makro bisa dimodifikasi sesuai kebutuhan kampus.

---

Dokumentasi ini dapat dikembangkan sesuai kebutuhan.
