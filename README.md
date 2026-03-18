# Fashion Analysis by Danai — Website

## 📁 Αρχεία του site

```
index.html              ← Αρχική σελίδα
articles.html           ← Σελίδα άρθρων
guides.html             ← Σελίδα guides & workbooks
about.html              ← Σελίδα about
capsule-workbook.html   ← Το capsule wardrobe workbook (από τα outputs)
style.css               ← Κοινά στυλ για όλες τις σελίδες
main.js                 ← Κοινό JavaScript
```

---

## 🚀 Πώς να ανεβάσεις στο GitHub Pages (βήμα-βήμα)

### Βήμα 1: Δημιούργησε λογαριασμό στο GitHub
Πήγαινε στο [github.com](https://github.com) και κάνε Sign Up (αν δεν έχεις ήδη).

### Βήμα 2: Δημιούργησε νέο repository
1. Πάτα το **"+"** πάνω δεξιά → **"New repository"**
2. Όνομα repository: **`fashionanalysisbydanai`** (ή ό,τι θέλεις)
3. Επίλεξε **Public**
4. Πάτα **"Create repository"**

### Βήμα 3: Ανέβασε τα αρχεία
1. Μέσα στο repository, πάτα **"uploading an existing file"**
2. Σύρε ΟΛΑ τα αρχεία (index.html, articles.html, guides.html, about.html, capsule-workbook.html, style.css, main.js)
3. Πάτα **"Commit changes"**

### Βήμα 4: Ενεργοποίησε το GitHub Pages
1. Πήγαινε στο **Settings** του repository
2. Στο αριστερό μενού → **Pages**
3. Στο "Branch" επίλεξε **main** και φάκελο **/ (root)**
4. Πάτα **Save**

### Βήμα 5: Το site είναι online! 🎉
Σε 1-2 λεπτά το site σου θα είναι διαθέσιμο στο:
```
https://[το-username-σου].github.io/fashionanalysisbydanai/
```

---

## ✏️ Πώς να προσθέσεις νέο άρθρο

Άνοιξε το `articles.html` και αντέγραψε αυτό το block μέσα στο `<div id="articlesGrid">`:

```html
<article class="article-card-full reveal" data-cat="color">
  <!-- data-cat: color | capsule | style -->
  <div class="article-cat">Color Analysis</div>
  <div class="article-date">Ιανουάριος 2025</div>
  <h3 class="article-title" style="font-size:1.3rem; margin-bottom:0.85rem;">
    Τίτλος άρθρου εδώ
  </h3>
  <p class="article-excerpt">Σύντομη περιγραφή του άρθρου εδώ.</p>
  <a href="link-στο-άρθρο.html" class="article-link" style="margin-top:auto;">Διάβασε →</a>
</article>
```

---

## ✏️ Πώς να προσθέσεις τη φωτογραφία σου

Στο `index.html` και `about.html` υπάρχει placeholder με κείμενο "Πρόσθεσε τη φωτογραφία σου εδώ".

Για να βάλεις τη φωτογραφία σου:
1. Ανέβασε τη φωτογραφία σου στο GitHub (π.χ. `danai.jpg`)
2. Βρες τον κώδικα `.img-placeholder` και αντικατέστησέ τον με:
```html
<img src="danai.jpg" alt="Δανάη" style="width:100%; border-radius:2px;" />
```

---

## 🔗 Σύνδεση με το Capsule Workbook

Αντέγραψε το αρχείο `capsule-wardrobe-workbook.html` (από τα outputs) και μετονόμασέ το σε `capsule-workbook.html`. Ανέβασέ το μαζί με τα υπόλοιπα αρχεία.

---

## 📧 Contact
dbvabydanai@gmail.com
