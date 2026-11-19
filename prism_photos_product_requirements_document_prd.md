# Photon Web — Product Requirements Document (PRD) & Product Brief

**Version:** 1.1
**Status:** Approved / In Active Development
**Author:** Product & Design Architecture
**Target Release:** Q1 2027

---

## 1. Executive Summary & Vision

## Mission Statement
Making art with A.I. is cheating. It requires no skill, no time, no effort. We assign a much higher value to **handmade** art for the same easons.

Art made and published using the Photon Suite of apps is **guaranteed** to be human-made.

## Photon Web
**Photon Web** is a public photo gallery where users can publish photos captured using their [Photon Photo](#photon-photo) camera app. **Photon Web** only publishes photos captured using **Photon Photo**.

Unlike conventional social media apps that aggressively compress imagery, strip technical metadata, and throttle reach behind engagement algorithms, Photon Web is built on the philosophy of **"Curate Without Noise."** It delivers:
- Lossless master archiving (Camera RAWs `.ARW`, `.DNG`, `.CR3`, `.IIQ` and master 16-bit WebP/JPEGs).
- Full technical transparency (deep EXIF inspection, lens optics, camera rigs, and geo-data).
- Zero algorithmic feed friction, no ad trackers, and sovereign creator vaults.
- Multi-modal public portfolio presentations (Desktop dashboards, immersive full-screen slideshows, and responsive mobile layouts across 1-column editorial, 2-column masonry, and 3-column Gallery compact grids).

---

## 2. Target Audience & Personas

| Persona | Primary Needs & Frustrations | Photon Web Solution |
| :--- | :--- | :--- |
| **The Gallery Fine-Art Photographer** *(e.g., Alex Rivera)* | Frustrated by Instagram/Twitter compression, lack of color space fidelity (AdobeRGB / ProPhoto), and lost EXIF data. | Uncompressed cloud vault storage, verified creator badge, deep EXIF inspection chips, medium format master badges (`100MP Hasselblad`). |
| **The Collector / Art Director (Visitor)** | Needs clean, high-resolution viewing, ambient slideshows for studio monitors, and transparent lens/capture specs without intrusive social clutter. | Dedicated full-screen ambient slideshow mode (4-second timed transitions), public stream filters, fast Google SSO conversion. |
| **The Mobile Creator & Casual Viewer** | Needs responsive browsing on mobile devices without losing visual hierarchy or grid flexibility. | Three distinct mobile viewing layouts: 1-column editorial stream, 2-column masonry, and 3-column gallery contact sheet. |

---

## 3. Core Product Features & Architectural Modules

### 3.1 Authentication & Account Management
- **Google OAuth 2.0 Single Sign-On:** Fast, friction-free login and registration for photographers.
- **Public vs. Private** Pictures marked `public` are published automatically, `private` photos remain unpublished.

### 3.2 Digital Asset Ingestion & Gallery Engine

- **Supported Formats:** `.jpg` and `.png` to start, with other formats planned: Camera RAW files (`.ARW`, `.DNG`, `.CR3`, `.IIQ`), high-depth JPEGs, and lossless WebP.
- **Automated EXIF Extraction:** Instant parsing of camera body, lens, focal length, aperture ($f$-stop), shutter speed, ISO rating, color temperature, and GPS coordinates, and more.
- **Full Gallery Export:** One-click bulk export feature packaging originals (`.tar or .zip`).

### 3.3 Public Feed, Portfolio & Sorting Matrix
Te search feature is used by visitors to find `public` content using fields such as `username`, `id`, `filename`, `tag`, `location`, `hash`, `key-value`, etc. Authenticated creators can also search content labelled `private`.

Visitors can sort a feed of `public` (published) photos using flexible organization mechanics, while creators can sort `private` photos as well:
- **Chronological Sorting:** Newest first vs. Oldest first with session-based date groupings (e.g., *Nov 1, 2026 · Petrolia*).
- **Geographic Sorting:** Dynamic location indexing using Google Maps API.
- **Lens & Rig Sorting:** Grouping by optical rig (e.g., *Sony FE 35mm F1.4 GM*, *Leica Summilux 28mm f/2.0*, *90mm Macro*).
- **Random Shuffle:** Algorand-neutral serendipitous shuffling for open discovery.
- **Series / Curated Folio Tagging:** Horizontal quick-filter chips (*Architectural Monoliths*, *Photon Web & Light Studies*, *Night Reflections*).

### 3.4 Multi-Surface Viewports & Layout Options
- **Desktop (`1440px+`):** Fixed left navigation sidebar, global search bar (`⌘K`), header utility row, multi-column gallery grid.
- **Mobile Responsive (`390px`):**
  1. **1-Column Feed:** Full-width photographic cards.
  2. **2-Column Masonry View:** Dynamic vertical rhythm with staggered aspect ratios (4:5, 9:16, 1:1, 16:9).
  3. **3-Column Compact Grid:** High-density contact sheet layout.
- **Full-Screen Slideshow Mode:** Ambient, zero-chrome theater presentation with 4-second cross-fade transitions and keyboard navigation (`←` / `→`).
- **Relevent Information** such as exif data, publish date, filename, owner, location, description, etc are hidde by default so as not to distract users with a busy ui. Tapping the `i` (information) badge reveals pertinant information.

---

## 4. Information Architecture & Site Map

```
Photon Web Platform
│
├── Public Visitor Experience
│   ├── /stream (Public Stream & Discovery Feed)
│   ├── /@username (Artist Public Profile & Portfolio)
│   │   ├── 1-Column Feed View
│   │   ├── 2-Column Masonry View
│   │   └── 3-Column Compact Thumbnail View
│   ├── /photo/:id (Photo Detail Modal & EXIF Deep-Dive)
│   └── /slideshow (Full-Screen Ambient Slideshow Mode)
│
└── Authenticated Creator Workspace
    ├── /library (All Photos Grid & Vault Management)
    ├── /albums (Curated Folios & Series Management)
    ├── /favorites (Starred Gallery Negatives)
    ├── /vault (Encrypted Storage & Passcode Lock)
    └── /settings/profile (Account, Public Presence & OAuth Safeguards)
```

---

## 5. Non-Functional & Technical Requirements

| Dimension | Specification |
| :--- | :--- |
| **Performance** | Sub-100ms client-side filter switches; progressive image loading with blur-hash placeholders; lossless thumbnail pyramid generation. |
| **Color Fidelity** | Native Display P3 and sRGB color profile retention with zero automatic contrast or sharpening post-processing. |
| **Privacy & Security** | Client-side AES-256 vault encryption; strict separation of public stream routes from private vault storage nodes (`CA-TOR-01`). |
| **Accessibility** | Full WCAG 2.1 AA compliance, high-contrast dark theme mode (`#0B0F12` background, `#F1F5F9` text), full keyboard navigable grids (`⌘K` command palette, arrow key slideshow). |

---

## 6. Project Roadmap & Milestones

- **Phase 1:** Desktop web app will have a feed of recently published photos by all users, full-screen slideshow mode, photo detail view, user profile pages. Authenticated users can turn `public` view on to see thier profile and feed pages the same way visitors see them, i.e. with `privte` content filtered out.
- **Phase 2 (Completed):** Mobile responsive layout suite (1-Column Feed, 2-Column Masonry, and 3-Column Compact Grid).
- **Phase 3 (Next):** Direct cloud-sync integration. The Android companion app [Photon Photo](#photon-photo) will upload selected photos directly to `cloudflare images cdn` storage using Ktor or something simliar. A new custom domain requires mapping (`photonphoto.app`).
