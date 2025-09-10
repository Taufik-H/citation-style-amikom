# CSL Utilities & Referensi Lengkap

Dokumentasi ini merangkum seluruh tag, atribut, utilitas, dan fitur penting dalam Citation Style Language (CSL), lengkap dengan penjelasan, contoh penggunaan, dan contoh output.

---

## 1. Daftar Tag Utama CSL

| Tag                           | Fungsi                                                        | Contoh Penggunaan                         |
| ----------------------------- | ------------------------------------------------------------- | ----------------------------------------- |
| `<style>`                     | Tag utama, membungkus seluruh file CSL                        | `<style ...> ... </style>`                |
| `<info>`                      | Metadata style: judul, penulis, lisensi, dsb                  | `<info> ... </info>`                      |
| `<locale>`                    | Definisi istilah lokal (misal: "dan", "dkk.")                 | `<locale xml:lang="id"> ... </locale>`    |
| `<macro>`                     | Blok fungsi/makro reusable untuk format tertentu              | `<macro name="author"> ... </macro>`      |
| `<citation>`                  | Aturan format sitasi dalam teks                               | `<citation> ... </citation>`              |
| `<bibliography>`              | Aturan format daftar pustaka                                  | `<bibliography> ... </bibliography>`      |
| `<choose>`                    | Logika pemilihan (if/else) untuk kondisi tertentu             | `<choose> ... </choose>`                  |
| `<if>`, `<else-if>`, `<else>` | Kondisi logika di dalam `<choose>`                            | `<if type="book"> ... </if>`              |
| `<group>`                     | Mengelompokkan beberapa elemen dengan delimiter/prefix/suffix | `<group delimiter=", "> ... </group>`     |
| `<names>`, `<name>`           | Format nama penulis/editor                                    | `<names variable="author"> ... </names>`  |
| `<text>`                      | Menampilkan variabel, makro, atau teks statis                 | `<text variable="title"/>`                |
| `<date>`                      | Format tanggal (tahun, bulan, hari)                           | `<date variable="issued"> ... </date>`    |
| `<number>`                    | Format angka (misal: edisi, volume)                           | `<number variable="edition"/>`            |
| `<label>`                     | Menampilkan label (misal: "ed.", "vol.")                      | `<label variable="editor" form="short"/>` |
| `<sort>`                      | Urutan daftar pustaka/sitasi                                  | `<sort> ... </sort>`                      |
| `<key>`                       | Kunci pengurutan dalam `<sort>`                               | `<key macro="author"/>`                   |
| `<substitute>`                | Pengganti jika variabel utama kosong                          | `<substitute> ... </substitute>`          |
| `<term>`                      | Menampilkan istilah dari locale                               | `<term name="and"/>`                      |

---

## 2. Daftar Atribut Tag & Penjelasan

| Atribut                       | Tag yang Umum Digunakan | Penjelasan & Contoh                                                                       |
| ----------------------------- | ----------------------- | ----------------------------------------------------------------------------------------- |
| variable                      | text, names, date       | Nama field dari metadata (author, title, year, URL, DOI, dsb). Contoh: `variable="title"` |
| macro                         | text                    | Memanggil makro lain. Contoh: `macro="author"`                                            |
| delimiter                     | group, names            | Pemisah antar elemen. Contoh: `delimiter=", "`                                            |
| prefix/suffix                 | text, group, names      | Tambahan karakter sebelum/sesudah elemen. Contoh: `prefix=" (" suffix=")"`                |
| font-style                    | text                    | "italic", "bold", "normal". Contoh: `font-style="italic"`                                 |
| text-case                     | text                    | "title", "sentence", "lowercase", "uppercase". Contoh: `text-case="title"`                |
| and                           | names, name             | "text" ("dan"), "symbol" ("&"). Contoh: `and="symbol"`                                    |
| et-al-min                     | names, name             | Jumlah minimal penulis untuk "dkk.". Contoh: `et-al-min="3"`                              |
| et-al-use-first               | names, name             | Jumlah penulis yang ditampilkan sebelum "dkk.". Contoh: `et-al-use-first="1"`             |
| name-as-sort-order            | name                    | "all" (Nama dibalik: "Santoso, A. B."). Contoh: `name-as-sort-order="all"`                |
| form                          | name, label             | "short", "long". Contoh: `form="short"`                                                   |
| match                         | if, else-if             | "any", "none", "all". Contoh: `match="any"`                                               |
| is-numeric                    | if                      | Cek apakah field numerik. Contoh: `is-numeric="edition"`                                  |
| plural                        | text, term              | "true"/"false". Contoh: `plural="true"`                                                   |
| sort-separator                | name                    | Pemisah antara nama saat sorting. Contoh: `sort-separator=", "`                           |
| initialize-with               | name                    | Inisialisasi nama depan. Contoh: `initialize-with=". "`                                   |
| form="ordinal"                | number                  | Format angka menjadi urutan (1st, 2nd, dst). Contoh: `form="ordinal"`                     |
| quotes                        | text                    | "true"/"false" (pakai tanda kutip). Contoh: `quotes="true"`                               |
| date-parts                    | date                    | Bagian tanggal yang ditampilkan. Contoh: `date-parts="year"`                              |
| font-variant                  | text                    | "small-caps". Contoh: `font-variant="small-caps"`                                         |
| strip-periods                 | text                    | "true"/"false". Contoh: `strip-periods="true"`                                            |
| plural                        | term                    | "true"/"false" (istilah jamak). Contoh: `plural="true"`                                   |
| value                         | text                    | Menampilkan teks statis. Contoh: `value="diakses pada"`                                   |
| quotes                        | text                    | "true"/"false" (pakai tanda kutip). Contoh: `quotes="true"`                               |
| sort                          | key                     | "ascending"/"descending". Contoh: `sort="ascending"`                                      |
| disambiguate-add-year-suffix  | citation                | "true"/"false". Menambah sufiks tahun jika perlu.                                         |
| collapse                      | citation                | "year", "citation-number". Contoh: `collapse="year"`                                      |
| givenname-disambiguation-rule | citation                | "primary-name", "all-names".                                                              |

