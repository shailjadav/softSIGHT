# Monocular Vision Based Control Framework for Grasping - Project Page

Static academic project page for the paper *"Monocular Vision Based Control Framework
for Grasping"* (Shail Jadav, Dongheui Lee - TU Wien / DLR).
[arXiv:2607.07897](https://arxiv.org/abs/2607.07897)

## Structure

```
index.html                 # single-page site
.nojekyll                  # tell GitHub Pages to serve static/ as-is
static/
  css/style.css            # styles
  images/                  # figures (converted from the paper) + video poster
  videos/supplementary.mp4 # supplementary video (web-optimized)
  pdf/paper.pdf            # paper PDF
```

## Hosting on GitHub Pages

1. Create a repository and push these files:
   ```bash
   git add index.html README.md .nojekyll static
   git commit -m "Add project website"
   git push origin main
   ```
2. In the repo, go to **Settings → Pages**, set **Source: Deploy from a branch**,
   branch `main`, folder `/ (root)`, and save.
3. The site publishes at `https://<user>.github.io/<repo>/`.

The `.nojekyll` file ensures the `static/` directory is served untouched.

## Regenerating assets

- Figures come from the AIM 2026 slide deck (`Aim2026_SJ_v1_F.pptx`) and the paper PDFs,
  flattened/resized with `sips`.
- `static/videos/hero.mp4` is a muted loop of the 2×2 demo grid; `static/videos/supplementary.mp4`
  is the full talk video - both re-encoded from `lknd (1).mp4` with `ffmpeg` (H.264, faststart).
- Raw source videos (`lknd (1).mp4`, `AIM26_0597_VI_fi (4).mp4`) are excluded via `.gitignore`.

Total deployed payload is ~10 MB.
