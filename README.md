# Training Plan Calculator

A single-file calculator that turns body data into a starting training prescription: BMR, TDEE, calorie target, macros and weekly set volume by experience level.

**Live:** https://decastropt.com/schede.html (the paid, fully personalised version)
**Paper behind the method:** https://doi.org/10.5281/zenodo.23767828

## What it does

Input: sex, age, weight, height, activity level, training experience, goal.

Output:

| Metric | Formula |
|---|---|
| BMR | Mifflin–St Jeor (1990) |
| TDEE | BMR × activity factor (1.2 – 1.9) |
| Calorie target | TDEE × (1 + goal), goal −15% / 0 / +10% |
| Protein | 1.8 g per kg bodyweight |
| Fat | 0.8 g per kg bodyweight |
| Carbs | remaining energy ÷ 4 |
| Weekly sets per muscle | 8–10 beginner · 12–18 intermediate · 16–22 advanced |

## Why it exists

Most "free workout plan" pages are a fixed template. The prescription should come from measurable inputs, and it should state the rule by which it changes. This tool shows the arithmetic so anyone can check it — no signup, no tracking, no server.

## Run it

No build step, no dependencies. Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
```

## Deploy

GitHub Pages: Settings → Pages → Source: `main` / root. The page is served at `https://<user>.github.io/<repo>/`.

## Licence

MIT for the code. The formulas are cited from the published literature listed below.

- Mifflin MD, St Jeor ST, et al. *Am J Clin Nutr.* 1990;51(2):241–247.
- Frankenfield D, et al. *J Am Diet Assoc.* 2005;105(5):775–789.
- Schoenfeld BJ, Ogborn D, Krieger JW. *J Sports Sci.* 2017;35(11):1073–1082.

---

Built by [Decastro Training Lab](https://decastropt.com) — personalised training plans built on your own numbers.
