# TEMPLATE 06: MULTI-IMAGE REFERENCE FUSION & FACIAL TRIANGULATION ENGINE

## 📌 DESKRIPSI & ARSITEKTUR MULTI-REFERENCE
Template ini dirancang untuk menangani skenario ketika pengguna mengunggah **lebih dari 1 gambar referensi** (2 sampai 3 gambar). 

Tanpa isolasi peran yang ketat (*role-binding*), AI akan mencampuradukkan fitur secara acak (*destructive feature bleeding*). Template ini membagi pemrosesan multi-gambar menjadi **2 MODE UTAMA**:

1. **MODE A: STEREOSCOPIC FACIAL TRIANGULATION (100% IDENTITY LOCK)**
   - Menggunakan 2 foto orang yang sama (misal: 1 foto tampak depan + 1 foto sudut 3/4 miring).
   - AI merekonsiliasi kedua sudut untuk membangun model topografi 3D tengkorak dan wajah, menghapus bias distorsi lensa tunggal. Tingkat kemiripan mencapai ~98-100%.
2. **MODE B: MODULAR ROLE-DECOUPLED FUSION (SUBJECT + POSE + ENVIRONMENT)**
   - Menggunakan 2-3 gambar berbeda:
     - **Image 1**: Donor Identitas (HANYA ekstrak wajah, mata, dan rambut).
     - **Image 2**: Donor Pose (HANYA ekstrak gestur tubuh dan framing, abaikan wajah model di Gbr 2).
     - **Image 3**: Donor Environment/Studio (HANYA ekstrak latar belakang dan skema lighting, abaikan orang di Gbr 3).

---

## 🎯 MODE A: MASTER PROMPT FACIAL TRIANGULATION (2 FOTO ORANG SAMA)

### 1. Midjourney v6.1 (Multi-Cref Syntax)
```text
[URL_FOTO_DEPAN] [URL_FOTO_SUDUT] commercial studio portrait photograph, stereoscopic dual-angle facial triangulation reconciling Input Image 1 and Input Image 2 into absolute 100 percent craniofacial identity fidelity. Synthesizing true 3D mandibular jawline depth, exact nasal bridge curvature, authentic eye spacing, and biological skin undertones with zero single-lens distortion. Natural relaxed direct gaze into Hasselblad H6D-100c medium format camera with 85mm portrait lens at f/5.6, visible micro-pores, natural sub-surface scattering skin glow. Placed against seamless neutral off-white studio cyclorama wall with subtle soft contact floor shadow, balanced dual softbox strobes, real camera photo, zero plastic airbrushing --cref [URL_FOTO_DEPAN] [URL_FOTO_SUDUT] --cw 100 --style raw --c 1 --s 65 --seed 49102934
```

### 2. Google Gemini Nano Banana 2 & Multimodal LLM (English Direct)
```text
[SYSTEM INSTRUCTION: DUAL-IMAGE FACIAL TRIANGULATION & IDENTITY RECONCILIATION]

TASK OVERVIEW:
Reconstruct a single high-definition studio portrait of the subject using Image 1 (frontal view) and Image 2 (angular/profile view).

PHASE 1: 3D CRANIOFACIAL TRIANGULATION (INTERNAL SCAN)
Cross-reference Image 1 and Image 2 to reconstruct the subject's true 3D facial geometry:
1. Reconcile both angles to calculate true nasal bridge height, nostril symmetry, cheekbone prominence, and jawline angle, eliminating single-lens focal distortion.
2. If glasses are present in either photo: enforce exact frame structure with 100% CLEAR TRANSPARENT optical lenses. Pupils and iris must be tack-sharp. Prohibit dark sunglasses.
3. Freeze hair silhouette and authentic skin undertones.

PHASE 2: DIRECTED STUDIO SYNTHESIS
Generate the unified portrait:
- [FROZEN IDENTITY - 100% LOCK]: Render the triangulated facial identity from Phase 1. Zero facial morphing.
- [STUDIO DELTA]: Position subject in a relaxed, confident chest-up 3:4 portrait stance facing the camera.
- [BACKGROUND & LIGHTING]: Seamless pure white photography studio cyclorama, balanced softbox key light at 45 degrees, gentle fill, realistic subtle contact floor shadow. Crisp 4K photographic texture with authentic micro-pores. No plastic AI skin smoothing.
```

---

## 🎯 MODE B: MASTER PROMPT ROLE-DECOUPLED FUSION (WAJAH + POSE + STUDIO)

