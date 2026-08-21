# RingMo-Agent &amp; RingMo-Claw — Project Page

Project page for two remote sensing works from the Aerospace Information
Research Institute, Chinese Academy of Sciences:

- **RingMo-Agent** — A Unified Remote Sensing Foundation Model for
  Multi-Platform and Multi-Modal Reasoning
  ([arXiv:2507.20776](https://arxiv.org/abs/2507.20776))
- **RingMo-Claw** — An Experience-Inspired Multi-Agent Framework for
  Self-Evolving Research in Remote Sensing (preprint coming soon)

## Contents

```
index.html          the whole page — figures are embedded, no build step
assets/demo.mp4     RingMo-Claw demo recording
.nojekyll           serve files as-is, skip Jekyll processing
```

`index.html` is self-contained: all CSS, JavaScript and figures live inside
the file. Open it directly in a browser, or serve the folder over HTTP.

## Publishing with GitHub Pages

1. Upload `index.html`, `assets/` and `.nojekyll` to the repository root.
2. Settings → Pages → Source → branch `main`, folder `/ (root)`.
3. The site goes live at `https://<username>.github.io/<repository>/`
   within a few minutes.

## Before publishing

Compress the demo recording — the raw capture is ~50 MB, which is slow over
a network:

```
ffmpeg -i assets/demo.mp4 -c:v libx264 -crf 28 -preset slow \
       -vf scale=1280:-2 -c:a aac -b:a 96k assets/demo-small.mp4
```

Then replace `assets/demo.mp4` with the compressed file. Expect 5–8 MB with
no visible loss of quality.

## Credits

Figures are taken from the corresponding papers.
