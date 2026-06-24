# 🗺 Greek Geology Explorer — PWA

Εφαρμογή γεωτεκτονικών ζωνών Ελλάδας για γεωλόγους στο πεδίο.
Λειτουργεί ως Progressive Web App (PWA) — εγκαθίσταται σε Android & iOS.

## Αρχεία

```
geology-pwa/
├── index.html       ← Κύρια εφαρμογή
├── manifest.json    ← PWA manifest
├── sw.js            ← Service Worker (offline)
└── icons/
    ├── icon-192.png
    └── icon-512.png
```

## Δωρεάν Deploy σε GitHub Pages

### Βήμα 1 — Δημιουργία αποθετηρίου
1. Πηγαίνετε στο https://github.com και συνδεθείτε
2. Κλικ **"New repository"**
3. Όνομα: `geology-explorer` (ή οτιδήποτε)
4. Ορίστε ως **Public**
5. Κλικ **"Create repository"**

### Βήμα 2 — Ανέβασμα αρχείων
1. Στο νέο repository, κλικ **"uploading an existing file"**
2. Σύρετε και αποθέστε **όλα** τα αρχεία (index.html, manifest.json, sw.js, φάκελος icons)
3. Κλικ **"Commit changes"**

### Βήμα 3 — Ενεργοποίηση GitHub Pages
1. Settings → Pages (αριστερό μενού)
2. Source: **"Deploy from a branch"**
3. Branch: **main** / **(root)**
4. Κλικ **Save**
5. Μετά από 1-2 λεπτά η εφαρμογή είναι διαθέσιμη στο:
   `https://[username].github.io/geology-explorer/`

> ⚠️ **Σημαντικό:** Το HTTPS είναι απαραίτητο για GPS και Service Worker.
> Το GitHub Pages παρέχει αυτόματα HTTPS — δωρεάν!

## Εγκατάσταση στο κινητό

### Android (Chrome)
1. Ανοίξτε τη διεύθυνση στο Chrome
2. Θα εμφανιστεί μπάνερ "Εγκατάσταση στην αρχική οθόνη"
3. Ή: μενού Chrome (⋮) → "Προσθήκη στην αρχική οθόνη"

### iOS (Safari)
1. Ανοίξτε τη διεύθυνση στο Safari
2. Κουμπί κοινοποίησης (□↑) → "Προσθήκη στην αρχική οθόνη"
3. Δώστε όνομα και κλικ "Προσθήκη"

## Λειτουργίες offline

Η εφαρμογή λειτουργεί **χωρίς internet** για:
- ✅ GPS εντοπισμός θέσης
- ✅ Εμφάνιση γεωτεκτονικών ζωνών
- ✅ Λιθολογία, ηλικία, τεκτονική
- ❌ AI αναφορά (απαιτεί σύνδεση)

## Τεχνικές λεπτομέρειες

- Καθαρό HTML/JS/CSS — χωρίς εξαρτήσεις
- Service Worker v5.2 — cache-first στρατηγική
- GPS: navigator.geolocation με enableHighAccuracy
- AI: Anthropic API claude-sonnet-4-6
- Πηγές: Τράνος (ΑΠΘ), Παπανικολάου, Μουντράκης (1994), Αλεξούλη-Λειβαδίτη (2008)
