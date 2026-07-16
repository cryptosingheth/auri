# Auri Hero Montage — Google Flow / Veo 3 Prompt Pack

**Goal:** Replace "pretty but concept-weak" clips with lifestyle clips where **gold is visibly the money being used** — bought, spent, gifted, sent, and grown. Every clip must survive muted, looping, ~4–5s, behind the headline **"Gold has been sleeping for 5,000 years."**

**The one rule that fixes the founder's critique:** In every clip, gold must *physically become* the transaction — a bar dissolving into the light that flows into a phone and out as a card tap; grams landing on a jeweller's scale; a bangle's glow drifting into a granddaughter's phone. No abstract "golden sparkles near a happy person." The gold has to *do the paying.*

---

## 0. How to use this pack in Google Flow

1. Open Flow → new generation → **Veo 3 (quality)** → aspect ratio **16:9**.
2. Copy ONE clip's paste-ready block (in the code fence) into the prompt field. Each block is already fully styled — do not add the style tail on top of it.
3. Paste the **Negative Prompt** block (Section 1) into Flow's negative field **every time**.
4. Generate **2–3 variations** per clip; pick the take where the gold-transformation reads clearly and hands/faces are clean.
5. For hero-critical clips you also want vertical, regenerate natively at **9:16** rather than cropping (Section 4 covers crop fallback).
6. Run winners through the ffmpeg block (Section 4) to trim, grade-match, strip audio, and compress.
7. **Advanced (brand accuracy):** In Flow, add a reference image of the real Auri card / a real minted gold bar as an *ingredient* so the prop matches your brand instead of a generic gold blob.

**Watermark note:** If your Flow tier stamps a visible "Veo" mark bottom-right, keep the money-action out of that corner and plan to crop ~6% or cover it with the site's lower-third gradient. (SynthID is invisible and fine.)

---

## 1. Prompt Grammar — the reusable style system

### 1a. STYLE TAIL (append ONLY when writing your own new clips)
Each of the ten clips below already contains this styling. Use this tail as a template when you author new ones:

```
Shot on a cinema camera, spherical prime lens, shallow depth of field, subtle
natural handheld micro-movement; soft diffused natural light with warm practical
accents; warm cream-and-champagne color grade, deep plum-tinted shadows, gentle
highlight halation, fine 35mm film grain; slow contemplative pacing with a single
deliberate camera move; premium, warm, quietly cinematic mood; 8 seconds, 16:9
landscape; keep the key action in the lower third or to one side, leaving calm
negative space for a headline overlay; no on-screen text, no readable UI, no
captions, no logos or watermarks; ambient room tone only, no spoken dialogue.
```

**Why "no dialogue":** clips are muted anyway, and forcing speech makes Veo warp lips and invent garbled subtitles. Keep people doing quiet, deliberate actions.

### 1b. NEGATIVE PROMPT (paste into Flow's negative field EVERY time)

```
text, on-screen text, captions, subtitles, watermark, logo, brand marks,
readable user interface, UI numbers, coins raining, showers of coins, cartoon
gold, gaudy shiny CGI, fake plastic gold, glitter overlays, sparkle spam, crypto
symbols, bitcoin, neon, oversaturated, HDR look, distorted hands, extra fingers,
warped faces, deformed jewellery, cluttered center frame, fast cuts, jittery
motion, whip pans, stock-photo grin, lens dirt, extreme chromatic aberration.
```

### 1c. Fixed technical spec (applies to all)
| Parameter | Setting |
|---|---|
| Duration | 8s native (trimmed to 4–5s in post) |
| Aspect | 16:9 primary; 9:16 native regen for hero-critical clips |
| Frame rate | 24 fps (filmic) |
| Pace | ONE camera move per clip, slow; the "money moment" lands mid-clip |
| Palette | Cream / champagne / amber highlights, plum-tinted shadows |
| Texture | Fine film grain + gentle halation on the gold light |
| Text | None on screen, ever. No readable UI, no numbers. |
| Composition | Money-action off dead-center (lower third or one side) so the headline breathes; plum CSS scrim sits on top |
| Audio | Strip in post (`-an`). Prompt for ambient only, no dialogue |
| Gold-as-money motif | Physical gold → warm light → phone → real-world outcome. Never sparkles-for-vibes. |

---

## 2. The Ten Clips

