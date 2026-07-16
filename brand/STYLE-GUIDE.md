# Auri — Design Style Guide

Extracted from the four product prototypes (`Final/Auri Web App v2.html`, `Auri Mobile App.html`, `Auri web Auth login.html`, `Auri Mobile Web.html`) by an automated Playwright crawl on 2026-07-16. All values below are **measured** — computed styles aggregated by frequency across the desktop app, mobile app, auth flow and mobile-web variant, plus the raw CSS of each bundle. Screenshot evidence lives in `Website (New)/assets/styleguide-crawl/` (48 captures).

---

## 1. Philosophy

Six principles the prototypes apply everywhere:

1. **Calm, light canvas.** The product lives on a near-white lavender-gray (`#F6F5F8`) with pure-white cards separated by 1px hairlines — never heavy borders, never dark chrome. Color exists only where it carries meaning.
2. **Every number is monospaced.** All figures — balances, prices, percentages, dates in ledgers — render in Geist Mono (web) with tight negative tracking at display sizes. Text is Geist; money is mono. Numbers *are* the interface.
3. **Semantic color discipline.** Gold = the asset and its proof ("Backed 1:1" chips, reserve badges). Plum (accent) = user action. Green = money-in, safety and success. Amber = caution / prerequisites ("ID required"). Red appears only for losses and errors. No decorative color.
4. **Soft geometry, sized to the component.** Radii scale with what they wrap: 7–9px chips, 10–12px buttons and cards (12px is the single most common radius on screen), 16–24px modals and sheets, 99px pills, circles for avatars and the FAB.
5. **Quiet elevation.** Resting cards get a 1px hairline plus a 1–2px micro-shadow you can barely see. Real depth is spent only on transient layers: dropdown menus, modals, the FAB and its accent-colored glow.
6. **One dark surface for power.** Everything financial is light; the single deliberate exception is the near-black "programmable" surface (Automate / Connect an agent / MCP·CLI·API panels) with a mono code block and a pale-accent eyebrow. Dark = developer power, light = money.

A seventh, structural observation: **branded at the core, native at the edges.** The web app is 100% Geist/Geist Mono; the mobile-app prototype deliberately switches UI text to the system stack (SF, weights up to 800) for a genuine iOS/Android feel while keeping the same tokens, semantics and layout language.

---

## 2. Color system

### 2.1 Neutrals (light theme)

| Token | Value | Measured use |
|---|---|---|
| Canvas | `#F6F5F8` | Page/body background everywhere |
| Surface | `#FFFFFF` | Cards, modals, inputs, secondary buttons (most frequent bg: 110 hits) |
| Well / rail | `#EFEEF4` · `#EFEEF3` | Segmented-control rails, inset wells, progress tracks |
| Well hover | `#ECEAF1` · `#E9E7F0` | Pressed / hover state of wells |
| Ink | `#15161B` (`rgb(21,22,27)`) | Primary text; also the **dark neutral fill** ("Buy" button, active timeframe chip) |
| Text strong-secondary | `#42454E` | Secondary-button labels, emphasized body |
| Text secondary | `#6B6F79` / `#6B6F7B` | Body copy |
| Text muted | `#8A8F9C` · `#9CA0AB` | Sub-labels, placeholders (the single most frequent text color) |
| Text faint | `#B4B7BF` | Disabled hints, tertiary meta |
| Hairline default | `rgba(20,21,27,.07)` @ 1px | Card borders (55 hits — the standard border) |
| Hairline subtle | `rgba(20,21,27,.05)` @ 1px | Row dividers |
| Hairline interactive | `rgba(20,21,27,.12)` @ 1px | Secondary buttons, filter chips |
| Hairline input | `rgba(20,21,27,.14)` @ 1px | Text inputs |

### 2.2 Accent ("action") — themable via `[data-accent]`

The accent is defined as four CSS custom properties and swapped by a single attribute. **Plum is the default.** Changing `data-accent` retints nav states, charts, primary buttons, FAB, icon tiles — verified by capture (`desktop-accent-*.png`).

```css
[data-accent="plum"]     { --accent:#A12C66; --accentDk:#852152; --soft:rgba(161,44,102,.10); --soft2:rgba(161,44,102,.05) }
[data-accent="violet"]   { --accent:#6A40E6; --accentDk:#5733C9; --soft:rgba(106,64,230,.10); --soft2:rgba(106,64,230,.05) }
[data-accent="wine"]     { --accent:#8E2D43; --accentDk:#752335; --soft:rgba(142,45,67,.10);  --soft2:rgba(142,45,67,.05) }
[data-accent="rosegold"] { --accent:#B26B73; --accentDk:#95565D; --soft:rgba(178,107,115,.12);--soft2:rgba(178,107,115,.06) }
[data-accent="sky"]      { --accent:#0E9CD4; --accentDk:#0B7FAE; --soft:rgba(14,156,212,.11); --soft2:rgba(14,156,212,.055) }
```

