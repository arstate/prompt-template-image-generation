# TEMPLATE 05: DYNAMIC MULTIMODAL STUDIO TRANSFORMER (GEMINI NANO BANANA 2 & MULTIMODAL AI)

## 📌 DESKRIPSI & ARSITEKTUR
Template ini dirancang untuk model multimodal modern (**Google Gemini Nano Banana 2 / Gemini 3.1 Flash Image**, GPT-4o Vision, Midjourney, dan model mutakhir lainnya). 

Alih-alih mengunci atribut secara statis (*hardcoded* seperti menyebut jenis baju atau kacamata manual), template ini memaksa AI melakukan **Two-Phase Chain-of-Thought (CoT) Visual Deconstruction**:
1. **Phase 1 (Deep Forensic Scan)**: AI memindai gambar input secara mandiri untuk mengekstrak geometri wajah, mata, kacamata (wajib deteksi bening/bukan kacamata hitam), pakaian asli, dan rambut.
2. **Phase 2 (Targeted Delta Execution)**: AI membekukan identitas hasil Phase 1 dan hanya mentransformasikan background menjadi studio putih cyclorama, pose sendakep santai, dan pencahayaan studio 4K.

Template ini **100% UNIVERSAL**: dapat dipakai untuk foto pria, wanita, kasual, formal, berkacamata, maupun tanpa kacamata tanpa mengedit isi prompt.

> 🚨 **MANDAT WAJIB LAMPIRKAN FOTO INPUT USER:**
> Prompt ini adalah instruksi rekonstruksi **Image-to-Image Multimodal**. **DILARANG** menjalankan prompt ini sebagai teks mentah tanpa melampirkan foto orang asli yang di-input pengguna. AI wajib memperlakukan file foto terlampir sebagai referensi absolut tunggal (*ground truth*).

---

## 🎯 MASTER UNIVERSAL PROMPT (ENGLISH - DIRECT INPUT)

Salin teks di bawah ini dan kirimkan bersama foto referensi di Gemini / Nano Banana 2 / AI Studio:

```text
[SYSTEM INSTRUCTION: MULTIMODAL IMAGE-TO-IMAGE RECONSTRUCTION WITH DYNAMIC IDENTITY LOCK]

TASK OVERVIEW:
Transform the attached reference image into a clean, professional studio portrait while maintaining 100% fidelity to the subject's identity, original apparel, and natural eyewear.

PHASE 1: FORENSIC MULTI-LAYER IMAGE SCAN (INTERNAL DECONSTRUCTION)
Before generating any pixels, thoroughly scan and analyze the attached reference image across all layers:
1. Facial Architecture: Map the subject's exact bone structure, jawline contours, eye shape, iris gaze, nose bridge, lips, and natural skin undertones.
2. Eyewear & Optics: Check if the subject wears spectacles. If detected: preserve the exact frame geometry, and enforce 100% CLEAR TRANSPARENT prescription optical glass. Pupils and eyes must be sharply visible behind lenses. Strictly prohibit dark sunglass tint or opaque shading.
3. Apparel Layering: Identify all garments currently worn (outerwear, inner t-shirt/shirt, fabric texture, weave patterns, exact colors, and visible graphics).
4. Hair & Silhouette: Identify exact haircut length, volume, layered texture, and silhouette edges.

PHASE 2: DIRECTED DELTA EXECUTION (TARGETED STUDIO RECONSTRUCTION)
Generate the final portrait adhering strictly to these directives:
- [FROZEN IDENTITY LOCK - 100% PRESERVED]: Lock all attributes detected in Phase 1. The face, haircut, clear optical spectacles, and exact clothing outfit must remain intact. Do NOT replace clothing with a business suit or blazer. Do NOT morph facial landmarks.
- [DELTA 1 - POSE & COMPOSITION]: Medium chest-up 3:4 portrait framing. Subject is posed comfortably with arms naturally crossed across chest (pose sendakep santai), confident and approachable expression looking directly into the camera lens.
- [DELTA 2 - BACKGROUND]: Completely eliminate original cluttered background. Replace with a seamless, solid pure white photography cyclorama studio backdrop. Include subtle, realistic soft floor contact shadows. Background must be pristine white with balanced exposure (zero blown-out highlight clipping).
- [DELTA 3 - STUDIO LIGHTING & RESOLUTION]: Professional 45-degree softbox key lighting, gentle ambient fill light, subtle catchlights in eyes, crisp 4K photographic sharpness, realistic uncompressed skin texture with visible natural micro-pores. No airbrushed plastic AI smoothing.
- [STRICT NEGATIVE CONSTRAINTS (DO NOT INCLUDE)]: formal business suit, tuxedo, blazer, necktie, dark sunglasses, tinted lenses, plastic skin, airbrushed skin, blown out white highlights, clipped whites, distorted hands, morphing jawline, generic stock photo face, 3d render, cartoon, digital illustration, watermark.
```