> Each block below is fully styled and paste-ready. Copy the fenced text into Flow's prompt field; paste Section 1b into the negative field.

---

### CLIP 1 — "The Bar Becomes the Groceries"  *(SPEND)*

```
Macro-to-medium cinematic shot. A small cast gold bar rests in the open palm of
an East Asian man in his early thirties at a cream-toned kitchen counter in warm
morning light. The gold bar slowly dissolves into a ribbon of soft golden light
that streams upward and sinks into the screen of the phone in his other hand.
Seamless match-cut: the same man taps a matte champagne-gold payment card on a
grocery-store terminal; a brief warm glow pulses at the tap point as a paper bag
of fresh produce settles on the counter beside it. Slow dolly-in, then a gentle
rack-focus to the tap; 50mm prime, shallow depth of field, natural handheld
micro-movement. Soft diffused daylight, warm cream-and-champagne palette, deep
plum-tinted shadows, fine film grain, subtle halation on the gold light. Calm,
premium, quietly magical mood. 8 seconds, 16:9. Ambient room tone only, no
dialogue. No on-screen text, no readable interface, no logos.
```

**Why it proves the concept:** Gold literally turns into the money that pays for groceries — the single clearest "gold *is* the spend" shot in the pack.

---

### CLIP 2 — "Grams Don't Lie"  *(PROOF / REAL AUDITED GOLD)*

```
Top-down macro cinematic shot on a warm wooden jeweller's counter. A small
traditional two-pan brass balance scale holds a few grains of real gold on one
pan; a phone lies beside it. A South Asian woman goldsmith in her forties gently
taps the phone, and in response a soft stream of fine gold grains flows onto the
scale's pan until the balance settles perfectly level — physical gold and phone
matched gram for gram. Behind her, glass cases of gold jewellery glow softly.
Slow overhead push-in, then a delicate rack-focus from the phone to the settling
scale; 60mm macro, shallow depth of field. Warm tungsten-and-daylight mix,
champagne highlights, deep plum shadows, rich film grain, gentle halation on the
gold. Trustworthy, tactile, precise mood. 8 seconds, 16:9. Ambient room tone
only, no dialogue. No on-screen text, no readable numbers, no logos.
```

**Why it proves the concept:** Puts weighed physical gold and the phone side by side and shows they're the *same grams* — directly answers "is it really gold?"

---

### CLIP 3 — "The Bangle and the Grams"  *(GIFT / TRADITION — Diwali)*

```
Intimate cinematic two-shot at dusk during Diwali. An elegant South Asian
grandmother in her seventies slides a slim gold bangle onto her granddaughter's
wrist; the young woman in her early twenties smiles. The grandmother then taps
her own phone, and a small warm mote of golden light lifts from the bangle and
drifts across to settle as a soft glow inside the granddaughter's phone. Around
them, clay diyas flicker and marigold garlands fill the warm bokeh of a cozy
Canadian home. Slow arc around the two women, ending on the phone's gentle glow
reflected in the granddaughter's eyes; 35mm, shallow depth of field, candlelit
warmth. Champagne-and-amber palette, deep plum shadows, soft film grain, delicate
halation from the diyas. Tender, celebratory, timeless mood. 8 seconds, 16:9.
Ambient room tone only, no dialogue. No on-screen text, no readable interface,
no logos.
```

**Why it proves the concept:** Frames digital gold grams as the same sacred gift as a family gold bangle — proves gifting gold and bridges tradition to the app in one gesture.

---

### CLIP 4 — "It Was Gold All Along"  *(EVERYDAY SPEND — reveal / smile)*

```
Warm cinematic medium shot in a cozy Canadian café with wood counters, hanging
plants, and soft snow falling past the window. A Black woman in her early thirties
taps a matte champagne-gold card on the terminal; as she does, the card catches
the light and a faint shimmer of gold grains glows through it, as if it were a
thin slab of solid gold. The young barista glances up with a small, charmed
double-take and an easy shrug-smile, then slides over a flat white. Handheld
medium shot, slow push-in on the tap, rack-focus to the barista's reaction;
40mm, shallow depth of field. Soft window daylight, warm cream-and-champagne
palette, deep plum shadows, fine film grain, gentle halation on the card's glow.
Everyday, human, quietly delightful mood. 8 seconds, 16:9. Ambient café tone
only, no dialogue. No on-screen text, no readable interface, no logos.
```

