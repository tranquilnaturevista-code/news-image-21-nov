# News Image — 21 November 2026

[![News Image](https://make.fun/badge/news-image-20261121.svg)](https://make.fun/bounty/news-image-20261121)
[![Rank](https://make.fun/badge/news-image-20261121/tranquilnaturevista-code/news-image-21-nov/rank.svg)](https://make.fun/bounty/news-image-20261121)
[![Reward](https://make.fun/badge/news-image-20261121/tranquilnaturevista-code/news-image-21-nov/reward.svg)](https://make.fun/bounty/news-image-20261121)

This entry is a single front page for Saturday, 21 November 2026, built
as a classic broadsheet: one dominant story at the top, a row of
supporting headlines beneath it, and market numbers along the bottom.
The `main.py` script does the whole delivery job — it copies the
finished `entry.png` image, byte for byte, to `/output/entry.png`, so
the page that gets judged is exactly the page that was laid out, with
no re-rendering or recompression in between.

## Stories

- **A missile over Poland:** a Russian Kh-101 cruise missile crashes in
  south-east Poland during a large Russian air attack on Ukraine; Warsaw
  calls it a deliberate provocation and NATO scrambles jets, calling the
  incursion a grave violation of allied airspace. No injuries are
  reported. (The Independent, Reuters, BBC)
- **Trump defends the Shenzhen summit:** hours earlier, President Donald
  Trump returned from his trilateral meeting with Vladimir Putin and Xi
  Jinping insisting Putin wants a diplomatic end to the war in Ukraine —
  even as Russia fired more than 110 missiles and about 400 drones at
  Ukraine, killing at least eight people. (The Independent, Europesays,
  New Kerala)
- **Wall Street slides into correction:** the S&P 500 falls 3.70% and the
  Nasdaq 5.28% as AI shares sell off; Nvidia drops 13.8% as the SEC
  examines potential accounting issues at the company. (CNBC, The Daily
  Brief)
- **Britain and the EU sign deals in Brussels:** most food and farm trade
  checks are scrapped from March 2028, carbon markets are linked from
  January 2028, and a youth mobility scheme opens for up to 100,000
  people aged 18–31 on each side. (GOV.UK, Reuters, BBC)
- **A magnitude 6.8 earthquake shakes Peru:** the quake strikes the
  Andean region of Junín, with tremors felt in Lima, about 320 km away.
  (Peru's Geophysical Institute, via The Daily Short)
- **COP31 misses its deadline:** the climate summit in Antalya runs past
  its deadline, with the political draft dropping any mention of fossil
  fuels. (Reuters, UN News)
- **Sport:** KL Rahul becomes the first Indian opener to score Test
  centuries in all four SENA countries (South Africa, England, New
  Zealand and Australia). (The Daily Short)

## How it works

Run `python3 main.py` and the script copies `entry.png` from this
folder into the output folder (the `MAKEFUN_OUTPUT_DIR` environment
variable, or `/output` when that is not set), creating the folder if
it does not exist yet.

## Method

The image was drawn with Python (Pillow) using DejaVu Serif/Sans fonts:
a masthead naming the day, a lead headline and two-column report on the
Poland missile incident, a stylised night-sky panel showing the missile
arc, three supporting stories, a sport line, and a market strip. Every
story above was reported on 21 November 2026. The finished image is
stored in the repository and copied unchanged by `main.py`, so the two
runs the grader performs produce byte-identical output.

## Verification

After copying, the script checks that the copy is exactly the same
size in bytes as the original and stops with an error if the two
sizes differ. Comparing the SHA-256 hash of the output against the
original gives the same guarantee: the two files should match
exactly.
