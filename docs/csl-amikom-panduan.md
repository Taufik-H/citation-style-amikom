# Panduan Instalasi & Penjelasan Detail CSL Amikom

## Instalasi Style CSL

1. **Download** file `citation-style-skripsi-amikom-purwokerto.csl` dari repositori ini.
2. **Zotero**: Edit > Preferences > Cite > Styles > Add Style > pilih file CSL.
3. **Mendeley**: View > Citation Style > More Styles... > Add > pilih file CSL.
4. Pilih style "Universitas Amikom Purwokerto - (Skripsi)" saat membuat sitasi/daftar pustaka.

## Penjelasan Struktur & Fungsi Tag/Atribut

- `<macro>`: Blok fungsi reusable, misal format penulis, judul, dsb.
- `<text variable="...">`: Menampilkan data dari metadata (misal title, author, container-title).
- `text-case="title"`: Mengubah output menjadi Title Case.
- `<names>`: Menampilkan daftar nama (penulis, editor, dll).
- `<group>`: Mengelompokkan beberapa elemen dengan delimiter.
- `<choose>`, `<if>`, `<else-if>`, `<else>`: Logika percabangan.
- `<bibliography>`, `<citation>`: Blok utama output daftar pustaka & sitasi.
- `type=...`: Menentukan tipe sumber (book, article-journal, dll).
- `<date>`: Format tanggal.
- `<label>`: Label tambahan (misal "ed.", "trans.").
- `<sort>`: Urutan daftar pustaka.

### Cara Kerja

- CSL membaca metadata dari aplikasi referensi.
- Macro/tag menentukan format output sesuai tipe sumber.
- Percabangan `<choose>` menyesuaikan format tiap jenis sumber.
- Atribut seperti `text-case`, `font-style`, dsb, mengatur tampilan.

---

**Tips:**

- Edit metadata di aplikasi referensi untuk hasil terbaik.
- Lihat komentar di file CSL untuk penjelasan tiap blok.
