# Scientist Profile / CV Management

Last reviewed: 2026-06-28

## Purpose

このリポジトリで、Noriyuki (Noly) Higashide の scientist profile、CV、公開プロフィールを継続管理する。PPTXで作った見た目を捨てるのではなく、業績・所属・受賞・リンクの正本をテキストで管理し、必要に応じてWeb / PDF / PPTXへ展開する。

## Source Snapshot

Primary CV source:

- `/Users/noly/Library/CloudStorage/GoogleDrive-norishide@gmail.com/マイドライブ/11_academia/CV/CV_en_250906.pdf`
- PDF metadata: 7 pages, A4, created/modified 2025-09-05
- CV internal update date: 2025-04-25

Public profile sources checked on 2026-06-28:

- X: `https://x.com/nolyhigashide`
- GitHub: `https://github.com/norishide`
- Google Scholar listed in CV: `https://scholar.google.co.jp/citations?user=g4Qp0HgAAAAJ&hl=ja`
- LinkedIn listed in CV/X: `https://www.linkedin.com/in/noriyuki-higashide-0221/`
  - Public request redirects to LinkedIn authwall.
  - User supplied screenshots of LinkedIn Education and Experience on 2026-06-28; those entries are now reflected in `profile/profile.yml`.

Current public-profile facts to reconcile:

- CV affiliation is still Graduate School of Engineering, The University of Tokyo / TMI.
- LinkedIn screenshots show current roles:
  - Impact Fellow, Northwestern Innovation Institute, Apr 2026 - Present, Evanston, Illinois, United States.
  - Postdoctoral Research Fellow, Northwestern University - Kellogg School of Management, Apr 2026 - Present, Evanston, Illinois, United States.
  - Founder CEO, fukan, Oct 2024 - Present, Tokyo, Japan.
- X bio says current affiliation is Impact Fellow at NI Institute, Kellogg School / Kellogg CSSI; this appears consistent with the LinkedIn roles above.
- X bio says: PhD, UTokyo TMI; award-winning dissertation; ex IBM Research Tokyo.
- GitHub public profile currently has name `Noly Higashide`; bio/company/location/twitter are not set.

## Immediate Update Tasks

### P0 - Must Fix Before Publishing

- [ ] Update current affiliation from UTokyo graduate-school affiliation to current role.
  - Candidate wording: `Impact Fellow, Northwestern Innovation Institute; Postdoctoral Research Fellow, Northwestern University - Kellogg School of Management`.
  - Confirm whether public CV should list both current Northwestern roles, or one primary role plus secondary affiliation.
- [ ] Replace obsolete UTokyo office phone/address if it is no longer valid.
- [ ] Update education status after PhD completion.
  - Current CV lists `2020.09 - 2025.09 Ph.D. in Technology Management for Innovation`.
  - LinkedIn screenshot lists `2020 - 2024`; reconcile exact PhD dates before generating the final CV.
  - Add dissertation title if useful for academic CV.
- [ ] Add the department/special-program head award.
  - Need exact Japanese and English name: user note says `専攻科長賞`; X suggests `award-winning dissertation`.
  - Confirm award date, awarding unit, and official English translation.
  - Candidate placement: `Awards, Honors and Scholarships`.
- [ ] Update contact block.
  - Keep personal email.
  - Decide whether to remove UTokyo email.
  - Add current institutional email if available.
- [ ] Add/update links in one canonical place: X, GitHub, Google Scholar, LinkedIn, website.
- [x] Check LinkedIn while logged in and sync visible education, current affiliation, and selected experience from supplied screenshots.
- [ ] Confirm LinkedIn headline and award wording if they are not visible in the supplied screenshots.

### P1 - Scientist Profile Polish

- [ ] Rewrite 80-120 word English research profile for the website and CV front page.
- [ ] Rewrite Japanese research profile for domestic opportunities.
- [ ] Create a short tagline.
  - Candidate: `Science of Science researcher studying how scientific knowledge becomes innovation and societal impact.`
- [ ] Add current keywords.
  - Keep: Science of Science, AI in Science, Computational Social Science, Network Science, Bibliometrics, Innovation Studies, Startup Ecosystem, Research Policy.
  - Consider adding: Science of Innovation, Venture Capital, Knowledge Translation, LLM-based Literature Mining.
- [ ] Decide whether `Founder / CEO, fukan Inc.` remains a current secondary affiliation or industry role.

### P1 - Achievement Updates

