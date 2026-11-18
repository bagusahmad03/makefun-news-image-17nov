# The day's world news in one image — Tuesday, 17 November 2026

[![make.fun · news-image-20261117](https://make.fun/badge/news-image-20261117.svg)](https://make.fun/bounty/news-image-20261117?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261117)
[![rank](https://make.fun/badge/news-image-20261117/bagusahmad03/makefun-news-image-17nov/rank.svg)](https://make.fun/bounty/news-image-20261117/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261117)
[![reward](https://make.fun/badge/news-image-20261117/bagusahmad03/makefun-news-image-17nov/reward.svg)](https://make.fun/bounty/news-image-20261117?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261117)

An entry for make.fun's `news-image-20261117`: one program that writes one
image, `entry.png`, summing up the world news of Tuesday 17 November 2026.
A vision judge compares entries pairwise and picks the one that best sums
up the day.

## How to run

```sh
mkdir -p out
MAKEFUN_OUTPUT_DIR=out python3 main.py
```

The grader runs `python3 -P -s /bot/main.py` and expects `entry.png` in
`/output`. Python 3 standard library only, no network. The program copies
the poster byte for byte, so two runs write identical bytes.

## What the image shows

A newspaper-front-page poster, masthead "THE WORLD TODAY", dated Tuesday,
17 November 2026. Ten stories, all from the day's reported news:

**Lead:** Ukraine struck the Crimean (Kerch) Bridge for a second day
running — a road section collapsed, traffic suspended; President Zelenskyy
called it "an unprecedented operation". Russia struck Kyiv's North and
South bridges over the Dnipro, disrupting heating, water and power.

**Middle East:** Iran fired drones at a US military radar at Sheikh Isa
base in Bahrain (intercepted, no casualties or damage); tankers struck
mines near the Strait of Hormuz; a third US aircraft carrier, USS Theodore
Roosevelt, arrived in the region.

**Diplomacy:** China confirmed the first Xi–Trump–Putin three-way
meeting, set for Thursday 19 November in Shenzhen on the APEC sidelines,
as Trump travels to Asia.

**In brief:** the Pentagon failed its financial audit for the 9th year
($4.8 trillion in assets unverified); Japan scrambled fighter jets after
suspected Russian aircraft violated its airspace; a G7 donor conference
in Paris aims to raise $250M to repair Chernobyl's containment shield;
the UK, Australia, Canada and Italy urged Israel to open Gaza crossings
for aid while the UK sanctioned 8 Israeli settlement construction firms;
Gérard Depardieu pleaded guilty to sexual assault before a Paris court;
a Houthi advance in Yemen pushed government forces back from the Red Sea
coast; US measles cases hit their highest since 1991, with 13 babies
born with congenital measles.

## Design notes

The poster is a flat editorial layout: serif headlines, a red-and-navy
accent palette on newsprint cream, and three simple drawn panels (the
damaged bridge, a radar/drone/tanker scene, and the three flags of the
summit). Every headline is set large enough to read at full size, and no
real outlet's logo or masthead is used. The image was rendered from a
self-contained HTML page with inline CSS/SVG and inspected at full size
before submission; the build file is not part of this repository.

## Verification

- Two runs with different `MAKEFUN_OUTPUT_DIR` values wrote byte-identical
  output, equal to `entry.png` in this repository.
- Output is a valid PNG, 1024x1024 pixels, 245,379 bytes — inside the
  1 MiB / 1024x1024 gate.
- The image differs from the kit starter's image (different bytes,
  different dimensions: the starter ships a 512x512 image).
- The poster was read back at full size and every headline checked for
  legibility: masthead, all three feature headlines, and all seven briefs
  are legible with no clipping or overlap.

## Files

- `main.py` — copies `entry.png` to the output directory (stdlib only)
- `entry.png` — the poster, 1024x1024, 245,379 bytes
- `README.md` — this file
- `LICENSE` — MIT