Usage: `--accent` for fills/text/lines, `--accentDk` for hover/pressed, `--soft` for selected-state washes (active nav item, icon tiles, selected payment row), `--soft2` for the faintest tint (selected card bg). On-dark pale accent for eyebrows: `#E6A8CC`.

**Do:** use accent for exactly one primary action per view, active nav/selection states, the FAB, chart lines.
**Don't:** use accent for positive amounts (that's green), for the gold asset (that's gold), or as decorative large fills.

### 2.3 Semantic colors

| Meaning | Token | Soft fill | Text-on-soft | Where seen |
|---|---|---|---|---|
| Money-in / safe / success | `#16A06A` | `rgba(22,160,106,.10–.12)` | `#16A06A` | `+$250.00` amounts, "Safe" LTV pill, "Add" button, "Connected"/"Active"/"1 active plan" badges, health bar |
| Gold / asset / proof | `#C4A25C` family | `rgba(196,162,92,.13)` bg + `rgba(196,162,92,.22)` border | `#8C6D1E` | "Backed 1:1 · audited reserves — Verify" chip, gold dot, reserve banners |
| Caution / prerequisite | `#C0892A` | `rgba(192,137,42,.13)` | `#B07A1E` | "ID required" pills in payment methods |
| Negative / down | `#D2483A` | — | — | Down-day chart, negative deltas |
| Error | `#B00020` | — | — | Form/validation errors |

Gold-card gradient stops (physical card render): `#EAD9AE → #E3CC92 → #D3B575 → #CDAD69` with `#E7C886`/`#D9B978` highlights and a `sc-shine 1.4s ease infinite` shimmer.

### 2.4 Dark "power" surface

- Panel: `#0A0A0A`–`#15161B` (gradient washes of deep violet/wine: `#241047`, `#3C1228`, `#0C3A4E` corner glows per accent)
- Text: `#FFFFFF`, secondary `rgba(255,255,255,.60–.65)`
- Chips/tiles on dark: `rgba(255,255,255,.06)` and `.10`
- Eyebrow on dark: pale accent `#E6A8CC`, 11.5px/700, +1.4px tracking, uppercase
- On-dark positive: `#9FEFC0`
- Reserved for: Automate page hero, "Automate your gold / Connect an agent" sidebar card, code blocks.

---

## 3. Typography

### 3.1 Faces

| Face | Role |
|---|---|
| **Geist** | All UI text on web (nav, buttons, titles, body) |
| **Geist Mono** | **Every numeral** on web: balances, prices, deltas, quantities, APRs, dates in ledgers; also code |
| System stack (`-apple-system` / SF) | Mobile-app UI text — deliberate native feel; weights run heavier (650–800) |
| `ui-monospace` fallback | Code blocks (`$ auri buy --gold 50 --every week`) |

### 3.2 Measured scale — web app

| Style | Spec | Sample |
|---|---|---|
| Hero number | Geist Mono 54/700, ls −2.2px | `$21,880.28` |
| Card value | Geist Mono 26/700, ls −0.8px | `$19,480` |
| Wordmark | Geist 20/700, ls −0.5px | Auri |
| Modal title | Geist 17–18/650 | "Buy gold" |
| Nav item | Geist 14.5/500 (active 600) | sidebar |
| Button / row title | Geist 14/600 | "Actions" |
| Ledger amount | Geist Mono 14/700 | `+$250.00` |
| Delta line | Geist Mono 14/600 | `+$231.00 (0.9%) today` |
| Small button / pill | Geist 13/600 | "Buy", "View all" |
| Sub-balance line | Geist Mono 13/400 | `$19,480 gold · $2,400 cash` |
| Chip / segment | Geist 12.5/600 · Geist Mono 12.5/600 | "1M", "CAD" |
| Secondary text | Geist 12.5/400 | row subtitles |
| Meta mono | Geist Mono 11.5–12/400 | `3.1820 oz · self-custody · XAUT`, `3.75% APR` |

Weights in use: 400 / 500 / 600 / 700 (+650/750/800 on mobile system font). Nothing lighter than 400.

### 3.3 Measured scale — mobile app (system font)

Hero `43/800 −1.6px`; card value `27/800 −0.8px`; price `23/750 −0.5px`; greeting/title `19/750 −0.3px`; section caps label `13/700 +0.3px` in `#8A8F9C` ("YOUR BALANCES", "RECENT"); dark-panel eyebrow `11.5/700 +1.4px` uppercase pale accent ("PROGRAMMABLE"); mobile CTA `15–17/650`.

### 3.4 Rules

- Mono for anything countable; never set a currency amount in the text face on web.
- Negative tracking scales with size: −2.2px @ 54, −0.8px @ 26–27, −0.3/−0.5 @ 17–23, normal below 16.
- Signed amounts: `+` green, `−` (true minus U+2212) in ink — color carries direction, weight 700.
- Uppercase only for tiny section labels/eyebrows (11.5–13px, 700, letter-spaced +0.3 to +1.4px). Everything else sentence case.

---

## 4. Shape & elevation

### 4.1 Radius scale (frequency-sorted, computed)

| Radius | Use |
|---|---|
| **12px** (most common, 91 hits) | Cards, primary buttons, payment rows, icon tiles |
| 9–11px | Small buttons (10), nav items (11), segmented rails (9), preset chips (9), provenance chip (10–11) |
| 7–8px | Segment thumbs (7), timeframe chips (8), tiny controls |
| 13–14px | Auth CTA (13), mobile inputs |
| 16px | Mobile sheet buttons ("Cancel") |
| 18px | Large feature cards |
| 20–24px | Modals; sheets use `20px 20px 0 0` |
| 99px | Pills, status badges, avatar buttons |
| 50% | Avatars, FAB, icon dots |

### 4.2 Borders

1px hairlines everywhere; the three working opacities on ink `rgba(20,21,27,…)` are `.07` (resting card), `.05` (divider), `.12` (interactive), with `.14` for inputs. Gold contexts use `rgba(196,162,92,.22)`. Selected payment rows switch the hairline to solid `--accent` at 1px. The FAB wears a 4px white ring.

### 4.3 Shadow ladder (measured)

| Level | Value | Use |
|---|---|---|
| 0 — resting card | `0 1px 2px rgba(20,18,60,.04)` (also `rgba(20,21,27,.03)`) | All cards |
| 1 — raised control | `0 1px 3px rgba(20,21,27,.12)` | Segmented-control active thumb |
| 2 — menu / popover | `0 2px 10px rgba(40,20,60,.08)` | Dropdowns, ticker popover |
| 3 — modal / dialog | `0 30px 70px -24px rgba(15,16,22,.5)` | Desktop modals (overlay `rgba(0,0,0,.5)`) |
| 3 — mobile sheet | `0 24px 50px -22px rgba(20,21,27,.6)` | Action sheet |
| Accent glow — primary | `0 8px 20px -10px var(--accent)` | Top-bar "Actions" button |
| Accent glow — FAB | `0 8px 20px -6px rgba(accent,.6)` | Tab-bar FAB |

Shadows are cool-tinted (blue-violet ink, never pure black at rest).

---

## 5. Components inventory (measured specs)

### Buttons

| Variant | Spec |
|---|---|
| **Primary (accent)** | bg `--accent`, text #FFF, h 42, r 12, 14/600, pad 0 16, glow `0 8px 20px -10px accent`; hover → `--accentDk` |
| **Primary in-card** | same colors, h 38, r 10, 13/600 ("Borrow more") |
| **Dark neutral** | bg `#15161B`, #FFF, h 38–42, r 10–12, 13–14/600 ("Buy", activity filter "All") |
| **Secondary** | bg #FFF, 1px `rgba(20,21,27,.12)`, text `#42454E`, h 38–42, r 10–12, 13/600 ("Sell", "Withdraw", "Repay", "Freeze card") |
| **Soft-positive** | bg `rgba(22,160,106,.12)`, text `#16A06A`, h 38–42, r 10–12 ("Add") |
| **Soft-accent** | bg `--soft`, text `--accent` ("+ New rule", state toggles) |
| **Ghost / link** | no bg, accent text 13/600 ("View all", "Verify", "Use phone instead") |
| **Disabled** | bg `#E7E5EA`, text `#A8A6B0` (auth "Continue" before input); on mobile: accent at ~50% |
| **Mobile CTA** | full-width, h 52–54, r 14–16, 15–17/650 ("Get started", "Continue", "Cancel") |
| **Top-bar utility** | bg #FFF, hairline .07, h 38–42, r 11 ("Refer & earn", gold ticker) |

### Cards
White, r 12–18, 1px hairline `.07`, pad 17–20px, level-0 shadow. Balance cards: label row (12.5/600 + colored dot) → mono value (26/700) → mono meta (12/400 muted) → chip/action row.

### Pills & badges
r 99, 11–12/600–650, pad ~3–5px 9–11px. Green soft = state good ("Safe", "Active", "Connected", "1 active plan"); amber soft = prerequisite ("ID required"); gold chip (r 10–11, square-ish) = provenance with trailing "Verify" link.

### Segmented controls
Rail `#EFEEF4/#EFEEF3`, r 9, inner pad ~3px; active thumb white, r 7, shadow level-1, 12–12.5/600 ink; inactive `#9CA0AB`. Used for Value/Returns, CAD/g/oz/XAUT, iPhone/Android. Timeframe row variant: bare chips, active = dark ink fill (#15161B, white text, r 8–9).

### Inputs
White, 1px `rgba(20,21,27,.14)`, r 10–13, h 36–50, placeholder `#9CA0AB`. Big-amount input: mono display digits, unit dropdown at right, focus ring/border → accent; `≈ 0.00 g · 0.0000 oz` mono echo underneath. Preset amount chips: h 34, r 9, 12.5/600, hairline `.12`. OTP: 6 boxed digits.

### List rows (activity / payment methods)
Leading icon tile 36–40px r 10–12 on `--soft` (or emoji tile on #FFF); title 14/600 ink; subtitle 12.5/400 `#8A8F9C` with `·` separators; trailing mono amount 14/700 (+ green / − ink) over 11.5–12/400 quantity (`0.041 oz`); rows split by `.05` hairlines. Payment rows become radio cards: selected = accent 1px border + `--soft2` wash + accent check.

### Modals (desktop)
Centered, ~600px, r 20+, header = icon tile (r 12, `--soft`) + title 17–18/650 + subtitle 12.5 muted + 30px X button; body sections labeled 13/600; footer full-width primary CTA (disabled tinted until valid); overlay `rgba(0,0,0,.5)`. Enter: `overlayIn .18s` + `sheetIn .24s`. Escape closes.

### Sheets (mobile)
Bottom sheet r `20px 20px 0 0`, grab-handle bar, caps label ("QUICK ACTIONS"), full-bleed white row list (56–64px rows, icon tile + title 17/650 + subtitle 15/400 muted + chevron), `slideUp .3s cubic-bezier(.32,.72,0,1)`. Flows are full-screen takeovers: "Cancel" (accent, top-left) · centered title 17/700 · content · sticky bottom CTA.

### Navigation
- **Desktop sidebar:** 260px; items 223×42, r 11, 14.5/500, icon 18–20; active = `--soft` bg + accent text/icon + 600; profile row pinned bottom ("Verified" + green dot); dark "Automate your gold" promo card above it.
- **Top bar:** search field (h 42, r 11), utility chips, accent "Actions" button, bell with dot badge.
- **Mobile tab bar:** Home/Invest/Activity/Card + center FAB (54px accent circle, white glyph, 4px white ring, accent glow); active tab accent, inactive `#9CA0AB`, labels ~11/600.

### Charts
Accent 2px line with `drawline 1.4s cubic-bezier(.4,0,.1,1)` entrance; area fill = vertical accent→transparent gradient; horizontal hairline grid only; terminal dot in accent; timeframe chip row underneath; delta always mono green/red.

### Status / proof elements
Gold provenance chip; green LTV "Safe" pill + slim green progress bar on track `#EFEEF4` (h ~6, r 99); `LTV 22% · liq. $1,600/oz` and `3.75% APR` in mono muted.

---

## 6. Motion

All motion is short, eased, and enters from below (rise) — nothing bounces except the success pop.

| Keyframe | Measured | Used for |
|---|---|---|
| `fadeUp` | .35s ease; `translateY(10px)` + fade | Page/card content on view switch |
| `fadeIn` / `fade` | .2–.3s | Generic reveals |
| `overlayIn` | **.18s ease** | Modal dim layer |
| `sheetIn` | **.24s cubic-bezier(.3,0,.1,1)**; `translateY(14px) scale(.985)` | Desktop modal panel |
| `menuIn` | ~.2s; `translateY(-8px) scale(.98)` | Dropdown menus (drop from trigger) |
| `slideUp` | **.3s cubic-bezier(.32,.72,0,1)** | Mobile sheets — iOS spring curve |
| `drawline` | **1.4s cubic-bezier(.4,0,.1,1)**; stroke-dashoffset 4000→0 | Chart line draw-in |
| `pop` | scale .5 → 1.08 → 1 | Success check |
| `sc-shine` / `shine` | **1.4s ease infinite** | Gold-card shimmer (only infinite loop in product) |
| `spin` | linear infinite | Loaders |
| `ring`, `barpulse` | ambient | Mobile lock-screen / chart pulse |

Durations cluster at **.18–.35s** for UI, ~1.4s for decorative draws. Curves: plain `ease` for fades; decelerate-style cubic-beziers (`.3,0,.1,1` / `.32,.72,0,1` / `.4,0,.1,1`) for anything that moves.

---

## 7. Spacing rhythm

Measured gaps cluster on a loose 4px grid with a preference for **8 / 9 / 12 / 13** (the four most frequent flex/grid gaps), 3–6px micro-gaps inside chips, 16–24px between sections. Card padding: **17–20px** (20 desktop, 17 compact). List rows: 13–14px vertical. Button padding: 0 14–16px (0 11px sidebar). Modals: 22px (`13px 22px` / `14px 22px` header/footer). Whitespace is generous — one primary card region per viewport row, three balance cards in a 3-col grid.

---

## 8. Voice & tone in UI copy

- **Benefit + factual qualifier, in one short line.** "Backed 1:1 · audited reserves — Verify" · "Against gold · 3.75% APR" · "Instant · no fee" · "EFT · identity check" · "Instant · 1% fee".
- **Verb-first actions, gold as a verb's object.** "Buy gold", "Sell gold", "Borrow cash", "Repay loan", "Gift gold", "Send gold", "Remit abroad". Subtitles explain mechanics: "Turn cash into gold", "Convert gold back to cash", "Pay down and lower your LTV", "Bank, Interac or deposit USDC", "To a contact, @username or wallet".
- **The middot `·` is the universal separator** — never slashes or pipes: `3.1820 oz · self-custody · XAUT`, `Recurring buy · from cash`, `Wedding · claim pending`.
- **Precise numbers build trust.** `$6,122/oz`, `0.041 oz`, `LTV 22% · liq. $1,600/oz`, `1 CAD = 61.2 INR · fee $0.00`. Never rounded vaguely.
- **Warm at the edges, factual in the middle.** Greetings and completions are human ("Good morning, Aarav", "You're all set", "For a birthday, wedding or festival"); transactional surfaces are dry and exact. Reassurance is woven in where money moves: "We convert gold to local currency and pay out to the recipient — fast, with mid-market rates", "Send gold to anyone — a contact claims it as gold, or it lands directly in a wallet you specify."
- **Sentence case everywhere** except tiny letter-spaced section labels (YOUR BALANCES, QUICK ACTIONS, RECENT, PROGRAMMABLE, BUILD ON AURI).
- Developer surface speaks CLI: `$ auri buy --gold 50 --every week`, "MCP · CLI · API keys", "Connect an agent".

---

## 9. Screenshot manifest (48)

`Website (New)/assets/styleguide-crawl/`

**Desktop app (21):** desktop-home, desktop-home-scrolled, desktop-auto-invest, desktop-activity, desktop-card, desktop-actions-page, desktop-automate, desktop-refer-earn, desktop-actions-menu, desktop-gold-ticker-popover, desktop-profile-menu, desktop-modal-buy, desktop-modal-sell, desktop-modal-add, desktop-modal-withdraw, desktop-modal-borrow, desktop-modal-repay, desktop-accent-violet, desktop-accent-wine, desktop-accent-rosegold, desktop-accent-sky

**Mobile app (17):** mobile-first-launch, mobile-lock-screen, mobile-home, mobile-invest, mobile-activity, mobile-card, mobile-actions-sheet, mobile-actions-sheet-scrolled, mobile-flow-buy-gold, mobile-flow-sell-gold, mobile-flow-borrow-cash, mobile-flow-repay-loan, mobile-flow-add-cash, mobile-flow-withdraw, mobile-flow-gift-gold, mobile-flow-send-gold, mobile-flow-remit-abroad

**Auth (6):** auth-01-login-email, auth-02-login-phone, auth-03-enter-the-code, auth-04-enter-the-code-filled, auth-05-add-a-passkey, auth-06-you-re-all-set

**Mobile web (4):** mweb-safari-first-launch, mweb-safari-signed-in, mweb-pwa-signed-in, mweb-pwa-lock-screen
