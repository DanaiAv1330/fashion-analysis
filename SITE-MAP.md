# Fashion Analysis by Danai — Site Map

Repo: `danaiav1330/fashion-analysis` (GitHub Pages) · Mapped: 7 Nov 2026, after the theme + menu update · updated after simplifying the quiz sign-ups.

---

## 1. Structure at a glance

```
Home (index.html)
├── Articles  →  external WordPress blog (dbvabydanai.wordpress.com)
├── Guides & Tools ▾
│   ├── Όλοι οι οδηγοί & εργαλεία  (guides.html — hub page)
│   ├── ΟΔΗΓΟΙ
│   │   ├── Color Analysis Guide        color-analysis-guide.html   (guide + quiz)
│   │   ├── Style Identity Guide        style-identity-guide.html   (guide + 3-word builder)
│   │   ├── Body Type Quiz              body-type-quiz.html         (quiz)
│   │   ├── Wardrobe Psychology Quiz    closet-quiz.html            (quiz)
│   │   ├── Shoe Matcher                shoe-quiz.html              (quiz)
│   │   ├── Wardrobe Audit Workbook     wardrobe-audit-workbook.html (long-form guide)
│   │   ├── Capsule Wardrobe Workbook   capsule-workbook.html       (long-form guide)
│   │   └── Wardrobe Portfolio Guide    wardrobe-portfolio-guide.html (guide + scoring exercise)
│   └── ΕΡΓΑΛΕΙΑ
│       ├── Budget Planner              fashion-budget.html         (calculator)
│       ├── Wardrobe Wishlist           wishlist.html               (app, login)
│       ├── Wardrobe Tracker            wardrobe-tracker.html       (app, login)
│       ├── KPIs Calculator             wardrobe-calculator.html    (calculator)
│       └── Το Προφίλ μου               wardrobe-profile.html       (collects all quiz results)
├── About (about.html)
└── Newsletter (newsletter.html)

Not in the menu:
- articles.html                  old on-site article list (kept; menu uses WordPress)
- articles/TEMPLATE-article.html template for on-site articles (see HOW-TO-NEW-ARTICLE.md)
```

The menu and footer are identical on every page except the two apps. Wishlist and Tracker have their own app headers.

---

## 2. Page by page

### Main pages

| Page | What it is | Sections (main headings) | Interactive / data |
|---|---|---|---|
| **index.html** — Home | Landing page built as a "style journey" in 4 chapters, each pointing to a guide or tool | Hero «Πόσα λεφτά έχεις κλειδωμένα στη ντουλάπα σου;» · Your Style Journey (colour, style, body type) · Πριν ξεκαθαρίσεις (closet quiz) · Ώρα για ξεκαθάρισμα (audit) · Τι σου λείπει (budget, wishlist) · Go Digital (tracker, calculator) · Newsletter CTA · Latest YouTube videos | 👤 account login · links to 11 pages |
| **about.html** — About | Your story and credentials | Γεια, είμαι η Δανάη · Δουλεύω στο beauty… · Ας μιλήσουμε (contact) | Social links (IG, YouTube, Pinterest, Facebook) |
| **guides.html** — Guides hub | Catalogue of every guide and tool as cards | Guides & Workbooks · Τα εργαλεία της ντουλάπας σου · Μάθε πρώτη για νέους οδηγούς | 👤 account · "email me" mailto button |
| **newsletter.html** — Newsletter | Signup page | Hero signup form · Γιατί να εγγραφείς (perks) | **MailerLite form** (name, email, interest) · 👤 account |
| **articles.html** | Old on-site article list (reads `articles.json`) | Fashion Articles + category filters | Not linked from the menu |

### Guides (Οδηγοί)

