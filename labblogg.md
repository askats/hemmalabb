# Labblogg – Hemmalabb

## 2026-09-24 – Steg 1: Kontroll av dator och förberedelser
- Dator: MacBook Air 2020, Intel Core i3 (2 kärnor), 8 GB RAM, macOS Sequoia
- Virtualisering: stöds (Intel-Mac)
- Ledigt diskutrymme: 96,6 GB
- Beslut: Kör max två VM samtidigt. Ubuntu Server utan GUI.
  Skippar brandvägg i första versionen p.g.a. begränsat RAM.
- Beslut: Projektmappen ligger i hemkatalogen, inte i iCloud,
  eftersom iCloud-synk kan skapa konflikter med Git.
  GitHub fungerar som säkerhetskopia.

## 2026-09-24 – Steg 2: GitHub
- Bytt användarnamn till askats, lämnar visningsnamnet tomt tills vidare
- Aktiverat tvåfaktorsautentisering med autentiseringsapp
- Döljer e-postadressen och använder GitHubs noreply-adress
- Skapat publikt repo "hemmalabb"

## 2026-09-24 – Steg 3: Git
- Kontrollerat att Git finns installerat: version 2.39.5 (Apple Git-154)
- Konfigurerat Git globalt via Terminalen:
  - Användarnamn: askats
  - E-post: GitHubs noreply-adress, så att min riktiga e-post
    inte syns i uppladdningar
  - Standardgren: main (samma som GitHubs standard)
- Kontrollerat inställningarna med: git config --global --list
- Notering: Terminalens prompt visar mitt riktiga namn och datornamn.
  Måste döljas i skärmdumpar och utskrifter som publiceras.