# 📖 PANDUAN MASTER: KONSISTENSI WAJAH 100% & RESTORASI HD (MIDJOURNEY & FLUX.1)

Panduan ini adalah standar operasional untuk memastikan wajah orang asli dari foto referensi terkunci 100% identik tanpa distorsi, serta cara mengeksekusi restorasi HD murni pada Midjourney v6.1 dan FLUX.1.

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

## 🚫 5. TROUBLESHOOTING: JIKA HASIL WAJAH MASIH KURANG MIRIP
1. **Wajah Terlalu Halus / Seperti Plastik:** Pastikan nilai `--s` tidak melebihi 65, dan pastikan parameter `--style raw` aktif.
2. **Baju Asli Ikut Terbawa Padahal Mau Ganti Baju:** Turunkan parameter `--cw` menjadi `--cw 0`.
3. **Wajah Kurang Mirip 100%:** Pastikan foto referensi input memiliki pencahayaan jelas di area mata dan wajah (tidak terpotong, tidak backlight gelap, dan tidak memakai filter kecantikan berlebihan).
