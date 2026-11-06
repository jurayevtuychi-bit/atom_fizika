# Atom Fizikasi — Interaktiv Mobil Ilova (GitHub & Capacitor)

Mazkur repozitoriy **"Atom Fizikasi"** interaktiv mobil ilovasining to‘liq manba kodi bo‘lib, unda fan mavzulari bo‘yicha har bir mavzuga **5 tadan interaktiv nazorat topshiriqlari** (jami 75 ta topshiriq) kiritilgan.

GitHub Actions orqali avtomatik ravishda tayyor Android **`app-debug.apk`** faylini yig‘ib olishingiz mumkin.

---

## 🚀 GitHub orqali APK yig‘ish (3 daqiqalik yo‘riqnoma):

### 1-qadam. GitHub'da yangi repozitoriy oching
1. [GitHub.com](https://github.com) ga kiring va yangi repozitoriy yarating (masalan: `atom-fizikasi-app`).
2. Repozitoriyni **Public** yoki **Private** qilib belgilang.

### 2-qadam. Ushbu arxivdagi barcha fayllarni yuklang
ZIP arxiv ichidagi barcha fayl va jildlarni repozitoriyga yuklang (Upload files yoki Git orqali):
```
├── .github/
│   └── workflows/
│       └── build-apk.yml       <- Avtomatik APK yig'ish skripti
├── www/
│   └── index.html              <- 75 ta nazorat topshiriqli mobil ilova kodi
├── resources/
│   ├── icon.png                <- Ilova logotipi
│   ├── icon-round.png
│   └── splash.png
├── capacitor.config.json       <- Capacitor ilova konfiguratsiyasi
├── package.json                <- Kutubxonalar va qaramliklar
├── .gitignore
└── README.md
```

### 3-qadam. Actions orqali APK ni yuklab oling
1. Fayllarni yuklaganingizdan so‘ng, repozitoriyning **"Actions"** bo‘limiga o‘ting.
2. **"Build Android APK"** jarayoni avtomatik ishga tushadi (yoki qo‘lda **"Run workflow"** tugmasini bosing).
3. Jarayon 2–3 daqiqada yakunlanadi (yashil belgi chiqadi).
4. Yakunlangan build sahifasining pastki **"Artifacts"** bo‘limidan **`AtomFizikasi-debug-apk`** faylini yuklab oling!
5. ZIP ichidan chiqqan `app-debug.apk` faylini telefoningizga o‘rnating.

---

## 📱 Nima uchun avvalgi APK o‘rnatilmadi va nima qilish kerak?

Agar Android telefoningizda avvalgi «Atom Fizikasi» ilovasi o‘rnatilgan bo‘lsa:
1. Yangi APK ning raqamli xavfsizlik imzosi (keystore) avvalgisidan farq qilgani sababli Android tizimi xavfsizlik nuqtayi nazaridan uni o‘rnatishga ruxsat bermaydi («Ilova o‘rnatilmadi» / «Пакет недействителен» xatosi).
2. **Yechim:** Telefoningizdagi eski versiyadagi «Atom Fizikasi» ilovasini **butunlay o‘chirib tashlang (Uninstall)**, so‘ng yangi APK faylini o‘rnating.
3. Shuningdek, «Noma'lum manbalardan o'rnatish» (Install unknown apps) ga ruxsat bering.

---

## 🛠 Texnik xususiyatlar:
- **App ID:** `uz.tabiiyfanlar.atomfizikasi`
- **Ilova nomi:** Atom Fizikasi
- **Freymvork:** Capacitor 5.x + HTML5 / TailwindCSS / Canvas
- **Tarkibi:** 15 ta nazariy mavzu, 75 ta interaktiv nazorat topshirig‘i, 12 ta virtual laboratoriya simulyatsiyasi, 12 ta modul testi.
