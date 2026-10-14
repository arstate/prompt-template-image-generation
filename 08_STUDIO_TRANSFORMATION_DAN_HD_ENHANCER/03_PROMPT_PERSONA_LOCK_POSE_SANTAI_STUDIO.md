# PROMPT PERSONA LOCK & POSE SANTAI STUDIO (MODULAR COMPOSITE)

Template kombo modular ini khusus digunakan untuk menggabungkan **Foto Orang Asli Pengguna** dengan **Pose Santai Rileks** dan **Background Baru Estetik**. Wajah orang asli terkunci 100% identik tanpa distorsi, sementara pose tubuh dan latarnya berpadu secara alami layaknya pemotretan majalah komersial profesional.

---

> ⚠️ **MANDAT WAJIB IMAGE REFERENCE:**
> DILARANG meng-generate dari teks mentah (*text-to-image from scratch*). Prompt ini WAJIB dijalankan dalam mode **Image-to-Image / Reference Binding** dengan melampirkan foto asli yang di-input pengguna.

---

## ⚡ ALL-IN-ONE MASTER PROMPT (NANO BANANA 2.1 / GPT IMAGE 2.5 - 1X COPAS LANGSUNG JADI)
> Cukup 1x salin teks di bawah ini dan tempelkan bersama foto input ke Gemini Nano Banana 2.1 atau ChatGPT GPT Image 2.5:

```text
[ATTACHED PHOTO IS SOLE GROUND TRUTH REFERENCE - PERSONA LOCK]
Generate a relaxed commercial lifestyle studio portrait using the attached reference photograph, 100 percent faithful facial identity retention maintaining exact craniofacial bone structure, distinctive eye contours, nose bridge, jawline, and natural warm skin tone with zero facial drift. The subject adopts an elegant relaxed stance with natural weight shift, relaxed dropped shoulders, hands resting gracefully with natural anatomically correct fingers, quiet confident friendly expression. Authentically rendered skin micro-pore definition, soft sub-surface scattering skin glow. Placed naturally within modern minimalist architectural studio environment, soft ambient daylight filtering from large side window combined with diffused studio fill, realistic soft contact floor shadow beneath footwear, shot on Hasselblad medium format with 85mm lens at f/5.6 for tack-sharp front-to-back optical clarity.
STRICT NEGATIVE CONSTRAINTS (DO NOT INCLUDE): altered facial features, modified facial structure, different person, facial morphing, deformed face, wrong ethnicity, changed eye shape, stiff robotic stance, awkward limb placement, clenched fists, deformed hands, extra fingers, missing fingers, floating body, no ground shadow, plastic skin, waxy texture, airbrushed skin, beauty filter, facetune, 3d render, cgi, cartoon, anime, over-processed, artifacts, watermark.
```

---

## 🎯 POSITIVE PROMPT SIAP PAKAI (MIDJOURNEY v6.1 - IMAGE-TO-IMAGE)
```text
[URL_FOTO_REFERENSI_USER] relaxed commercial lifestyle studio portrait of the input reference person, 100 percent faithful facial identity retention maintaining exact craniofacial bone structure, distinctive eye contours, nose bridge, jawline, and natural warm skin tone of the reference person with zero facial drift. The subject is posed in an elegant relaxed stance, natural casual weight shift, relaxed dropped shoulders, hands resting gracefully with natural anatomically correct fingers, quiet confident friendly expression. Authentically rendered micro-pore definition, soft sub-surface scattering skin glow, zero plastic smoothing. Placed naturally within modern minimalist architectural studio environment, soft ambient daylight filtering from large side window combined with diffused studio fill, grounded with realistic soft contact drop shadow beneath footwear on floor, captured on Hasselblad H6D-100c medium format camera with 85mm lens at f/5.6 for tack-sharp front-to-back optical clarity, genuine high-end editorial lifestyle lookbook standard, real camera photograph, zero plastic sheen, no CGI slop --cref [URL_FOTO_REFERENSI_USER] --cw 0 --style raw --c 1 --s 65 --seed 38192044
```


> **💡 PANDUAN NILAI `--cw`:**
> - Parameter `--cw 0` mengunci wajah 100% identik dari foto input, namun membebaskan badan dan pakaian untuk mengikuti pose santai baru.
> - Jika ingin tetap mempertahankan pakaian asli dari foto referensi, ubah menjadi `--cw 100`.

---

## 🚫 NEGATIVE PROMPT (ANTI WAJAH BERUBAH & ANTI POSE KAKU)
altered facial features, modified facial structure, different person, facial morphing, deformed face, wrong ethnicity, changed eye shape, stiff robotic stance, awkward limb placement, clenched fists, deformed hands, extra fingers, missing fingers, floating body, no ground shadow, plastic skin, waxy texture, airbrushed, beauty filter, facetune, 3d render, cgi, cartoon, anime, over-processed, artifacts, watermark

---

## ⚙️ SEED & PARAMETERS
- **Image Input Slot:** `[URL_FOTO_REFERENSI_USER]` (Wajib disematkan di awal)
- **Character Reference:** `--cref [URL_FOTO_REFERENSI_USER]`
- **Character Weight:** `--cw 0` (pose santai baru) atau `--cw 100` (pakaian asli)
- **Seed:** `38192044`
- **Style:** `--style raw`
- **Chaos:** `--c 1`
- **Stylize:** `--s 65`

---

## ⚡ FLUX.1 COMPANION (IMAGE-TO-IMAGE / CONDITIONED POSE)
```text
[INPUT: REFERENCE_IMAGE_1 (MANDATORY ATTACHED PHOTO)]
A relaxed commercial lifestyle studio portrait of the exact person in the attached reference image. The subject's craniofacial structure, eyes, nose, facial proportions, and authentic skin texture are preserved with 100 percent fidelity. The subject adopts a relaxed natural posture with dropped shoulders and relaxed hands, looking warmly toward the lens. The setting is a clean modern minimalist architectural interior with soft window daylight entering from the side and gentle fill lighting. The subject is firmly grounded on the floor with natural soft contact shadows beneath their footwear. Shot on a medium format camera with an 85mm lens at f/5.6 for crisp detail from facial features to clothing drape. Real camera photograph, zero plastic smoothing.
```

