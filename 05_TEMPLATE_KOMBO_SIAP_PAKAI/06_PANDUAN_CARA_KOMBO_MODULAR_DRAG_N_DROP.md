# PANDUAN FORMULA MODULAR DRAG & DROP PROMPT (DENGAN KUNCI POSE)

Sistem peracikan prompt ini bekerja seperti balok LEGO. Anda cukup menggabungkan elemen teks dari masing-masing folder tanpa tanda kurung siku dan tanpa simbol aneh.

---

## 🔒 HUKUM MUTLAK KONTROL POSE:
- **JIKA ANDA TIDAK MEMASUKKAN TEMPLATE POSE:** Prompt secara default **WAJIB MENGUNCI POSE MODEL** agar postur, letak tangan, dan posisi tubuh tidak bergeser saat Anda mengganti busana atau produk.
- **JIKA ANDA INGIN MENGUBAH POSE:** Barulah tempelkan snippet pose dari folder `03_TEMPLATES_POSE`.

---

## 1. FORMULA STRUKTUR PROMPT KOMBO
Urutan penggabungan teks:
`BAGIAN 1: MODEL PERSONA` + `BAGIAN 2: BUSANA / PRODUK` + `BAGIAN 3: KONTROL POSE (KUNCI ATAU POSE BARU)` + `BAGIAN 4: CAMERA FRAMING & STUDIO LIGHTING` + `BAGIAN 5: PARAMETERS`

---

## 2. CONTOH CARA MERANGKAI DENGAN CEPAT

### Langkah A: Ambil Model Persona (dari Folder 02)
commercial advertising photography of gorgeous young 21-year-old Indonesian woman, authentic Sundanese beauty, feminine oval face, sweet gentle smile with subtle cheek dimple, clear bright dark brown almond eyes, soft rosy lips, healthy voluminous dark wavy hair, radiant warm golden undertone skin with natural micro-pores,

### Langkah B: Masukkan Busana / Produk Pilihan Anda
wearing modern tailored fashion apparel garment with authentic fabric weave and fluid natural drape,

### Langkah C: Kontrol Pose (PILIH SALAH SATU)
- **Pilihan 1: JIKA INGIN POSE TIDAK BERUBAH (KUNCI POSE):**
strictly maintaining the exact body pose, hand placement, and natural posture of the model with zero pose modification, unchanged stance,

- **Pilihan 2: JIKA INGIN POSE BARU (Ambil dari Folder 03):**
standing three-quarter fashion model pose, natural contrapposto weight shift onto left leg, right hand resting casually along thigh, upright relaxed posture,

### Langkah D: Tempelkan Kamera, Framing & Latar (dari Folder 04 atau 06)
three-quarter cowboy framing from mid-thigh to head, shot on Sony A7R V with 85mm lens, f/5.6 aperture for edge-to-edge optical sharpness. Seamless matte soft neutral light grey studio cyclorama background, balanced dual softbox studio strobes, calibrated exposure, realistic subtle contact drop shadow,

### Langkah E: Akhiri dengan Parameter Bawaan
real camera photograph, zero plastic sheen, no CGI slop --style raw --c 1 --s 65 --seed 38192044

---

## 3. CATATAN PENTING
1. Tanpa kurung siku sama sekali.
2. Parameter rasio `--ar` sengaja tidak disertakan, ketik manual di paling belakang sesuai target kanvas Anda (misal: `--ar 3:4` untuk IG Feed, `--ar 9:16` untuk Reels/Story, atau `--ar 1:1` untuk e-commerce marketplace).
3. **Negative Prompt Pengunci Pose Wajib:** Jika mengunci pose, selalu sertakan kata berikut pada negative prompt:
`changed pose, modified posture, shifted arms, repositioned legs, different body angle, altered stance, new pose`
