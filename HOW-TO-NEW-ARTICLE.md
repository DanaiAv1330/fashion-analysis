# ✍️ Πώς να Γράψεις Νέο Άρθρο — 5 Βήματα

---

## Βήμα 1: Αντέγραψε το template

Πήγαινε στον φάκελο `articles/` και αντέγραψε το αρχείο:
```
TEMPLATE-article.html
```
Μετονόμασέ το με το slug του άρθρου σου, π.χ.:
```
articles/style-identity-guide.html
```

> **Τι είναι slug;** Ο τίτλος του άρθρου με παύλες αντί για κενά, πεζά γράμματα.
> "Πώς να βρεις το στυλ σου" → `pos-na-vreis-to-styl-sou.html`

---

## Βήμα 2: Άλλαξε τα 6 σημεία στο HTML

Άνοιξε το νέο αρχείο και αντικατέστησε παντού που γράφει σχόλιο `═══ ΑΛΛΑΞΕ ═══`:

| Τι αλλάζεις | Παράδειγμα |
|---|---|
| `<title>` | `Πώς να βρεις το στυλ σου — Fashion Analysis by Danai` |
| `<meta description>` | Μια πρόταση περιγραφή |
| Κατηγορία (2 σημεία) | `Style Education` |
| Τίτλος `<h1>` | `Πώς να βρεις το στυλ σου` |
| Excerpt | Σύντομη περιγραφή |
| Ημερομηνία | `20 Μαρτίου 2026` |
| `CURRENT_ARTICLE_ID` | `style-identity-guide` |
| `CURRENT_CATEGORY` | `style` |

---

## Βήμα 3: Γράψε το περιεχόμενο

Βρες την ενότητα με τα σχόλια:
```html
<!-- ΕΔΩ ΓΡΑΦΕΙΣ ΤΟ ΠΕΡΙΕΧΟΜΕΝΟ ΤΟΥ ΑΡΘΡΟΥ -->
```

Και γράψε εκεί το κείμενό σου χρησιμοποιώντας:
- `<h2>` για κύριες ενότητες
- `<h3>` για υποενότητες
- `<p>` για παράγραφοι
- `<ul><li>` για λίστες
- `<blockquote>` για quotes
- `<img src="../images/ΕΙΚΟΝΑ.jpg" alt="..." />` για εικόνες

---

## Βήμα 4: Πρόσθεσε στο articles.json

Άνοιξε το `articles.json` και **πρόσθεσε στην ΑΡΧΗ** (πριν το πρώτο `{`):

```json
[
  {
    "id": "style-identity-guide",
    "title": "Πώς να βρεις το προσωπικό σου στυλ",
    "excerpt": "Μια σύντομη περιγραφή, 1-2 προτάσεις.",
    "category": "style",
    "categoryLabel": "Style Education",
    "date": "2026-03-20",
    "dateLabel": "20 Μαρτίου 2026",
    "image": "images/style-identity.jpg",
    "url": "articles/style-identity-guide.html",
    "featured": false
  },
  ... (τα υπόλοιπα άρθρα)
]
```

> ⚠️ Σημαντικό: Πρόσθεσε στην ΑΡΧΗ της λίστας — έτσι αυτό θα είναι το πιο πρόσφατο και θα εμφανίζεται πρώτο παντού.

**Κατηγορίες (category):**
- `color` → Color Analysis
- `style` → Style Education
- `capsule` → Capsule Wardrobe
- `wardrobe` → My Closet

---

## Βήμα 5: Ανέβασε στο GitHub

1. Πήγαινε στο repository σου στο GitHub
2. Σύρε το νέο HTML αρχείο στον φάκελο `articles/`
3. Σύρε το ενημερωμένο `articles.json`
4. Πάτα **Commit changes**

✅ Αυτόματα:
- Εμφανίζεται στη σελίδα Articles με το σωστό filter
- Αν είναι το πιο πρόσφατο, εμφανίζεται στα 3 featured της Homepage
- Έχει prev/next navigation στο τέλος
- Έχει related articles αυτόματα

---

## 📸 Για τις εικόνες

1. Βάλε τις εικόνες στον φάκελο `images/`
2. Στο HTML χρησιμοποίησε: `<img src="../images/ΟΝΟΜΑ.jpg" alt="..." />`
3. Στο JSON χρησιμοποίησε: `"image": "images/ΟΝΟΜΑ.jpg"`

Ιδανικές διαστάσεις: **1200×675px** (16:9) για cover εικόνες.

---

## 📊 Google Analytics — Πώς να το ενεργοποιήσεις

1. Πήγαινε στο [analytics.google.com](https://analytics.google.com)
2. Δημιούργησε νέο Property για το site σου
3. Θα πάρεις ένα κωδικό της μορφής `G-XXXXXXXXXX`
4. Αντικατέστησε **σε όλα τα HTML αρχεία** το `GA_MEASUREMENT_ID` με τον κωδικό σου

Μπορείς να κάνεις Find & Replace σε όλα τα αρχεία ταυτόχρονα:
- Βρες: `GA_MEASUREMENT_ID`
- Αντικατέστησε με: `G-XXXXXXXXXX`

---

## 🔗 Custom Domain (προαιρετικό)

Αν θέλεις να έχεις δικό σου domain (π.χ. `fashionanalysisbydanai.com`):

1. Αγόρασε domain από [Porkbun.com](https://porkbun.com) ή [Namecheap.com](https://namecheap.com) (~8-12€/χρόνο)
2. Στο GitHub repo → Settings → Pages → Custom domain
3. Πρόσθεσε το domain σου
4. Στο DNS του domain πρόσθεσε CNAME record που δείχνει στο `[username].github.io`
5. Τσέκαρε "Enforce HTTPS"

Ο χρόνος ενεργοποίησης είναι 24-48 ώρες.