---

## 🇮🇩 VARIAN INDONESIA (UNTUK GEMINI BAHASA INDONESIA)

Gunakan jika berinteraksi dengan Gemini dalam Bahasa Indonesia:

```text
Instruksi Sistem: Transformasi Foto Multimodal dengan Kunci Identitas Otomatis

Foto terlampir adalah referensi utama. Lakukan analisis dan generasi gambar dalam 2 tahap:

TAHAP 1: PEMINDAIAN FORENSIK VISUAL (DEKONSTRUKSI OTOMATIS)
Pindai subjek pada foto terlampir secara menyeluruh:
1. Struktur Wajah: Petakan bentuk rahang, mata, hidung, bibir, dan warna kulit asli subjek.
2. Kacamata & Aksesoris: Jika subjek berkacamata, pertahankan bingkai aslinya dan WAJIBKAN lensa kaca BENING TRANSPARAN 100% (mata dan pupil terlihat jelas di balik kaca). Dilarang mengubahnya menjadi kacamata hitam/sunglasses.
3. Pakaian Asli: Deteksi seluruh pakaian yang dipakai (luaran, baju dalaman, motif, warna, dan logo).
4. Rambut: Deteksi gaya potongan, volume, dan tekstur rambut asli.

TAHAP 2: EKSEKUSI TRANSFORMASI STUDIO
Hasilkan foto baru dengan aturan ketat:
- KUNCI IDENTITAS (100% TETAP): Pertahankan wajah, kacamata bening, pakaian asli, dan rambut hasil Tahap 1. DILARANG mengganti baju dengan jas/blazer. DILARANG mengubah kemiripan wajah.
- UBAH POSE: Reframe foto potret 3:4 (dada ke atas), pose tangan bersedekap santai di dada (pose sendakep santai), ekspresi ramah, santai, dan percaya diri menatap kamera.
- UBAH BACKGROUND: Ganti latar belakang berantakan menjadi studio foto putih polos mulus (seamless white cyclorama) dengan bayangan lantai alami yang halus. Background putih bersih tanpa overexposure silau.
- PENCAHAYAAN & KUALITAS: Tata cahaya softbox studio 45 derajat, ketajaman foto 4K, tekstur pori-pori kulit alami tampak nyata tanpa efek plastik AI halus.
- LARANGAN KETAT (NEGATIVE CONSTRAINTS): Dilarang jas formal/blazer, dilarang kacamata hitam/lensa gelap, dilarang kulit plastik mulus palsu, dilarang background silau overexposure meledak, dilarang tangan distorsi, dilarang 3D render atau kartun.
```


---

## ⚙️ PARAMETER TEKNIS IMPLEMENTASI
| Platform | Metode Eksekusi | Tips Efektivitas |
| :--- | :--- | :--- |
| **Google Gemini (Nano Banana 2)** | Lampirkan foto + Paste Prompt Phase 1 & 2 | Jangan gunakan `/image-gen`. Ketik langsung teks di kolom chat bersama attachment foto. |
| **NightCafe (Nano Banana)** | Mode Image-to-Image / Edit | Aktifkan brush protection mask pada wajah jika tersedia fitur inpainting. |
| **Midjourney v6.1 / Niji 6** | `[URL_FOTO] [Prompt Phase 2] --cref [URL_FOTO] --cw 85 --ar 3:4` | Gunakan `--cw 85` agar pakaian dan rambut terbawa tanpa drift. |
| **FLUX.1 Redux / Kontext** | Image Guidance Weight: 0.85 | Gunakan teks Phase 2 sebagai conditioned prompt. |

---

## 🚫 ATURAN NEGATIF (ANTI-DRIFT GUARD)
- `Negative Prompt / Prohibited Elements`:
  - `formal business suit, tuxedo, blazer, necktie, dark sunglasses, tinted lenses, plastic skin, airbrushed skin, blown out white highlights, clipped whites, distorted hands, morphing jawline, generic stock photo face`.
