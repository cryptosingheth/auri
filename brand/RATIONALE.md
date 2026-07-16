# Auri — Logo System Rationale

Four directions, one winner. All marks are geometrically constructed (circles, arcs,
snapped grids), drawn to survive one flat color at 16px.

## Concepts

**Concept 1 — Dawn Disc** (`concept-1.svg`)
A full gold disc, flat-cut on its chord, floating just above a horizon bar. Aurum is
dawn: the coin as a rising sun, the horizon as the ledger line. Deliberately a *whole*
disc rather than a semicircle — the coin has already risen; the mood is arrival, not
waiting. Warm and calm, but the sun-over-horizon genre is crowded in banking; it is
the least ownable of the four.

**Concept 2 — Ingot A** (`concept-2.svg`) — WINNER
The letter A cast as a gold bar. The silhouette is the end profile of a poured ingot —
flat top, keystone stance, walls sloping exactly 1:3 — with the counter and notch cut
in to make it a letter. One shape carries the whole brand: the initial, the product
(real bars), and the keystone, the stone that bears load — "your gold, in your custody."
No heraldry, no coin clichés, nothing crypto. Solid geometry means it is legible from
240px down to a 16px favicon without redrawing its idea.

**Concept 3 — Minted a** (`concept-3.svg`)
A coin struck with a lowercase "a" in negative, stencil-cut: the bowl and stem are one
connected void, the bowl's island stays coin metal, like a die-struck counter. Quietly
premium and the most "mint mark" of the set. Its negative detail softens below ~24px,
which keeps it from winning, but it makes a beautiful large-scale texture or coin motif.

**Concept 4 — Reserve Stack** (`concept-4.svg`)
The reserve reduced to three rounded strokes stacked into a pyramid. Honest, stable,
and instantly understood — but it sits too close to generic bullion clip-art and, at
UI sizes, to a hamburger icon. Useful as an illustration motif, not as the mark.

## Why the Ingot A wins

It is the only candidate that is simultaneously **the name** (A), **the product**
(a cast bar), and **the promise** (a keystone: load-bearing, self-custodied). It needs
no gradient to mean gold, no circle to mean money. It is one flat shape with six grid
levels, so it is ownable, trademarkable, and indestructible at small sizes — the
Rand/Haviv test: simple, appropriate, memorable, and boring in none of those three.

## Winner files

- `mark.svg` — production mark, 32×32, flat ink `#15161B`. Redrawn on a 32-grid with
  slightly heavier legs/crossbar than the 240px display cut (optical size compensation).
- `mark-gold.svg` — dress-up variant. Brand gradient `#EAD9AE → #D3B575` with a deep
  cast edge `#B98A2F` so the light end keeps contrast.
- `lockup.svg` — mark + "Auri". Wordmark is drawn as paths: monoline geometric-humanist
  on Geist proportions (cap 20 / x-height 14.5 / stroke 3.75, flat terminals; the cap A
  carries a small flat apex echoing the ingot). Production may set live type in Geist
  Medium at the same proportions; the drawn version keeps the file font-independent.
- `favicon.svg` — ink tile (`rx=7`) with the gold-gradient mark. Ink tile chosen over a
  gold tile: it holds on both light and dark browser chrome, and gold-on-ink is the
  premium end of the palette.

## Usage rules

**Clearspace.** Keep clear area on all sides ≥ 25% of the mark's height (at 32px, that
is 8px). In the lockup this equals the gap between mark and wordmark — nothing else may
sit inside it.

**Minimum sizes.** Flat mark: 12px absolute floor, 16px in UI. Gold gradient mark: 24px
minimum on dark grounds; below that switch to flat ink, or flat deep gold `#8C6D1E` on
light grounds. Lockup: 80px wide minimum; below that use the mark alone.

**Color — do.** Ink `#15161B` on light surfaces (`#F6F5F8`) is the default. Gold
gradient on ink/dark surfaces or at large display sizes. Off-white `#F6F5F8` mark on
ink for reversed contexts. One color per instance.

**Color — don't.** No gold gradient on white/light backgrounds below 24px (fails
contrast). Never plum `#A12C66` for the mark — plum is a UI accent only. No outlines,
strokes, drop shadows, bevels, or metallic-foil effects — the shape is the gold. Never
rotate, skew, or set the mark inside another container shape (the favicon tile is the
one sanctioned exception). Never typeset a substitute "A" from a font in place of the
mark.
