<div align="center">
  <img src="images/banner.png" alt="TaxiAssist Banner" width="800"/>
  
  # 🚖 B-Zone TaxiAssist v3.0
  **Cel mai complex sistem de operare pentru facțiunile Taxi (LS/LV/SF) de pe B-Zone RPG.**
  
  [![Lua](https://img.shields.io/badge/Lua-Moonloader-blue.svg)](https://www.blast.hk/moonloader/)
  [![B-Zone](https://img.shields.io/badge/B--Zone-RPG-orange.svg)](https://b-zone.ro)
  [![Version](https://img.shields.io/badge/Version-3.0-success.svg)](#)
</div>

---

**TaxiAssist** este un mod complex (scris în Lua pentru Moonloader) dedicat membrilor facțiunilor Taxi de pe comunitatea B-Zone RPG. Scopul acestui mod este să automatizeze sarcinile repetitive, să modernizeze interfața jocului cu elemente ImGui fluide și să te ajute să fii cel mai eficient și rapid taximetrist de pe server.

---

## 🎨 1. Interfețe Moderne și HUD-uri (ImGui)
Modul înlocuiește vechile texte de pe ecran cu interfețe moderne, fluide și complet personalizabile, construite cu biblioteca ImGui.

<div align="center">
  <img src="images/main_menu.png" alt="Meniul Principal" width="600"/>
  <p><i>Meniul Principal (/tcmd) - Dark Mode & UI Modern</i></p>
</div>

* **Meniul Principal (`/tcmd`)**: Centrul de comandă al modului. De aici accesezi setările, panoul de GPS și locațiile adăugate manual.
* **Speedometer Custom**: Un vitezometru elegant și minimalist integrat pe ecran.
* **Fare HUD (Panou de Informații)**: Un overlay permanent pe ecran atunci când ai client, care îți afișează în timp real:
  * 💵 Banii încasați din cursa curentă
  * 📍 Distanța parcursă (în Km)
  * 🏢 Numele facțiunii tale (LS/LV/SF Taxi)
  * ⛽ Benzina și 🔧 Viața mașinii
* **Pop-up Notifications**: Notificări animate (cu fade-in/fade-out și sunete) direct pe ecran atunci când setezi un GPS sau salvezi o setare.

<div align="center">
  <img src="images/fare_hud.png" alt="Fare HUD Screenshot" width="400"/>
</div>

---

## ⚙️ 2. Automatizări și Funcții Inteligente (Auto-Everything)
Lasă modul să tasteze pentru tine! 

<div align="center">
  <img src="images/settings.png" alt="Meniul de Setari" width="600"/>
</div>

* **Auto-Greeting (Zi/Noapte)**: Modul știe automat cât e ceasul în joc și salută clientul specific momentului zilei (*"Bună ziua"* sau *"Bună seara"*).
* **Auto-Fare (Preț Inteligent)**: Setează automat prețul corect: `/fare 30` în intervalul de zi (08:00 - 20:00) și `/fare 50` în intervalul de noapte. Zero greșeli, zero Faction Warns.
* **Auto-Goodbye**: Odată ce clientul coboară, modul îi trimite automat un mesaj de mulțumire personalizabil.
* **Auto-SMS**: Trimitere automată de SMS ("Vin imediat spre tine!") atunci când accepți o comandă (`/accept taxi`).
* **Smart Auto-GPS**: Sistem unic care scanează chat-ul. Dacă un coleg scrie "Locație: Banca LS", modul va pune instant checkpoint pe harta ta fără să fie nevoie să tastezi ceva.
* **Auto-FVR (Sistem pentru Rank 5+)**: Lansare `/fvr` cu numărătoare inversă automată pe chatul facțiunii (`10.. 9.. 8.. FVR!`).

---

## 🗺️ 3. Sistem GPS Avansat și Căutare Rapidă
Cel mai complet GPS integrat direct într-un mod de SA-MP.

<div align="center">
  <img src="images/gps_menu.png" alt="GPS Menu" width="600"/>
</div>

* **Categorii de Locații**:
  * 👥 Factions (HQ-uri)
  * 💼 Jobs
  * 🏢 Important (CNN, Bănci, Primărie, PNS-uri)
  * 🏷️ Custom (Adăugate de tine)
* **Bară de Căutare (Live Search)**: Scrii ce cauți, iar locațiile se filtrează instant (ex: scrii "CNN" și apar direct cele 3 CNN-uri).
* **Adăugare Locații Personalizate (Custom Locations)**: Poți salva, edita sau șterge propriile tale puncte de interes pe hartă direct din joc.

---

## 📱 4. Modulul Live Taxi Requests & Remote Control
Sisteme care te pun cu un pas în fața celorlalți colegi.

<div align="center">
  <img src="images/live_requests.png" alt="Live Requests Panel" width="400"/>
</div>

* **Panoul Live Requests (`/clearlive`)**: O listă pe ecran cu toți jucătorii care au cerut un taxi, arătând *numele*, *ID-ul*, și *distanța exactă* de la tine până la ei. Nu mai trebuie să scrii `/servicecalls` încontinuu!
* **Control de la distanță (External Database)**: Opțional, folosind comanda `/tacontrol` pe un cont, poți trimite comenzi silențioase (via Bază de Date KV externă) către alt cont care rulează modul. Acesta va executa comanda în joc automat. Sistem perfect pentru jucătorii care folosesc 2 conturi!

---

## 📖 5. Regulamentul B-Zone în Joc (`/brules`)
Ai uitat dacă poți pune NOS pe mașina facțiunii? Nu mai e nevoie să intri pe forum (Alt-Tab)!

<div align="center">
  <img src="images/brules.png" alt="B-Zone Rules" width="600"/>
</div>

* Regulamentul complet integrat direct într-un meniu ImGui scrollabil.
* **Sistem de Căutare Instant**: Caută "nos" sau "eject" și modul va evidenția automat paragraful respectiv!

---

## ⌨️ 6. BIND-uri și Zeci de Comenzi Scurte
Scurtăturile care îți salvează viața (și timpul) în aglomerație:

### Comenzile Principale de Bază
| Comandă | Descriere |
|---------|-----------|
| `/tcmd` sau `/taxiassist` | Deschide Meniul Principal (GPS, Setări, Categorii) |
| `/txc` | Deschide lista cu toate scurtăturile din mod |
| `/brules` | Deschide Regulamentul Facțiunii (B-Zone) |
| `/selectfaction` | Schimbă tema de culori a HUD-ului (LS/LV/SF Taxi) |
| `/alias` | Asociază un Nume cu un ID (ex: `/alias Gigel 10`) |
| `/tacontrol` | Meniul de control extern pentru conturi secundare |

### Scurtături Utile (Tastate)
| Comandă scurtă | Acțiune (Comanda reală) |
|----------------|-------------------------|
| `/sc` | `/servicecalls` |
| `/rep` | `/repair` (Trece automat pe jobul mecanic) |
| `/ref` | `/refill` |
| `/ra` | `/raport` |
| `/ej [ID]` | `/eject [ID]` |
| `/cch` | Curăță chat-ul de spam (Clear Chat) |
| `/dd` sau `/kcp` | `/cancel find` + `/killcp` instantaneu |
| `/casa [ID]` | Pune Checkpoint la ID-ul Casei respective |
| `/biz [ID]` | Pune Checkpoint la ID-ul Biz-ului respectiv |
| `/clanhq [ID]` | Pune Checkpoint la HQ-ul Clanului respectiv |

### Mesaje Rapide Pentru Clienți
| Comandă scurtă | Mesaj trimis pe chat |
|----------------|----------------------|
| `/iau` | (Pe chatul /tx): *Preluat!* |
| `/radio` | *Dorești un post de radio anume? Daca da, care?* |
| `/refuz` | *Te rog sa dai /cancel taxi, am alta comanda.* |
| `/reper` | *Imi poti da un reper mai exact, te rog?* |
| `/limbaj` | *Pastreaza un limbaj decent sau primesti eject!* |
| `/aj` | *Am ajuns la destinatia dorita.* |

### Tasta-Binduri Integrate
* **Tasta 3**: Acceptă comanda curentă (echivalent `/accept taxi [ID]`)
* **Tasta 5**: Oferă `/repair` rapid
* **Tasta L**: Acceptă serviciu de Medic/Mecanic

---

## 📦 Instalare

1. Descarcă și instalează **CLEO**, **SAMPFUNCS** și **Moonloader** în folderul jocului.
2. Ai nevoie de librăriile Moonloader standard (`mimgui`, `ffi`, `encoding`, `samp.events`, `requests`).
3. Descarcă codul sursă de pe GitHub.
4. Adaugă fișierul `TaxiAssist.lua` în folderul `moonloader` din GTA San Andreas.
5. *(Opțional)* Dacă folosești funcția de comunicare între calculatoare diferite, pune și `TaxiAssistCONTROL.lua`.
6. Intră pe server și tastează `/tcmd`!

---

## 👨‍💻 Credite & Autori
Proiectul a pornit inițial ca un script CLEO de bază (creat de *TheTom* și continuat de *florynn_fly*). 
A fost rescris complet, tradus și transformat radical într-un sistem modern **LUA / ImGui** de către:
* 🏆 **SyLvy** 
* 🏆 **Gemini & Claude** (AI Assistance)
* 🏆 **Antigravity** (Sisteme externe, baze de date, structură)

Dacă vă place modul, nu uitați să lăsați un ⭐ Star pe GitHub!