---

## 3. Utilities & Fitur Khusus

| Utility/Fitur      | Penjelasan & Contoh Output                                                               |
| ------------------ | ---------------------------------------------------------------------------------------- |
| Komentar XML       | Dokumentasi di dalam file. Contoh: `<!-- Ini komentar -->`                               |
| Penggunaan Makro   | Memanggil makro untuk menghindari duplikasi kode. Contoh: `<text macro="author"/>`       |
| Substitusi         | Menampilkan alternatif jika field utama kosong. Contoh: `<substitute> ... </substitute>` |
| Pengurutan (Sort)  | Mengatur urutan daftar pustaka. Contoh: `<sort><key macro="author"/></sort>`             |
| Locale & Term      | Menyesuaikan istilah lokal. Contoh: `<term name="and">dan</term>`                        |
| Conditional Output | Output berbeda sesuai tipe sumber. Contoh: `<if type="book"> ... </if>`                  |
| Formatting         | Italic, bold, title case, dsb. Contoh: `<text variable="title" font-style="italic"/>`    |

---

## 4. Contoh Output & Penggunaan

### a. Buku

```xml
<group delimiter=". ">
  <text macro="author"/>
  <text macro="issued"/>
  <text variable="title" font-style="italic" text-case="title"/>
  <group delimiter=": ">
    <text variable="publisher-place"/>
    <text variable="publisher"/>
  </group>
</group>
```

**Output:**

```
Santoso, A. B. dkk. (2021). Pemrograman Dasar. Yogyakarta: Andi Publisher.
```

### b. Jurnal

```xml
<group delimiter=". ">
  <text macro="author"/>
  <text macro="issued"/>
  <text macro="title-plus-extra"/>
  <text macro="container"/>
</group>
<text macro="locators"/>
```

**Output:**

```
Sukorini, R. S. dkk. (2024). New Era In Higher Education. Jurnal Ilmiah, 11(2), 154–166.
```

### c. Website

```xml
<group delimiter=". ">
  <text macro="author"/>
  <text macro="issued"/>
  <text macro="title-plus-extra"/>
  <text macro="container"/>
</group>
<group delimiter=", ">
  <group delimiter=" ">
    <text value="Diambil dari link"/>
    <text variable="URL"/>
  </group>
  <group delimiter=" ">
    <text value="diakses pada"/>
    <date variable="accessed" form="text"/>
  </group>
</group>
```

**Output:**

```
Rahmawati, D. (2025). Panduan Skripsi Amikom. Website Amikom. Diambil dari link https://amikom.ac.id/panduan, diakses pada 9 September 2025
```

---

## 5. Referensi Resmi & Tools

- [CSL Specification](https://docs.citationstyles.org/en/stable/specification.html)
- [CSL Visual Editor](https://editor.citationstyles.org/visualEditor/)
- [CSL GitHub](https://github.com/citation-style-language/)
- [Daftar Lengkap Tipe CSL](https://aurimasv.github.io/z2csl/typeMap.xml)

---

_Dokumen ini dapat dikembangkan sesuai kebutuhan skripsi Amikom Purwokerto._