- [ ] Review publications after 2025-04-25 and add accepted/published items.
- [ ] Update working papers.
  - `Basic-to-Applied Transitions Boost Scientific Impact`
  - `Technological hypes and venture capital investment`
  - `Discovering startup-ready scientists from co-author networks`
- [ ] Check whether 2025 conference presentations should move from upcoming/planned to completed.
- [ ] Add new talks, invited seminars, press, grants, awards, and services since 2025-04-25.
- [ ] Normalize author markers.
  - Current CV uses `‡` for corresponding author and `†` for equal contribution.
  - Decide whether to keep symbols in web/plain-text outputs.

### P2 - Public Profile Alignment

- [ ] Update GitHub profile bio/company/location if desired.
  - Current GitHub API shows no bio/company/location and 4 public repos.
- [ ] Add GitHub button, X, LinkedIn, Scholar, and CV download links to the Hugo profile page.
- [ ] Create a dedicated website page: `/profile/` or `/cv/`.
- [ ] Add selected projects from GitHub and fukan work only if they support scientist positioning.
- [ ] Decide whether to expose full CV PDF, short CV, or both.

## Current CV Inventory

### Research Products

- Journal articles: 3
- Conference papers: 4
- Conference presentations: 7
- Working paper: 1
- Working in progress: 3
- Media / press: 2

Notable current CV items:

- `Mid-career pitfall of consecutive success in science`, Scientific Reports 14, 28172 (2024)
- `Quantifying advances from basic research to applied research in material science`, Technovation 135, 103050 (2023)
- `Academic Knowledge Accumulation Drives Venture Capital Investments`, ICSSI 2025
- `Basic-to-Applied Transitions Boost Scientific Impact`, ICSSI 2025

### Awards / Honors / Scholarships

- 2023.06 Winner in Knowledge Track, ICSSI Metascience Hackathon
- 2022.06 CEO Award, SRE Holdings Corporation
- 2022.02 Best Business Plan, Deeptech Entrepreneurship Incubation Program
- 2020.03 Finalist in New Venture Challenge, The University of Chicago
- 2018.05 Selected Member, IBM Japan Ltd. Singapore institutional tour
- 2011.03 Special Commendation, HNCT
- 2013.04 - 2015.03 Scholarship for Graduate Student, THE USHIO FOUNDATION
- 2012.04 - 2015.03 Kazuko Inoue Scholarship, Ningenjuku Foundation
- TODO: Add `専攻科長賞` / dissertation-related award after exact name/date confirmation.

### Current Experience Signals

- 2026.04 - Impact Fellow, Northwestern Innovation Institute.
- 2026.04 - Postdoctoral Research Fellow, Northwestern University - Kellogg School of Management.
- 2024.10 - Founder CEO, fukan.
- X profile currently says Impact Fellow at NI Institute / Kellogg CSSI.
- Previous roles include SRE Holdings, freelance consulting, IBM Japan, Sony CSL, and University of Tokyo technical assistant.

## PPTX vs TeX Decision

Recommendation: move the canonical CV source out of PPTX and into text-managed source files, then generate PDF from TeX or Typst. Keep PPTX only for profile decks and visually designed one-pagers.

Why:

- CVs change often and need diffable version control.
- Publications, awards, and talks are structured data; PPTX makes consistency checks hard.
- Multiple outputs are likely needed: full academic CV, short bio, website profile, Japanese profile, and slide-deck version.
- TeX is standard for academic PDFs and gives stable page layout.

Suggested architecture:

- `profile/profile.yml`: canonical person, affiliations, links, keywords, bios.
- `profile/publications.bib`: publications and conference papers.
- `profile/awards.yml`: awards, honors, scholarships.
- `profile/cv.tex` or `profile/cv.typ`: PDF template.
- Hugo content pages generated or manually synced from the same source.

TeX vs Typst:

- Choose TeX if strict academic convention, BibTeX compatibility, and long-term CV portability matter most.
- Choose Typst if faster iteration, cleaner syntax, and easier maintenance matter more.
- For this portfolio, a practical path is: start with YAML/Markdown as source of truth, prototype Typst or TeX after the current facts are confirmed.

## Next Build Tasks

- [x] Create `profile/profile.yml` with verified current affiliation, links, keywords, bios, and contact policy.
- [x] Create `profile/awards.yml` and add `専攻科長賞` once official wording is confirmed.
- [ ] Create `profile/publications.bib` from the current CV.
- [ ] Draft short English and Japanese website bios.
- [ ] Update Hugo home/profile buttons and create a `/profile/` page.
- [ ] Decide output stack: TeX or Typst.
- [ ] Generate a new CV PDF and visually inspect it before replacing the existing PDF.