**Why it proves the concept:** The ordinary card tap is secretly gold — proves you spend real gold anywhere, with a relatable, shareable human beat.

---

### CLIP 5 — "Same Sun, Two Kitchens"  *(REMITTANCE — match-cut)*

```
Two-part cinematic match-cut. First: a South Asian man in his late thirties
stands in a sunlit Toronto kitchen, morning light across cream cabinets; he taps
his phone and a ribbon of warm golden light streams out through the window toward
the sun. Match-cut on the glowing sun: the same golden ribbon arrives through a
window into a modest, sunlit Delhi kitchen and settles gently into the phone of
his mother, a woman in her sixties, who lifts it, smiles, and presses a hand to
her heart. Identical warm sunlight and champagne tones bind both kitchens as one
continuous beam. Slow push-in on each side with a seamless light-matched cut in
the middle; 35mm, shallow depth of field. Warm cream-and-gold palette, deep plum
shadows, soft film grain, gentle halation along the light ribbon. Loving,
connected, effortless mood. 8 seconds, 16:9. Ambient room tone only, no dialogue.
No on-screen text, no readable interface, no logos.
```

**Why it proves the concept:** A cross-border transfer becomes one unbroken beam of gold light from one family kitchen to another — proves remittance as gold, instantly usable abroad.

---

### CLIP 6 — "The Vault Opens onto the Street"  *(THESIS — gold unlocked into daily life)*

```
Symbolic cinematic tracking shot. A massive polished vault door slowly swings
open; instead of a dark chamber it reveals a warm, sun-drenched Canadian open-air
street market bustling with produce stalls, cut flowers, and a diverse crowd. A
woman in her thirties steps forward through the threshold, moving from the cool
metallic interior into golden daylight, and the camera follows her through into
the lively market. Soft motes of golden light drift from the vault out into the
street air. Smooth Steadicam push through the doorway, cool shadow into warm
light; anamorphic 40mm, shallow depth of field, gentle lens flare at the
threshold. Cool-to-warm transition landing on a champagne-and-gold palette, deep
plum shadows, film grain, soft halation in the doorway light. Liberating,
awakening, cinematic mood. 8 seconds, 16:9. Ambient market tone only, no dialogue.
No on-screen text, no logos.
```

**Why it proves the concept:** Visually argues the entire pitch — gold walks out of the vault into everyday life — the literal picture of "gold has been sleeping," now waking.

---

### CLIP 7 — "Dust Into a Future"  *(AUTO-INVEST / OUTCOMES)*

```
Tabletop cinematic shot in warm afternoon light. On a cream kitchen table, fine
gold dust lifts and swirls, self-assembling into a softly glowing, gently rising
chart of golden light. As the chart climbs, it dissolves forward and reforms into
tangible things on the same table: a neat stack of school books and a small bag
of fresh groceries. A Filipino-Canadian mother in her late thirties and her young
child watch; the child reaches out and touches the books. Slow macro push from
the swirling dust, pulling back to a warm medium two-shot; 50mm, shallow depth of
field. Soft golden-hour window light, champagne highlights, deep plum shadows,
fine film grain, gentle halation on the gold dust. Hopeful, nurturing, quietly
proud mood. 8 seconds, 16:9. Ambient room tone only, no dialogue. No on-screen
text, no readable chart numbers, no logos.
```

**Why it proves the concept:** Gold visibly grows and then *becomes* school books and food — proves that investing gold turns into real family outcomes, not an abstract line.

---

### CLIP 8 — "The Shagun Opens as Light"  *(GIFT / WEDDING)*

```
Warm cinematic close-to-medium shot at a home table covered with wedding-planning
notes, fabric swatches, and marigold petals. A South Asian couple in their late
twenties are handed an ornate red-and-gold shagun envelope by an elder's hands;
as the couple gently open it, instead of cash a soft burst of warm golden light
rises out and drifts down to settle into the phone resting between them. They
glance at each other and smile. Slow push-in on the opening envelope, rack-focus
to their faces, then to the glowing phone; 45mm, shallow depth of field. Warm
lamp-and-daylight mix, champagne-and-rose-gold palette, deep plum shadows, soft
film grain, delicate halation from the rising light. Celebratory, intimate,
auspicious mood. 8 seconds, 16:9. Ambient room tone only, no dialogue. No
on-screen text, no readable interface, no logos.
```