| Page | What it is | Sections | Interactive / data captured |
|---|---|---|---|
| **color-analysis-guide.html** | 12-season colour analysis guide | Το χρώμα είναι επιστήμη · Color Analysis Quiz · Βρες την εποχή σου · Δοκίμασε στον καθρέφτη · Γιατί μπερδεύει · Δεν είναι περιορισμός | **Quiz** → season result · **MailerLite** (`color_season`, `source=Color Analysis Quiz`) · Supabase · saves to Profile · 👤 |
| **style-identity-guide.html** | Personal style beyond trends — the 3-word method | Τι είναι το Style Identity · Οι 3 λέξεις · Η φόρμουλα της ιδανικής ντουλάπας | **3-word builder** → style DNA · **MailerLite** (`lifestyle`, `moodboard`, `feeling`, `style_dna`, `name`) · Supabase · Profile · 👤 |
| **body-type-quiz.html** | Body type guide + quiz | Οι 5 βασικοί σωματότυποι · Βρες τον δικό σου | **Quiz** → body type · **MailerLite** (`body_type`) · Supabase · Profile · 👤 |
| **closet-quiz.html** | Wardrobe psychology test: 12 questions → 10 profiles | Intro · quiz · result with top-3 profiles | **Quiz** · **MailerLite** (`wardrobe_profile`) · Supabase · Profile · **PDF download (file missing)** · 👤 |
| **shoe-quiz.html** | Shoe Matcher: outfit or occasion → ideal shoe | Choose a path (outfit / occasion) · result | **Quiz** · **MailerLite** (`shoe_result`, `name`), "guide when it launches" · Supabase · Profile · 👤 |
| **wardrobe-audit-workbook.html** | Step-by-step closet audit | Γιατί δεν λειτουργεί · Audit ≠ ξεκαθάρισμα · Πριν ξεκινήσεις · 4 ερωτήσεις · Σύστημα 4 στοιβών · Ποια κομμάτια αξίζουν · Σε κολακεύει το χρώμα; · Εκτός εποχής · Step by Step · Επόμενο βήμα | Checklists in the page · links to Color, Style, Capsule |
| **capsule-workbook.html** | Seasonal capsule wardrobe workbook | Ποιότητα όχι ποσότητα · Η λογική · Κομμάτια της εποχής σου · Checklist · 8 φόρμουλες · Γιατί δεν λειτουργεί · Πώς να αγοράζεις · Εργαλεία όχι κανόνες | In-page navy sub-menu (Τι είναι, Εποχές, Checklist, Φόρμουλες, Αγορές) · season swatches |
| **wardrobe-portfolio-guide.html** | Wardrobe as an investment portfolio — 4 indicators | Κάθε κομμάτι έχει 4 δείκτες · Τι σημαίνει κάθε νούμερο · Ιδανική vs τυπική · Αξιολόγησε 10 κομμάτια | Scoring exercise · links to KPIs Calculator |

### Tools (Εργαλεία)

| Page | What it is | Sections | Interactive / data |
|---|---|---|---|
| **fashion-budget.html** | Budget Planner — income → real clothing budget → 70-20-10 split | Πόσα έχεις για ρούχα · Μηνιαίο εισόδημα · Πρώτα ό,τι μετράει · Πού πάει ό,τι έμεινε · Core · Trend · Function · 4 κανόνες πριν κάθε αγορά | Calculator (nothing saved) · links to Wishlist |
| **wardrobe-calculator.html** | Wardrobe KPIs Calculator | Cost Per Wear · Scale αξιολόγησης · Πόσες φορές πρέπει να το φορέσεις · Γιατί αυτό το target | CPW and break-even calculators by garment type and occasion (nothing saved) |
| **wardrobe-profile.html** | "Το Wardrobe Portfolio σου": dashboard of every quiz result the visitor has done | Profile cards (colour, style, body, closet, shoe) · Blueprint waitlist | Reads results saved on the visitor's browser (`faProfile`) · **MailerLite** waitlist (`source=Wardrobe Profile - Blueprint Interest`) · Supabase · 👤 |
| **wishlist.html** | Wardrobe Wishlist app (login) | Wishlist · Σύνοψη · Αγορές · Αρχείο | Supabase tables `wishlist`, `wardrobe`, `annual_budgets`, `outfit_uniforms` · own theme (sand / mocha / pink) |
| **wardrobe-tracker.html** | Wardrobe Tracker app (login) | Ντουλάπα · Ημερολόγιο · Dashboard · Sets · Gone (per year) · Uniforms | Supabase tables `wardrobe`, `wear_log`, `wardrobe_archive`, `outfit_uniforms` · own theme (burgundy / olive) |

