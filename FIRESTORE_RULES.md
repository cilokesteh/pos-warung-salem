# firestore.rules

```
rules_version = '2';

service cloud.firestore {
  match /databases/{database}/documents {
    match /{document=**} {
      allow read, write: if request.auth != null;
    }
  }
}
```

## Cara Deploy Rules (WAJIB — ini penyebab menu ilang)

### Opsi 1: Paste langsung di Console (Paling Gampang)
1. Buka: https://console.firebase.google.com/project/pos-warung-salem/firestore/rules
2. Hapus isi default, paste rules di atas
3. Klik **Publish**

### Opsi 2: Via Firebase CLI
```bash
npm install -g firebase-tools
firebase login
firebase init firestore   # pilih project pos-warung-salem
firebase deploy --only firestore:rules
```

## Penting
- Default Firebase = **locked mode** (deny all). Itu kenapa setalah logout→login, produk ga muncul.
- Rules di atas mengizinkan read/write asal user sudah login.
- Untuk production nanti, perketat lagi (per-user isolation).
