# PROMPT UNIVERSAL HD ENHANCER (OPTICAL REMASTERING & ZERO MORPHING)

Template ini khusus digunakan untuk merestorasi dan meningkatkan resolusi foto apa pun (foto HP buram, foto lama, atau gambar beresolusi rendah) menjadi kualitas ultra HD setara kamera medium format Hasselblad 100MP **TANPA MENGUBAH SEDIKITPUN** wajah, pakaian, pose, atau latar belakang aslinya.

---

> ⚠️ **MANDAT WAJIB IMAGE REFERENCE:**
> DILARANG meng-generate dari teks mentah (*text-to-image from scratch*). Prompt ini adalah **Optical Remastering** yang WAJIB dijalankan dalam mode **Image-to-Image** dengan melampirkan foto asli yang di-input pengguna.

---

## 🎯 POSITIVE PROMPT SIAP PAKAI (MIDJOURNEY v6.1 - IMAGE-TO-IMAGE)
```text
[URL_FOTO_REFERENSI_USER] ultra-high definition commercial optical remastering of the input reference photograph, 100 percent faithful preservation of the exact subject facial features, eye details, hair strands, outfit textile weave, posture, and environmental background with zero alteration or morphing. Eliminating digital compression noise, motion blur, and optical aberrations, rendering authentic biological micro-pore definition, delicate vellus skin peach fuzz, crisp iris striations with natural specular catchlights, healthy sub-surface scattering skin luminosity, and tangible thread textures across garments. Masterfully captured with Hasselblad H6D-100c medium format sensor, 100mm prime lens, stopped down to f/8 for edge-to-edge tack-sharp MTF resolution clarity, perfectly balanced dynamic range with clean highlight roll-off and anchored deep shadow details, authentic tangible photographic reality, zero plastic smoothing, zero CGI artifacts --iw 2.0 --cref [URL_FOTO_REFERENSI_USER] --cw 100 --style raw --c 0 --s 25 --seed 24091367
```

---

## 🚫 NEGATIVE PROMPT (ANTI HALUSINASI & ANTI PERUBAHAN BENTUK)
altered face, modified facial structure, changed eyes, different nose, altered mouth, morphed clothing, changed pattern, modified posture, different background, digital compression, blur, pixelation, chromatic aberration, plastic skin, waxy texture, airbrushed, beauty filter, facetune, 3d render, cgi, cartoon, digital illustration, uncanny valley, over-sharpened halos, noise artifacts, watermark

---

## ⚙️ SEED & PARAMETERS
- **Image Input Slot:** `[URL_FOTO_REFERENSI_USER]` (Wajib disematkan di awal)
- **Character Reference:** `--cref [URL_FOTO_REFERENSI_USER]`
- **Character Weight:** `--cw 100` (100% kunci pakaian dan pose)
- **Image Weight:** `--iw 2.0` (prioritas absolut ke foto input)
- **Seed:** `24091367`
- **Style:** `--style raw`
- **Chaos:** `--c 0` (zero randomness)
- **Stylize:** `--s 25` (minimal stylization)

---

## ⚡ FLUX.1 COMPANION (IMAGE-TO-IMAGE / CONDITIONED REMASTER)
```text
[INPUT: REFERENCE_IMAGE_1 (MANDATORY ATTACHED PHOTO)]
An ultra-high-definition optical restoration and remaster of the exact reference photograph. Every detail of the subject's face, facial bone structure, eyes, hair, clothing, and background is preserved 100 percent identically without any morphological changes. The image quality is enhanced to match a raw medium format sensor capture, resolving genuine biological micro-pores on the skin, clear eye iris reflections, and tangible thread weaves in the fabric. Noise, compression artifacts, and soft blur are eliminated, replaced with crisp optical sharpness at f/8 aperture. Balanced natural studio lighting with authentic dynamic range and zero artificial smoothing.
```

