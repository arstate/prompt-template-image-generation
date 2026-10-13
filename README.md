# 🎨 REPOSITORI MASTER TEMPLATE PROMPT IMAGE GENERATION (DJADI CREATIVE)

Repositori modular terstruktur untuk kebutuhan komersial studio fotografi produk, model fesyen wanita Indonesia, katalog pose, sudut kamera, dan alur kombo siap pakai.

## 📁 STRUKTUR FOLDER TERORGANISIR:

0. **`00_MASTER_VISUAL_BREAKDOWN_ENGINE/`**
   - Berisi 1 berkas master tunggal: `MASTER_AI_VISUAL_BREAKDOWN_ENGINE.md` (Hybrid Smart-Command & Forensic Edition).
   - Mendukung 2 jalur kerja: **Jalur Speedrun (Direct Command)** seperti `BREAKDOWN OUTFIT`, `BREAKDOWN BEAUTY`, `BREAKDOWN PRODUCT` (1x jalan tanpa ping-pong) dan **Jalur Eksplorasi** (`VISUAL BREAKDOWN` menghasilkan Quick Master Preview + Menu Adaptif bernomor sederhana).
   - Membedah visual referensi ke tingkat forensik (tekstil GSM, kraniofasial, ray-tracing, optik f/5.6-f/8) dengan format siap pakai untuk **Midjourney v6.1** dan **FLUX.1**.

1. **`01_PRODUCT_STUDIO_STANDALONE/`**
   - Koleksi 6 template prompt khusus objek produk tunggal tanpa manusia/manekin (Universal, Fashion Gantungan Kastok, Kerajinan Kulit, Sepatu, Kemasan Pouch/Botol, Aksesori Mewah).
   - Latar netral terkalibrasi (*anti-overexposure / anti-silau*), zero-morphing, 100% faithful ke gambar referensi.

2. **`02_MODEL_WANITA_INDONESIA/`**
   - 5 arketipe persona wanita muda Indonesia (Sunda Manis, Jawa Eksotis Sawo Matang, Jakarta Urban Chic, Hijab Modest, Editorial Runway).
   - Detail anatomi realistis: pori-pori mikro asli, peach fuzz, zero plastic waxy AI slop.

3. **`03_TEMPLATES_POSE/`**
   - 7 katalog pose anatomis terperinci (Berdiri Kontraposto, Duduk Kursi/Plinth, Memegang Produk Tas, Toleh Bahu Beauty, Berjalan Runway, Sentuhan Leher/Kerah, Duduk Lantai).

4. **`04_CAMERA_ANGLE_DAN_FRAMING/`**
   - 8 spesifikasi framing lensa dan sudut kamera profesional (termasuk Wide Full-Body Pulled Back / Kamera Mundur Jauh) (Extreme Close-Up, Bust Shot, Medium Shot Waist-Up, Cowboy Shot, Full Body Lookbook, Low Angle Heroic, High Angle Editorial).

5. **`05_TEMPLATE_KOMBO_SIAP_PAKAI/`**
   - 7 template kombo matang langsung eksekusi (termasuk Universal Skincare, Fashion, Handheld Product, Zero Pose Lock, dan Wide Pulled-Back, dan Jewelry Auto-Harmonization) (Kebaya Wisuda, Gamis Syari, Tas Kulit, Streetwear Blazer, Sepatu Kulit).
   - Panduan cara merangkai balok modular LEGO drag-and-drop.


6. **`06_BACKGROUND_TEMPAT_LOKASI/`**
   - 20 template prompt latar tempat & lingkungan arsitektural komersial (Galeri Beton Minimalis, Japandi Warm Wood, Cafe Specialty Coffee, Villa Tropis Bali, Archway Mediterania, Joglo Heritage, Penthouse Skyline, Parisian Sidewalk, Museum Brutalis, Rumah Kaca Botani, Loft Industrial, Sand Dune Pantai, Butik Salon, Workshop Batik, Fine Dining, Rooftop Senja, Zen Bamboo, Studio Keramik, Underpass Arsitektur, French Molding Klasik).
   - Pencahayaan ruang nyata, perspektif optik lensa asli, tanpa manusia, tanpa kurung siku, siap dipakai sebagai background tunggal atau di-merge ke model produk.


7. **`07_MULTI_ANGLE_SHOT_GENERATOR/`**
   - Berkas Master Multi-Angle Generator dari 1 foto referensi input (`01_MASTER_AI_MULTI_ANGLE_GENERATOR_FROM_REFERENCE.md`).
   - Otomatis mengunci identitas model, busana, dan pencahayaan, lalu memproduksi 8 sudut kamera lengkap:
     * Shot 1: Front Eye-Level (0° Depan)
     * Shot 2: Three-Quarter (45° Dimensional)
     * Shot 3: Side Profile (90° Samping)
     * Shot 4: Low-Angle Hero (15° Menengadah)
     * Shot 5: High-Angle Elevated (35° Menunduk)
     * Shot 6: Extreme Macro Detail (Serat & Aksesori)
     * Shot 7: Rear Back View (180° Belakang)
     * Shot 8: Wide Pulled-Back (8 Meter Mundur Jauh)
   - Dilengkapi `02_SNIPPET_8_SUDUT_KAMERA_PLUG_AND_PLAY.md` untuk peracikan instan.
   - Dilengkapi kompanion sintaks resmi FLUX.1 natural spatial prose untuk seluruh 8 sudut kamera.

8. **`08_STUDIO_TRANSFORMATION_DAN_HD_ENHANCER/`**
   - Koleksi 4 template & panduan penguncian wajah 100% dan restorasi optik HD:
     * `01_PROMPT_STUDIO_PUTIH_POLOS_BALANCED_EXPOSURE.md`: Mengubah foto kasual/outdoor menjadi foto studio berlatar belakang putih bersih terkalibrasi (*anti-overexposure / anti-glare / contact shadow*).
     * `02_PROMPT_UNIVERSAL_HD_ENHANCER_ZERO_MORPHING.md`: Restorasi foto apa pun menjadi resolusi ultra HD setara sensor medium format Hasselblad 100MP tanpa mengubah wajah, pakaian, atau pose.
     * `03_PROMPT_PERSONA_LOCK_POSE_SANTAI_STUDIO.md`: Kombo modular foto orang asli + background baru + pose santai rileks dengan wajah 100% terkunci identik.
     * `04_PANDUAN_KONSISTENSI_WAJAH_DAN_RESTORASI_HD.md`: Cheatsheet operasional cara upload URL, parameter `--cref`, perbedaan `--cw 0` vs `--cw 100`, dan panduan FLUX.1.

## 📌 ATURAN EMAS:
- **Tanpa Kurung Siku (`[]`):** Seluruh prompt berupa teks kalimat deskriptif mengalir bersih.
- **Tanpa URL Dummy:** Tidak ada link palsu di dalam prompt.
- **Tanpa Parameter Aspek Rasio (`--ar`):** Dikosongkan agar rasio bebas diketik sendiri di ujung prompt sesuai kanvas (misal `--ar 3:4` atau `--ar 9:16`).
