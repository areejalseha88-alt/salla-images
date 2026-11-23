# salla-images

Product images for the Salla store. All files are named by product **SKU**; an extra image of the same product is `SKU-1`, `SKU-2`, ...

| Folder | Contents |
|---|---|
| `raw/` | Original source images (pharmacy downloads and Sherif's own photos), untouched |
| `main/` | Main store image: pure white background, product 53% of frame, soft shadow |
| `cutout/` | Transparent product cutouts sent to Claid |
| `scenes/` | Raw Claid scenes (no text). the generation tool never calls Claid for a SKU that already has a scene or promo |
| `promo/` | Promotional gallery images with the store logo badge; `promo/clean/` = same images without logo |
| `images/` | Legacy files named by Salla product id — already linked in Salla, kept as-is |

Flow: Salla product → `raw/` → processing (local tool or Claid) → `main/` or `promo/` → after Sherif's review, uploaded to Salla from the raw GitHub URL.
