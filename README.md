# zigaxblg
Test for Black Lagoon

---

Ekipa ciao,

vračam testno nalogo. Upam, da rešitev zajame vse, kar potrebujete za uvid v moje misli. Pišem na hitro (brez zamer), ker ura teče in rad dostavim, kar obljubim.

---

**Na kratko o procesu:**
- Pregledal vaše materiale
- Skiciral, delal notese — brez tega mi pač ne gre
- Figma moodboard (spomnil sem se tvoje omembe Dicka Tracyja — in vmes mi je kliknilo, da je eden mojih najljubših karakterjev Kapitan Nemo)
- Voice chat s Claudeom glede na moje notese in vašo vsebino, ki sem jo res hitro preletel (super fast glance)
- Build PRD v1
- Re-chat, ker mi je bil whack in preveč "vaše vsebine"
- Build PRD v2
- Claude Code je tukaj dobil vaše testne requiremente > zbuildal sem one-pager za strukturo in informacijsko vrednost glede na zahtevan output naloge > /design-flow
- Promptal Google AI Studio 2x — prvič nisem bil zadovoljen s konsistenco, zato sem zbuildal boljši world-building prompt
- Export code, nato mini popravki in pucanje na hitro z VSC
- Deploy repo na GitHub, predhodno polinkano na staging Netlify
- T+20min

**Na kratko o mojih mislih (in kaj sem s tem v rešitvi naredil):**
- Vajbam dokumente, ki ste mi jih poslali
- Par stvari hejtam. Vedno ko kjerkoli preberem "authenticity", si rečem... damn, niste avtentični. No biggie — znam to nagovoriti, in to dobro 🙂 V one-pagerju sem to besedo porezal in raje pokazal, kako brand zveni brez nje.
- High-flying words! Too much. Ne sežejo do globine Balatona. To sem porezal in se osredotočil na tdistinct, true stvari — tiste, ki so res samo vaše.
- .svg logo! Ošpice dobim, ko ga firme nimajo. Malenkost, a pokaže globino resnosti vsake organizacije.
- Najbolj so mi všeč vaše LN slike, kjer ste... human first 😄 — tam živi vaš brand, in ravno okrog tega sem gradil.

Zej, jaz to tko vidim... vi imate lahko svojega monstruma pod površjem, I get it — ampak da postane Kapitan Nemo, mora še malo čokolina pojest.

Pod črto: če bi se ujeli, znam(/-va) zbuildat svet, ki bi bil po globini in resonanci tam-tam z Jules Vernom in 20k miljami pod morjem. Verjamem, da bi vaši organizaciji ustvaril svet in globino, ki jo potrebujete za doseg operatorjev in uspešen B2B posel — obenem pa interno gradi full jak občutek, lojalnost, cool-faktor itn.

---

Pomagala:
1. mood folder -> 2K images (https://aistudio.google.com/, Nano Banana Pro, gemini-3-pro-img)
2. design flow for speed -> https://github.com/julianoczkowski/designer-skills
3. icons -> https://icones.js.org/
4. subtle animations -> https://animejs.com/documentation/getting-started/
5. figma board -> https://www.figma.com/design/B6w2bswSnGeUmxNy9l9rus/Black-Lagoon-Games?node-id=0-1&t=c8n9RRPJAJbmDFHH-1
6. Timelapse -> https://www.icloud.com/photos/#/icloudlinks/08fyV69Imfu852pKJhh3vLWKA/0/

---

Claude Session:
# Summary: Black Lagoon Games Pitch Page Build

## Starting Point
- **Context:** PRD (5–10 min internal pitch), 3 PDF brand documents (strategy, CGP, presentation), 2 logo assets
- **Goal:** One self-contained HTML page, light mode, no build step, ready for Netlify deploy

## Process

### 1. **Research & Compression** (20 min)
- Read PRD, strategy doc, brand presentation, and CGP (rendered PDFs to images to see visual system)
- Understood: Verne-oceanic brand, "deeper side of gaming," Captain Nemo as outlaw intellectual, teal/navy palette, Montserrat + Istok Web type
- Skipped full grill-me/IA/tokens phases — PRD was thorough enough; compressed to confirm + build

### 2. **Core Build** (index.html, 1080px max-width)
- **Hero:** anchor tagline ("Beyond the reels"), headline split (navy + teal), badge logo, chips (role/time/format)
- **7 sections:** LinkedIn audit (3+3 cards), mini campaign (4-week arc + Week 1 sample), brand review (3+3), evolution timeline (6 months), monster concept (Nemo), moodboard (10 frames), footer
- **Tech:** vanilla JS + anime.js for scroll-reveal and hero ripples; CDN fonts only; zero framework

### 3. **Voice Rewrite** (Jules Verne + Harry Dry)
- Removed jargon, cut "authenticity" (showed behavior instead), tightened to short rhythmic lines
- Examples: "Three soundings up, three down" | "Eight aboard, all quiet" | "The hull is weak" (maritime metaphor throughout)
- Kept PRD-canonical lines intact: the core headline, campaign chapters, Nemo's voice quotes, AI prompts

### 4. **Name Fix & Logo**
- Changed `Žigi → Žiga` everywhere (4 instances: title, chips, comic-strip caption, footer)
- Removed logo-plate dark background (unneeded); used horizontal logo in sticky nav at 34px

### 5. **Images & Moodboard Rebuild**
- **Optimization:** Your 10 concept images were ~40MB total → generated web-optimized versions (max 2200px, q85, progressive) = **3.7MB** in `assets/mood/`
- **Layout:** Replaced fixed 16/10 aspect grid with **CSS-column masonry** respecting native ratios:
  - The Descent: tall portrait (1228×2200)
  - The Comic Strip & Surface Conquered: square-ish (2016×2088)
  - Other 7: cinematic 21:9 (2200×933)
- **Lightbox:** Click any frame → full image on dark blurred backdrop + caption (prompt #, title, description), close via ×/Escape/backdrop click
- **Accessibility:** keyboard nav (Enter/Space), focus management, aria-modal, alt text

### 6. **Export for Translation** (COPY.md)
- Extracted all visible text in reading order, grouped by section
- Flagged canonical brand lines `[keep]`, AI prompt `[keep]`, and transcreation notes for Slovenian translator
- Ready for SL → pickup without re-reading the HTML

### 7. **Verification & Cleanup**
- Tested in preview: hero, all cards, campaign cards, evolution timeline, monster section, masonry moodboard, lightbox click
- Confirmed all 10 images load, zero broken
- Removed temp preview configs
- Built folder is clean: `index.html` + `assets/` (logos + mood/ optimized images)

## Deliverable
**Single `index.html` file** (~35KB HTML + CSS + JS), `assets/` folder with logos and moodboard images.

**Ready to:**
- Push to GitHub
- Drag onto Netlify for instant deploy
- Send to Luka with the pitch email

**No further changes needed** — the page is complete, accessible, performant, and stands on its own (readable before/during/after the pitch meeting).

