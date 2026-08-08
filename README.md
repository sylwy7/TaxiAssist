<div align="center">
  <img src="images/banner.png" alt="TaxiAssist Banner" width="800"/>
  
  # 🚖 B-Zone TaxiAssist v3.0
  **Cel mai complex sistem de operare pentru facțiunile Taxi (LS/LV/SF) de pe B-Zone RPG.**
  
  [![Lua](https://img.shields.io/badge/Lua-Moonloader-blue.svg)](https://www.blast.hk/moonloader/)
  [![B-Zone](https://img.shields.io/badge/B--Zone-RPG-orange.svg)](https://b-zone.ro)
  [![Version](https://img.shields.io/badge/Version-3.0-success.svg)](#)
</div>

---

**TaxiAssist** este un mod complex (scris în Lua pentru Moonloader) dedicat exclusiv membrilor facțiunilor Taxi de pe comunitatea B-Zone RPG. Modul a fost conceput pentru a automatiza sarcinile repetitive, a aduna toate informațiile vitale într-un singur loc și a-ți oferi un avantaj major prin HUD-uri live, scurtături și sisteme de monitorizare pe ecran.

---

## 🗺️ 1. Meniul Principal (GPS & Rules) - Totul la un click distanță

Fereastra principală a modului (accesată prin `/txc` sau `/taxiassist`) revoluționează modul în care navighezi și accesezi informațiile pe server.

<div align="center">
  <img src="images/gps_menu.png" alt="GPS Menu" width="800"/>
</div>

* **Locațiile Obligatorii Centralizate**: Nu mai e nevoie să cauți disperat pe forum sau să memorezi locații. Absolut toate locațiile de care ai nevoie sunt integrate aici, sortate vizual în categorii (Facțiuni, Joburi, Important, Custom).
* **Căutare Instantanee**: Bara de căutare filtrează în timp real locațiile pe măsură ce tastezi.
* **Adăugare Custom**: Poți adăuga, edita și șterge oricând locațiile tale personale direct din acest meniu.
* **Butonul "RULES" (Regulamentul)**: Da, până și regulamentul serverului/facțiunii este prezent! Apăsând pe butonul RULES, ai acces imediat la regulament pentru a rezolva orice dubiu fără să faci Alt-Tab.

---

## ⚙️ 2. Meniul de Configurare (TAXI Menu)

Apasă butonul **TAXI** din colțul dreapta-jos al ferestrei GPS pentru a deschide **Meniul de Control**.

<div align="center">
  <img src="images/config_menu.png" alt="Config Menu" width="800"/>
</div>

Acesta este "creierul" modului, împărțit în secțiuni logice:
* **Automatizare**: Activezi/Dezactivezi funcții precum Auto-Fare (setează `/fare` automat conform orei zi/noapte), Auto-Greeting, Auto-Goodbye.
* **Texte (Custom Greetings)**: Te-ai săturat de textele clasice? Aici poți scrie propriile tale texte custom cu care modul să salute clienții sau să-și ia la revedere.
* **Comenzi (Help)**: O listă completă și explicată cu absolut toate comenzile scurte pe care le oferă modul. Ai uitat ce face o scurtătură? Verifici aici direct în joc.
* **Taste (Keybinds)**: Configurează butoanele rapide. Modul îți va afișa discret pe ecran scurtăturile tale (ex: *TAXI ASSIST KEYS: Open GPS Menu [K], Live Selector [L]*).

---

## 📱 3. Live Requests (Comenzi în așteptare)

Fii primul care ajunge la client cu sistemul **Live Requests** afișat permanent pe ecran!

<div align="center">
  <img src="images/live_requests.png" alt="Live Requests Panel" width="400"/>
</div>

* Modul interceptează automat absolut toți jucătorii care cheamă un taxi și îi pune într-o listă inteligentă.
* **Distanța și Timpul Exact**: Vezi numele, ID-ul, locația exactă cerută, timpul scurs de la cerere și distanța estimată până la jucător. Nu mai e nevoie să spamezi `/servicecalls` manual.
* *(Notă: Dacă apare o eroare de chat sau spam masiv, poți folosi comanda `/clearlive` doar pentru a curăța lista afișată, pentru un reset rapid).*

---

## 🏎️ 4. Fare HUD & Speedometer Custom

Modernizează-ți complet interfața de condus cu elemente ImGui. Aceste elemente pot fi **dezactivate sau activate oricând** din meniul TaxiAssist.

<div align="center">
  <img src="images/fare_hud.png" alt="Fare & Speedometer HUD" width="300"/>
</div>

* **Speedometer Minimalist**: Îți arată Viteza (KM/H), Viața mașinii (%) și nivelul de Benzină. Arată excelent și nu încurcă vederea.
* **Fare HUD**: Se activează automat când urcă un client. Monitorizezi pe ecran:
  * Numele companiei tale (Personalizat LS/LV/SF)
  * Distanța cursei în timp real
  * Tariful curent aplicat
  * Câștigul exact din acea cursă

---

## ⌨️ 5. Zeci de Scurtături și Comenzi (Shortcuts)

Pe lângă interfețe, ai cel mai complet set de comenzi scurte, concepute pentru aglomerația din trafic:

### Comenzi de navigare/sistem
| Comandă | Acțiune |
|---------|---------|
| `/txc` | Deschide fereastra principală a modului |
| `/selectfaction` | Schimbă culoarea modului conform facțiunii tale (LS/LV/SF) |
| `/alias` | Mapează un Nume pe un ID ca să-l poți folosi ușor în comenzi |
| `/casa [ID]`, `/biz [ID]`, `/clanhq [ID]` | Pune checkpoint instant pe harta ta la aceste locații |
| `/dd` sau `/kcp` | Șterge instant Checkpoint-ul de pe hartă (`/killcp` + `/cancel find`) |

### Scurtături Utile (Tastate)
Modul îți scurtează tastarea pentru 90% din acțiunile necesare:
| Tu scrii | Ce face modul |
|----------|---------------|
| `/sc` | `/servicecalls` |
| `/rep` | `/repair` (Trece automat pe jobul de mecanic dacă e nevoie) |
| `/ref` | `/refill` |
| `/ra` | `/raport` |
| `/ej [ID]` | `/eject [ID]` |
| `/cch` | Curăță chat-ul (Clear Chat) doar pe ecranul tău, ca să scapi de spam |

### Comunicarea cu clienții și colegii
| Tu scrii | Mesaj trimis automat pe chat |
|----------|------------------------------|
| `/iau` | *(Pe chatul facțiunii /tx)*: "Preluat!" |
| `/aj` / `/amj` | "Am ajuns la destinatia dorita." / "Taxiul solicitat a ajuns." |
| `/radio` | "Dorești un post de radio anume? Daca da, care?" |
| `/refuz` | "Te rog sa dai /cancel taxi, am alta comanda." |
| `/reper` | "Imi poti da un reper mai exact, te rog?" |
| `/limbaj` | "Pastreaza un limbaj decent sau primesti eject!" |

---

## 📦 Instalare

1. Descarcă și instalează **CLEO**, **SAMPFUNCS** și **Moonloader 0.26** în folderul jocului.
2. Ai nevoie de librăriile Moonloader standard (`mimgui`, `ffi`, `encoding`, `samp.events`, `vkeys`).
3. Descarcă codul sursă sau ultima versiune de pe acest GitHub (din secțiunea Releases).
4. Adaugă fișierul `TaxiAssist.lua` în folderul `moonloader` din directorul GTA San Andreas.
5. Intră pe server și tastează `/txc`!

---

## 👨‍💻 Credite & Autori
Acest mod a fost inițial construit ca un script CLEO (creat de *TheTom*, continuat de *florynn_fly*). A fost preluat, complet rescris de la zero și adus la standardele actuale folosind **LUA și ImGui** de către:
* 🏆 **SyLvy** 
* 🏆 **Gemini & Claude** (AI Assistance pentru algoritmi și design UI)
* 🏆 **Antigravity** (Optimizări și rescriere a arhitecturii meniurilor)

Dacă vă place și vă ajută, lăsați un ⭐ **Star** pe GitHub!
