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

## 2026-09-24 – Steg 4: Koppla projektet till GitHub
- Gjort projektmappen till ett Git-repo (git init)
- Skapat .gitignore som utesluter macOS-filen .DS_Store,
  eftersom den kan avslöja mappnamn och filstruktur
- Skapat en SSH-nyckel (ed25519) skyddad med lösenfras,
  sparad i macOS nyckelring
- Lagt till den publika nyckeln på GitHub
- Verifierat GitHubs officiella fingeravtryck innan första
  anslutningen, som skydd mot man-in-the-middle-attacker
- Gjort första uppladdningen (push) till GitHub

## 2026-09-24 – Steg 5: VirtualBox
- Laddat ner VirtualBox 7.2.20 för Intel-Mac från virtualbox.org
- Verifierat filens SHA256-kontrollsumma mot den officiella listan
  för att säkerställa att filen är äkta och oförändrad
- Installerat VirtualBox och raderat installationsfilen efteråt
- macOS meddelade att VirtualBox lagt till bakgrundsobjekt.
  Förväntat, eftersom VirtualBox behöver en hjälptjänst.
  Notering: oväntade bakgrundsobjekt kan vara tecken på
  skadlig kod som försöker uppnå persistens.

## 2026-09-24 – Steg 6: Operativsystem
- Laddat ner Ubuntu Server 26.04.1 LTS (amd64) från ubuntu.com
- Laddat ner Kali Linux 2026.2 installer (amd64) från kali.org
- Verifierat båda filernas SHA256-kontrollsummor mot de officiella
  (shasum -a 256 --check gav OK för båda)
- Valde Ubuntu Server LTS eftersom den får långvariga
  säkerhetsuppdateringar och är vanlig i företagsmiljöer
- Valde Kalis installer istället för färdig VM-avbild för att
  själv välja användarnamn och lösenord, istället för
  standardinloggningen kali/kali som alla känner till