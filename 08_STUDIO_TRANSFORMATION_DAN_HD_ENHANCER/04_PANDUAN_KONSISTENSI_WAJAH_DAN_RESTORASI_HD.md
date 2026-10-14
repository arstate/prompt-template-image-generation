# 📖 PANDUAN MASTER: KONSISTENSI WAJAH 100% & RESTORASI HD (MIDJOURNEY & FLUX.1)

Panduan ini adalah standar operasional untuk memastikan wajah orang asli dari foto referensi terkunci 100% identik tanpa distorsi, serta cara mengeksekusi restorasi HD murni pada Midjourney v6.1 dan FLUX.1.

> 🚨 **HUKUM ABSOLUT EDIT FOTO: DILARANG GENERATE DARI PROMPT TEKS MENTAH!**
> Setiap kali ada permintaan **Edit Foto / Ubah Background / Ubah Pose / Restorasi HD**, AI atau pengguna **WAJIB MENGGUNAKAN GAMBAR REFERENSI INPUT** (Image-to-Image / Inpainting / Multimodal Attachment).
> **Mengapa prompt teks mentah selalu gagal?**
> Jika Anda hanya mengandalkan teks (Text-to-Image dari nol), AI akan *berhalusinasi* menciptakan orang baru yang acak. Wajah, proporsi mata, dan baju asli tidak akan pernah bisa 100% identik tanpa menautkan file gambar aslinya sebagai jangkar referensi (*visual anchor*).

---

## 🔑 1. CARA MENGAMBIL DIRECT URL GAMBAR DI DISCORD / MIDJOURNEY
Untuk menggunakan fitur penguncian wajah atau image reference, Anda membutuhkan tautan langsung (*direct image URL*) yang berakhiran `.jpg` atau `.png`:
1. Seret (*drag and drop*) foto referensi Anda ke chat Discord Midjourney Bot (atau channel Anda).
2. Tekan Enter untuk mengirim gambar tersebut.
3. Klik gambar yang sudah terkirim hingga terbuka penuh di layar.
4. Klik kanan pada gambar, lalu pilih **Copy Link** (atau **Buka di Browser** lalu salin URL di address bar).
5. Pastikan URL tersebut berakhiran `.png`, `.jpg`, atau `.webp`.

---

## 🧬 2. RAHASIA PARAMETER `--cref` DAN KALIBRASI `--cw` (CHARACTER WEIGHT)

Fitur Character Reference (`--cref`) pada Midjourney v6 dirancang untuk mentransfer identitas karakter dari 1 foto ke generasi baru.

### Sintaks Dasar:
```text
/imagine prompt: [Teks Prompt Komersial] --cref [URL_GAMBAR] --cw [NILAI] --style raw --c 1 --s 65
```

### ⚠️ PERBEDAAN KRUSIAL ANTARA `--cw 100` DAN `--cw 0`:

| Nilai Parameter | Fungsi Kerja | Kapan Harus Digunakan? |
| :--- | :--- | :--- |
| **`--cw 100`** *(Default)* | Mengunci **Wajah + Bentuk Rambut + Pakaian/Busana** dari foto referensi. | Gunakan pada **Template 02 (HD Enhancer)** saat Anda ingin merestorasi foto yang sama persis tanpa mengubah bajunya. |
| **`--cw 0`** *(Face Only)* | **HANYA Mengunci Wajah**. Pakaian, badan, dan latar belakang dibebaskan untuk diganti. | Gunakan pada **Template 01 (Studio Putih)** dan **Template 03 (Pose Santai)** agar baju kasual/kaos di foto asli bisa diganti jadi busana studio baru. |

---

## 🔍 3. FORMULA RESTORASI HD MURNI (ZERO-MORPHING OPTICAL REMASTERING)

Jika Anda ingin membuat foto HP biasa menjadi kualitas tajam setara kamera Hasselblad tanpa merubah wajah atau pose:
1. Pasang URL foto di awal prompt (*Image Prompt*).
2. Salin teks dari `02_PROMPT_UNIVERSAL_HD_ENHANCER_ZERO_MORPHING.md`.
3. Pasang parameter kunci:
```text
--iw 2.0 --style raw --c 0 --s 25 --cref [URL_GAMBAR] --cw 100
```
- `--iw 2.0`: Memberi bobot gambar input maksimal (100% patuh ke foto asli).
- `--c 0`: Mematikan keacakan (zero chaos) agar tidak ada elemen aneh yang muncul.
- `--s 25`: Menurunkan stylize agar AI tidak mendesain ulang subjek, melainkan hanya membersihkan noise dan menajamkan optik.

---

## ⚡ 4. PANDUAN KONSISTENSI WAJAH UNTUK PENGGUNA FLUX.1

Generator **FLUX.1 (Schnell / Dev / Pro)** memiliki arsitektur yang berbeda dengan Midjourney:
1. **Penggunaan PuLID / InstantID (ComfyUI):**
   - FLUX.1 di ComfyUI mendukung node **PuLID for FLUX** untuk mengunci embedding wajah 100% tanpa distorsi gaya.