**Why it proves the concept:** Reimagines the traditional cash shagun as gold delivered to the phone — proves gifting gold for life's big occasions.

---

### CLIP 9 — "A Snow-Day Gram"  *(BUY in seconds — cozy Canadian)*

```
Cozy cinematic medium shot by a frosted window with soft snow falling outside a
Canadian home. A woman in her thirties in a chunky knit sweater cradles a warm
mug on the sill, then taps her phone twice; a small, soft bloom of golden light
forms just above the screen and settles gently into it — a tiny amount of gold
acquired in seconds on an ordinary snowy morning. Steam rises from the mug; a
knit blanket and a dozing cat sit nearby. Slow push-in from the snowy window to
the warm glow on her face; 50mm, shallow depth of field, gentle handheld. Cool
blue snow-light outside meeting warm champagne interior light, deep plum shadows,
fine film grain, soft halation on the phone glow. Calm, cozy, effortless mood.
8 seconds, 16:9. Ambient winter-quiet tone only, no dialogue. No on-screen text,
no readable interface, no logos.
```

**Why it proves the concept:** Buying real gold becomes a two-tap, 30-second everyday habit in an unmistakably Canadian moment — proves how easy owning gold is.

---

### CLIP 10 — "Night Shift, Sent Home"  *(REMITTANCE — sender's POV, emotional)*

```
Quiet nighttime cinematic close-up. In a dim hospital corridor lit by a single
warm lamp, a Filipino-Canadian nurse in her forties sits on a short break, tired
but tender. She taps her phone, and a warm ribbon of golden light lifts from the
screen and threads softly out through a dark window toward the distant,
snow-dusted city lights — value sent home while the world sleeps. The phone's
warm glow lights her face. Slow push-in from over her shoulder to her lit face,
then a rack-focus to the light leaving the window; 35mm, shallow depth of field.
Cool nighttime blues against the warm champagne phone glow, deep plum shadows,
fine film grain, soft halation on the light ribbon. Weary, loving, quietly heroic
mood. 8 seconds, 16:9. Ambient hospital-quiet tone only, no dialogue. No
on-screen text, no readable interface, no logos.
```

**Why it proves the concept:** Puts a real worker's love on screen as gold light sent home overnight — proves remittance emotionally, from the sender's side.

---

### Coverage map (for reference)
| Value prop | Clip(s) |
|---|---|
| Buy gold in 30s | 9 |
| Spend via gold card | 1, 4 |
| Real audited gold / grams | 2 |
| Gift gold | 3, 8 |
| Remittance abroad | 5, 10 |
| Auto-invest / growth → outcomes | 7 |
| Brand thesis ("gold set free") | 6 |

> **Deliberately omitted from the hero loop:** *borrow cash against gold, 5x boost, agent/MCP automation.* These are logic/UI features that don't read as a wordless 4s lifestyle beat and would need on-screen text. Show them in product sections with real UI, not the muted hero montage.

---

## 3. Montage Plan

### 3a. Generate these 6 first
Chosen to cover every core value prop once, maximize concept-proof, vary scenes, and span the diversity brief:

| # | Clip | Prop proven |
|---|---|---|
| 1 | **9 — A Snow-Day Gram** | Buy |
| 2 | **2 — Grams Don't Lie** | It's real gold |
| 3 | **1 — The Bar Becomes the Groceries** | Spend |
| 4 | **3 — The Bangle and the Grams** | Gift |
| 5 | **5 — Same Sun, Two Kitchens** | Remit |
| 6 | **7 — Dust Into a Future** | Grow / outcomes |

*(Second batch, once the loop is proven: 6 Vault, 4 Barista, 8 Shagun, 10 Night Shift.)*

### 3b. Hero loop order + why
The loop should feel like gold **waking up and flowing into a life** — mirroring the headline. Arc: **acquire → verify → spend → gift → send → grow → (loop back to acquire).**