### 1. Midjourney v6.1 (Omni-Reference Partition)
```text
[URL_FOTO_WAJAH] [URL_FOTO_POSE] [URL_FOTO_STUDIO] commercial editorial lookbook portrait photograph. STRICT ROLE-BINDING PARTITION: 100 percent facial identity and facial bone structure extracted exclusively from Image 1 with zero facial drift. Body posture, shoulder line, and hand gestures adopted strictly from Image 2. Background architecture, cyclorama wall, and lighting mood adopted strictly from Image 3. Zero cross-feature bleeding. Captured on medium format Hasselblad at f/5.6 for front-to-back optical clarity, realistic fabric drape, authentic micro-pores, natural contact floor shadow --cref [URL_FOTO_WAJAH] --cw 0 --sref [URL_FOTO_STUDIO] --style raw --c 1 --s 65 --seed 81920384
```

### 2. Google Gemini Nano Banana 2 & Multimodal LLM (English Direct)
```text
[SYSTEM INSTRUCTION: MULTI-IMAGE ROLE-DECOUPLED COMPOSITE (ZERO FEATURE BLEEDING)]

INPUT ROLE ASSIGNMENTS:
- Image 1: SUBJECT IDENTITY DONOR (Face, Eyes, Eyewear, Hair)
- Image 2: POSE & ANATOMICAL GESTURE DONOR (Body Posture, Hand Placement, Framing)
- Image 3: ENVIRONMENT & LIGHTING DONOR (Background, Studio Wall, Lighting Temperature)

STRICT EXECUTION DIRECTIVES:
1. IDENTITY EXTRACTION (FROM IMAGE 1 ONLY):
   - Transfer the exact craniofacial geometry, facial landmarks, eye shape, and skin tone from Image 1.
   - If Image 1 wears spectacles, preserve frame shape and enforce 100% CLEAR TRANSPARENT prescription glass.
   - COMPLETELY DISREGARD the body posture and background of Image 1.
2. POSE EXTRACTION (FROM IMAGE 2 ONLY):
   - Apply the body stance, arm positioning, and gesture shown in Image 2 onto the subject from Image 1.
   - COMPLETELY DISREGARD the head and face of the person in Image 2.
3. ENVIRONMENT EXTRACTION (FROM IMAGE 3 ONLY):
   - Place the combined subject inside the exact studio or ambient space shown in Image 3.
   - Match key lighting angle and color temperature from Image 3, anchoring realistic contact shadows.
   - COMPLETELY DISREGARD any human subject inside Image 3.

QUALITY GATE:
Tack-sharp 4K photographic fidelity, authentic skin micro-pores, zero plastic smoothing, zero feature cross-contamination.
```

---

## 🇮🇩 VARIAN INDONESIA UNTUK GEMINI (ROLE-DECOUPLED)

```text
Instruksi Sistem: Fusi Multimodal Multi-Gambar dengan Partisi Peran Ketat (Anti-Campur Aduk)

Tetapkan peran spesifik untuk tiap gambar yang terlampir:
- GAMBAR 1 = DONOR IDENTITAS WAJAH (Wajah, Mata, Kacamata, Rambut)
- GAMBAR 2 = DONOR POSE (Sikap Badan, Posisi Tangan, Gestur)
- GAMBAR 3 = DONOR STUDIO / LATAR (Background, Pencahayaan, Suasana Ruang)

ATURAN PARTISI KETAT (DILARANG TERCAMPUR):
1. Dari Gambar 1: Ambil 100% kemiripan wajah, mata, dan rambut asli. Jika memakai kacamata, wajib lensa bening transparan (bukan kacamata hitam). Buang pose dan latar belakang Gambar 1.
2. Dari Gambar 2: Ambil bentuk pose tubuh dan tangan bersedekap/santai. Buang seluruh wajah dan kepala model di Gambar 2.
3. Dari Gambar 3: Ambil latar belakang studio putih bersih dan tata lampu studio. Buang orang di Gambar 3 jika ada.
4. Kualitas: Ketajaman foto komersial 4K, tekstur pori-pori kulit asli, tanpa efek plastik halus AI.
```

---

## ⚙️ RINGKASAN MATRIKS MULTI-REFERENCE
| Kebutuhan Pengguna | Jumlah Gambar | Mode yang Dipakai | Parameter Utama |
| :--- | :--- | :--- | :--- |
| **Ingin wajah mirip 100% maksimal** | 2 Foto (Depan + Sudut Miring) | **Mode A: Facial Triangulation** | Midjourney: `--cref URL1 URL2 --cw 100`<br>Gemini: *Dual-Image Triangulation* |
| **Ingin wajah sendiri tapi tiru pose orang lain** | 2 Foto (Gbr 1: Diri Sendiri, Gbr 2: Model Pose) | **Mode B: Role-Decoupled** | Midjourney: `--cref URL1 --cw 0`<br>Gemini: *Gbr 1 Identity + Gbr 2 Pose* |
| **Wajah sendiri + Tiru pose + Latar studio khusus** | 3 Foto (Gbr 1: Wajah, Gbr 2: Pose, Gbr 3: Latar) | **Mode B: Role-Decoupled** | Midjourney: `--cref URL1 --sref URL3`<br>Gemini: *Gbr 1 + Gbr 2 + Gbr 3* |
