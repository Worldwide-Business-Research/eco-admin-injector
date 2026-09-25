# ECO Admin Block Injector — Chrome Extension

Paste a full HTML file and automatically split it into separate page_content blocks in ECO Admin. Each `.container` or `.container-fluid` becomes its own block.

---

## Install

1. Open Chrome and go to `chrome://extensions`
2. Enable **Developer mode** (top right toggle)
3. Click **Load unpacked**
4. Select this folder (`eco-admin-injector`)
5. The extension icon appears in your toolbar

---

## How to use

1. Navigate to an ECO Admin page editor (the page with Page Regions)
2. Click the extension icon in your toolbar
3. Paste your full HTML into the text area
4. Click **Parse blocks** — each `.container` / `.container-fluid` is detected and auto-named from its heading
5. Review and rename blocks if needed (click **preview** to see the HTML)
6. Click **Run all → CMS** — it adds each block one by one automatically

---

## Notes

- Only works on `ecoadmin.wbresearch.com`
- Blocks are added to the **page_content** region
- Auto-naming pulls the first `h1/h2/h3` heading inside each block
- You can stop mid-run with the **Stop** button
- If a block errors, you'll be asked whether to continue or abort

---

## Changelog

### 2026-09-25
- Added an **Enable existing** button to bulk re-enable disabled blocks (mirrors the existing Disable button).
- Added an **Activity log** panel — every add/disable/enable/delete action is recorded locally (timestamp, section, block name), with a **Restore** link on delete entries to re-inject the saved HTML.
- Replaced the plain blue toolbar icon with a syringe design.
