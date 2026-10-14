# PROMPT STUDIO PUTIH POLOS (BALANCED EXPOSURE & NATIVE FACE-LOCK)

Template ini khusus digunakan untuk mengubah foto orang biasa (selfie, outdoor, atau foto kasual) menjadi foto studio komersial berlatar belakang putih bersih terkalibrasi (*anti-overexposure / non-blinding*) dengan penguncian wajah orang asli 100% identik tanpa distorsi.

---

> ⚠️ **MANDAT WAJIB IMAGE REFERENCE:**
> DILARANG meng-generate dari teks mentah (*text-to-image from scratch*). Prompt ini WAJIB dijalankan dalam mode **Image-to-Image / Reference Binding** dengan melampirkan foto asli yang di-input pengguna.

---

## 🎯 POSITIVE PROMPT SIAP PAKAI (MIDJOURNEY v6.1 - IMAGE-TO-IMAGE)
```text
[URL_FOTO_REFERENSI_USER] commercial studio portrait photograph of the input reference person, 100 percent faithful facial identity retention maintaining exact craniofacial bone structure, identical eyes, nose, lips, natural skin tone, and unique facial markers of the input reference person with zero facial morphing. The subject is posed naturally with calm confident gaze into the camera, authentic micro-pore definition, soft sub-surface scattering skin glow, zero waxy plastic smoothing. Positioned against seamless soft neutral light alabaster off-white studio cyclorama background, perfectly calibrated 1:1 key-to-background exposure preventing blown-out highlights or harsh glare, balanced dual 120cm softbox studio strobes with subtle edge rim light, soft realistic ambient occlusion contact drop shadow anchored beneath footwear on the studio floor, captured with Hasselblad H6D-100c medium format camera, 85mm portrait lens, f/5.6 aperture for edge-to-edge optical sharpness, genuine commercial lookbook quality, real camera photo, zero plastic sheen, no CGI slop --cref [URL_FOTO_REFERENSI_USER] --cw 100 --style raw --c 1 --s 65 --seed 24091367
```

> **💡 PANDUAN NILAI `--cw`:**
> - Gunakan `--cw 100` jika ingin **mempertahankan pakaian asli** dari foto referensi.
> - Gunakan `--cw 0` jika ingin **mengganti pakaian biasa menjadi pakaian studio baru** tanpa mengubah wajah.

---

## 🚫 NEGATIVE PROMPT (ANTI WAJAH BERUBAH & ANTI SILAU)
altered facial features, modified facial structure, different person, facial morphing, deformed face, wrong ethnicity, changed eye shape, plastic skin, waxy texture, airbrushed skin, beauty filter, facetune, pure blinding white background, blown-out highlights, clipped white glare, washed-out exposure, overexposed walls, missing ground shadow, floating person, 3d render, cgi, cartoon, anime, illustration, extra fingers, deformed hands, artifacts, watermark

---

## ⚙️ SEED & PARAMETERS
- **Image Input Slot:** `[URL_FOTO_REFERENSI_USER]` (Wajib disematkan di awal)
- **Character Reference:** `--cref [URL_FOTO_REFERENSI_USER]`
- **Character Weight:** `--cw 100` (pakaian asli) atau `--cw 0` (ganti pakaian)
- **Seed:** `24091367`
- **Style:** `--style raw`
- **Chaos:** `--c 1`
- **Stylize:** `--s 65`

---

## ⚡ FLUX.1 COMPANION (IMAGE-TO-IMAGE / CONDITIONED EDIT)
```text
[INPUT: REFERENCE_IMAGE_1 (MANDATORY ATTACHED PHOTO)]
A commercial high-end studio portrait photograph of the exact person in the attached reference image. The subject's facial identity, bone structure, eyes, and natural features are 100 percent preserved with exact fidelity and natural skin micro-pores. The subject is centered comfortably against a clean seamless matte alabaster off-white studio cyclorama backdrop. The studio lighting is evenly calibrated with dual large softboxes, creating gentle highlights without overexposing the background or creating harsh glare. Realistic soft ambient contact drop shadows are grounded directly beneath the subject on the studio floor. Shot on a medium format camera with an 85mm portrait lens at f/5.6 for tack-sharp facial clarity and realistic depth. Zero digital airbrushing, authentic human skin luminosity.
```