| Order | Clip | Beat in the story | Trim target (from 8s take) | Keep this segment |
|---|---|---|---|---|
| 1 | 9 — Snow-Day Gram | Gold enters a life | **~2.5s → 7.0s** (≈4.5s) | The two taps → golden bloom settling into the phone. Drop the window-only intro. |
| 2 | 2 — Grams Don't Lie | Proof it's real | **~2.0s → 6.5s** (≈4.5s) | Tap → grains flow → scale settles level. |
| 3 | 1 — Bar → Groceries | Spend it | **~1.5s → 6.0s** (≈4.5s) | Bar dissolving → light into phone → the match-cut card tap. Keep the match-cut intact. |
| 4 | 3 — Bangle & Grams | Give it | **~2.5s → 7.0s** (≈4.5s) | Bangle onto wrist → mote drifts into granddaughter's phone. |
| 5 | 5 — Same Sun, Two Kitchens | Send it far | **~1.5s → 6.5s** (≈5.0s) | Toronto tap → ribbon out window → match-cut → arrival in Delhi. Keep the match-cut centered. |
| 6 | 7 — Dust Into a Future | It grows into a future | **~2.0s → 6.5s** (≈4.5s) | Dust swirl → chart rises → reforms into books/groceries. Warm ending flows back into Clip 9's cozy open. |

**Trim principles:** land ON the transformation; start ~0.5s before the gold moment, end ~0.5s after it settles; pick in/out frames where motion is calm so the 0.5s crossfades between clips read as one continuous film. Total loop ≈ **25s** after 0.5s crossfades.

**Headline-safe framing:** headline sits center-upper with the plum scrim on top. Where a clip's money-action is dead-center (macro Clips 1, 2, 7), the scrim darkens it enough — but favor takes where the transformation sits slightly lower/off-axis so the words breathe.

---

## 4. Encoding — ffmpeg

Assumes Veo/Flow exports are 8s, 16:9, ~24fps, with audio. All commands **strip audio (`-an`)** and normalize to 1080p.

Working layout:
```
raw/     # Flow exports:  09_snowday.mp4, 02_grams.mp4, ...
trim/    # step 1 output
web/     # final web assets (mp4 + webm)
vert/    # 9:16 variants
```

### 4a. Step 1 — Frame-accurate trim + strip audio + normalize to 1080p24
`-ss`/`-to` **after** `-i` = frame-accurate. Adjust timecodes per the table in 3b. CRF 18 here = near-lossless intermediate before grading.

```bash
ffmpeg -i raw/09_snowday.mp4 -ss 00:00:02.5 -to 00:00:07.0 -an \
  -vf "scale=1920:1080:force_original_aspect_ratio=increase,crop=1920:1080,fps=24,format=yuv420p" \
  -c:v libx264 -crf 18 -preset slow trim/09_snowday_trim.mp4
```

### 4b. Step 2 — Grade-match to the Auri look + web compress (one pass)
Unifies all clips to champagne highlights + plum shadows + film grain + soft vignette, then compresses for web. This is the master web asset.

```bash
ffmpeg -i trim/09_snowday_trim.mp4 -an \
  -vf "eq=contrast=1.06:brightness=0.005:saturation=1.06:gamma=0.98,\
colorbalance=rs=0.03:gs=-0.02:bs=0.03:rm=0.02:gm=0.00:bm=-0.01:rh=0.05:gh=0.02:bh=-0.05,\
curves=preset=lighter,\
vignette=angle=PI/5,\
noise=alls=7:allf=t+u,\
format=yuv420p" \
  -c:v libx264 -crf 22 -preset slow -movflags +faststart web/09_snowday_web.mp4
```

**What each filter does:**
- `eq` — gentle contrast/gamma lift, mild saturation bump.
- `colorbalance` — the Auri grade: **warm highlights** (`rh+ bh-`), **plum shadows** (`rs+ gs- bs+`). This is what makes every clip feel like one film.
- `curves=preset=lighter` — soft filmic lift in the mids.
- `vignette` — subtle edge fall-off that matches the cinematic scrim.
- `noise=alls=7:allf=t+u` — fine temporal film grain (raise to 9–10 for more, drop to 4–5 for less).
- `format=yuv420p` — web/browser compatibility.

> **Compression headroom:** because the site lays a dark plum scrim + film grain + headline over the video, you can push **CRF 24–26** for the background and barely see it — smaller files, faster hero paint. Keep CRF 20–22 only if you also cut standalone social versions from these.