2. **Penggunaan Natural Language Phrasing (Text-to-Image / Multi-modal):**
   - Sertakan kalimat pengunci identitas:
     `The subject's facial identity, distinctive eye shape, nose bridge, jawline, and natural skin tone are 100 percent identical to the reference image, rendered with natural skin micro-pores and realistic sub-surface scattering.`
   - Masukkan gambar referensi ke slot Image Input pada platform web FLUX.

---

## 🍌 5. PANDUAN GOOGLE GEMINI (NANO BANANA 2 / GEMINI 3.1 FLASH IMAGE)

Berbeda dengan Midjourney yang menggunakan CLI flags (`--cref`), Gemini Nano Banana 2 adalah **Multimodal LLM Image Editor**. 

### Aturan Emas Gemini Nano Banana 2:
1. **Dilarang Gunakan Perintah Pendek Kasual**: Prompt seperti `/image-gen buat jadi hd...` membuat model mengabaikan identitas asli dan beralih ke generasi bebas.
2. **Gunakan Two-Phase Chain-of-Thought (CoT)**:
   - **Phase 1 (Forensic Scan)**: Paksa Gemini memindai geometri wajah, kacamata (wajib tegaskan lensa bening transparan agar tidak berubah jadi kacamata hitam/sunglasses), layer pakaian asli, dan rambut.
   - **Phase 2 (Delta Transformation)**: Kunci seluruh atribut Phase 1 dan hanya transformasikan background (studio cyclorama putih) dan pose (sendakep santai).
3. **Template Siap Pakai**: Gunakan langsung prompt dari file `05_DYNAMIC_MULTIMODAL_STUDIO_TRANSFORMER.md`.

---

## 🔮 6. TEKNIK MULTI-IMAGE REFERENCE: TRIANGULASI 3D & FUSI MODULAR (KEMIRIPAN 98-100%)

Jika 1 foto referensi masih dirasa kurang mirip akibat distorsi lensa HP atau bayangan gelap, gunakan **Multi-Image Reference**:

### A. Stereoscopic Facial Triangulation (2 Foto Orang Sama)
- **Konsep:** Masukkan 2 foto orang yang sama (1 foto lurus ke kamera + 1 foto sudut 3/4 miring).
- **Hasil:** AI merekonsiliasi kedua sudut dan membentuk model 3D tengkorak yang presisi, melenyapkan distorsi perspektif foto tunggal.
- **Midjourney Syntax:** `--cref [URL_FOTO_1] [URL_FOTO_2] --cw 100` (Midjourney merata-rata embedding wajah dari kedua foto).
- **Gemini / Multimodal:** Gunakan template `06_MULTI_IMAGE_REFERENCE_FUSION_ENGINE.md` Mode A.

### B. Modular Role-Decoupled Fusion (Wajah + Pose + Latar Berbeda)
- **Konsep:** Menggabungkan 3 foto berbeda tanpa *feature bleeding*:
  - Gambar 1: Wajah sendiri (Identity Lock).
  - Gambar 2: Pose model dari majalah (Pose Donor).
  - Gambar 3: Latar studio atau cafe (Environment Donor).
- **Midjourney Syntax:** `--cref [URL_WAJAH] --cw 0 --sref [URL_LATAR]`
- **Gemini / Multimodal:** Gunakan template `06_MULTI_IMAGE_REFERENCE_FUSION_ENGINE.md` Mode B.

---

## 🚫 7. TROUBLESHOOTING: JIKA HASIL WAJAH MASIH KURANG MIRIP
1. **Wajah Terlalu Halus / Seperti Plastik (Semua Platform):** Pastikan prompt memuat klausa `natural skin micro-pores, uncompressed realistic skin texture, no airbrushed plastic AI smoothing`. Di Midjourney turunkan `--s 25` dan aktifkan `--style raw`.
2. **Kacamata Berubah Jadi Kacamata Hitam (Gemini/Nano Banana 2):** Pantulan cahaya lensa sering disalahartikan sebagai kacamata hitam. Selalu sertakan: `100% CLEAR TRANSPARENT prescription glass with pupils clearly visible behind lenses, no dark sunglass tint`.
3. **Baju Berubah Jadi Jas Formal Padahal Mau Baju Asli:** Kata "profesional" memicu bias formal. Tegaskan: `Keep the exact clothing outfit detected in the reference photo, do not replace with a formal business suit or blazer`.
4. **Fitur Gambar Tercampur Aduk (Multi-Image Bleeding):** Berikan partisi peran eksplisit pada setiap gambar (`Image 1: Face ONLY`, `Image 2: Pose ONLY`, `Image 3: Environment ONLY`).
5. **Wajah Kurang Mirip 100%:** Gunakan Mode A Facial Triangulation dengan mengunggah 2 sudut foto wajah sekaligus.