---

## 3. Where data goes

**MailerLite:** every signup form posts to **one** form, "Newsletter Signup - Site" (account `2295067`, form `185835026362926505`). It has double opt-in, so new subscribers get a confirmation email, and it adds them to the group "Fashion Analysis Newsletter".

Every quiz now ends with the same generic box: **«Γράψου στο newsletter»** — news, fashion advice and new free guides. No results by email, no PDF. Quiz results are still saved on the visitor's Profile page and in Supabase, but are **no longer sent to MailerLite**.

| `source` value (sent, but there's no `source` field in MailerLite yet, so it's dropped) | Page | Other fields sent |
|---|---|---|
| *(none)* | newsletter.html | name, interest |
| Color Analysis Quiz | color-analysis-guide.html | — |
| Style Identity Guide | style-identity-guide.html | name |
| Body Type Quiz | body-type-quiz.html | — |
| Closet Quiz | closet-quiz.html | — |
| Shoe Quiz | shoe-quiz.html | name |
| Wardrobe Profile - Blueprint Interest | wardrobe-profile.html | — (**Blueprint waitlist** — kept) |

MailerLite automations: "Style Identity Quiz — Αποστολή Style DNA" (active) and "Style Identity : Οι 3 λέξεις σου" (draft).

**Supabase**
- The quiz pages and the Profile page save to `email_subscribers` and `quiz_responses`.
- The apps use `wardrobe`, `wear_log`, `wardrobe_archive`, `outfit_uniforms`, `wishlist` and `annual_budgets`.
- The 👤 account login uses Supabase Auth. It appears on index, guides, newsletter, the colour, style, body, closet and shoe pages, and the Profile page.

**Visitor's browser (localStorage)**
- `faProfile` is written by each quiz and read by wardrobe-profile.html.
- `fa_cpw_targets` and `wb_brands` are used by the apps.

**Google Analytics** (G-DBRDY0FNX7) is on most pages. See the issues below for gaps.

---

## 4. Shared files

| File | Purpose |
|---|---|
| `style.css` | Original shared layout. Loaded by index, about, articles, guides, newsletter and the quiz / guide pages |
| `theme.css` | **New.** Fonts, navy / chocolate / ivory / gold colours, shared menu + footer. Loaded by every page except the two apps |
| `main.js` | Nav scroll effect, mobile menu, scroll-reveal animation |
| `articles.json` | Article list read by articles.html |
| `HOW-TO-NEW-ARTICLE.md` | Steps for creating an on-site article from the template |
| `wardrobe_data.js` | Bulk wardrobe import data loaded by the Tracker (205 items; fixed so it's valid JavaScript) |
| `favicon.ico` | Site icon |

---

## 5. Open items

| # | Item | Status |
|---|---|---|
| 1 | Closet quiz PDF download promise | **Removed** (generic signup instead) |
| 2 | Quiz pages promising results by email | **Removed** on all 5 quizzes |
| 3 | `wardrobe_data.js` had curly quotes and wasn't valid JavaScript | **Fixed** |
| 4 | Duplicate files `wardrobe_data`, `wardrobedata.js` | **Deleted** |
| 5 | Google Analytics missing on closet-quiz, fashion-budget | **Added** |
| 6 | GA placeholder id on articles.html and the template | **Fixed** (G-DBRDY0FNX7) |
| 7 | Missing meta descriptions on 4 pages | **Added** |
| 8 | Closet quiz video button hidden (`VIDEO_URL` = "#") | Open: add the YouTube link when ready |
| 9 | Style DNA automation still active in MailerLite | Open: the site no longer sends style_dna, so it should stop firing. Pause it if you want to be sure |
| 10 | Blueprint by email | Later: when ready, add a `source` field + automation for the Blueprint waitlist |