### 4c. Step 3 — Alt web codecs (smaller files, broad support)
```bash
# VP9 / WebM — best size for a background hero
ffmpeg -i web/09_snowday_web.mp4 -an -c:v libvpx-vp9 -crf 33 -b:v 0 -row-mt 1 \
  -pix_fmt yuv420p web/09_snowday_web.webm

# HEVC / H.265 — small, Safari-friendly
ffmpeg -i web/09_snowday_web.mp4 -an -c:v libx265 -crf 28 -tag:v hvc1 -preset slow \
  -pix_fmt yuv420p web/09_snowday_web_h265.mp4
```
Serve WebM first with the H.264 mp4 as fallback in a `<video>` source list. **Target ≈ 1–3 MB per 4.5s clip** at 1080p.

### 4d. Step 4 — Poster frame (first paint before video loads)
```bash
ffmpeg -ss 00:00:01.5 -i web/09_snowday_web.mp4 -frames:v 1 -q:v 2 web/09_snowday_poster.jpg
```

### 4e. Step 5 — Stitch the 6-clip montage with 0.5s crossfades
All inputs must be same res/fps (they are, after 4a/4b). Offsets assume ~4.5s clips + 0.5s crossfade; recompute if your trims differ (`offset = running_total − 0.5`).

```bash
ffmpeg \
  -i web/09_snowday_web.mp4 -i web/02_grams_web.mp4 -i web/01_groceries_web.mp4 \
  -i web/03_bangle_web.mp4 -i web/05_twokitchens_web.mp4 -i web/07_dust_web.mp4 \
  -filter_complex "\
[0][1]xfade=transition=fade:duration=0.5:offset=4.0[a];\
[a][2]xfade=transition=fade:duration=0.5:offset=8.0[b];\
[b][3]xfade=transition=fade:duration=0.5:offset=12.0[c];\
[c][4]xfade=transition=fade:duration=0.5:offset=16.0[d];\
[d][5]xfade=transition=fade:duration=0.5:offset=20.0[e]" \
  -map "[e]" -an -c:v libx264 -crf 22 -preset slow -movflags +faststart \
  web/auri_hero_montage.mp4
```
**Seamless loop tip:** the loop opens on Clip 9 (calm snowy window) and closes on Clip 7 (warm gold settle), so a plain `loop` on the `<video>` reads clean. For an extra-invisible seam, add a 400ms CSS opacity dip at loop point, or crossfade the montage's tail back into its head with one more `xfade`.

### 4f. Step 6 — Vertical 9:16 variant (center-safe crop)
Clips were prompted with center-safe action, so a center crop works:
```bash
ffmpeg -i web/09_snowday_web.mp4 -an \
  -vf "crop=ih*9/16:ih:(iw-ih*9/16)/2:0,scale=1080:1920,format=yuv420p" \
  -c:v libx264 -crf 22 -preset slow -movflags +faststart vert/09_snowday_vertical.mp4
```
- To reframe off-center clips (e.g., the two-kitchen match-cut), change the crop x-offset from `(iw-ih*9/16)/2` to a manual value.
- **Better for hero-critical verticals:** regenerate natively at 9:16 in Flow — cropping throws away the wide composition and can clip the gold-transformation.

### 4g. Batch — grade + compress every trimmed clip
```bash
#!/usr/bin/env bash
set -euo pipefail
GRADE="eq=contrast=1.06:brightness=0.005:saturation=1.06:gamma=0.98,\
colorbalance=rs=0.03:gs=-0.02:bs=0.03:rm=0.02:gm=0.00:bm=-0.01:rh=0.05:gh=0.02:bh=-0.05,\
curves=preset=lighter,vignette=angle=PI/5,noise=alls=7:allf=t+u,format=yuv420p"

mkdir -p web
for f in trim/*_trim.mp4; do
  name=$(basename "$f" _trim.mp4)
  ffmpeg -y -i "$f" -an -vf "$GRADE" \
    -c:v libx264 -crf 22 -preset slow -movflags +faststart "web/${name}_web.mp4"
done
```

---

## 5. QA checklist before a clip ships to the loop
- [ ] Is gold **visibly doing the paying/gifting/sending** — not just floating near a happy person?
- [ ] Hands, faces, jewellery clean (no extra fingers, no warped bangles)?
- [ ] No accidental readable text/UI/numbers (regenerate if Veo invented any)?
- [ ] Grade matches the champagne/plum family after 4b?
- [ ] Reads in ~4.5s, muted, with the money-moment mid-clip?
- [ ] Headline area stays calm behind the plum scrim?
- [ ] Bottom-right clear of any Veo watermark (or cropped/covered)?
