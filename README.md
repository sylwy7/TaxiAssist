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
Modul înlocuiește vechile texte de pe ecran cu interfețe moderne, fluide și complet personalizabile, construite cu biblioteca ImGui. Nu mai trebuie să ghicești date – totul este la un click distanță!

<div align="center">
  <img src="images/main_menu.png" alt="Meniul Principal" width="700"/>
  <p><i>Meniul Principal (/tcmd) - Controlul central al modului</i></p>
</div>

* **Meniul Principal (`/tcmd`)**: Centrul de comandă al modului. De aici accesezi setările, panoul de GPS, aliasele și toate configurațiile necesare.
* **Speedometer Custom**: Un vitezometru elegant și minimalist integrat pe ecran. Poți să-l activezi/dezactivezi direct din setări.

<div align="center">
  <img src="images/speedometer.png" alt="Speedometer" width="400"/>
  <p><i>Speedometer Custom</i></p>
</div>

* **Fare HUD (Panou de Informații)**: Un overlay permanent pe ecran atunci când ai client, care îți afișează în timp real datele cursei:
  * 💵 Banii încasați din cursa curentă
  * 📍 Distanța parcursă (în Km)
  * 🏢 Numele facțiunii tale (Personalizat în funcție de oraș)
  * ⛽ Benzina și 🔧 Viața mașinii

<div align="center">
  <img src="images/fare_hud.png" alt="Fare HUD Screenshot" width="400"/>
  <p><i>Panoul activ în timpul unei curse (Fare HUD)</i></p>
</div>

* **Pop-up Notifications**: Când setezi un GPS, când îl ștergi, sau când salvezi o setare, un mesaj frumos animat va apărea discret în colțul ecranului.

<div align="center">
  <img src="images/notifications.png" alt="Notificari Pop-up" width="300"/>
  <p><i>Sistemul de Notificări Pop-up animate</i></p>
</div>

---

## ⚙️ 2. Automatizări și Funcții Inteligente (Auto-Everything)
Am construit acest mod să tasteze în locul tău. Te scapă de greșelile umane care duc la Faction Warns (FW).

<div align="center">
  <img src="images/settings_tab.png" alt="Tab-ul de Setari" width="700"/>
  <p><i>Tab-ul de Setări - Activează/Dezactivează automatizările</i></p>
</div>

* **Auto-Greeting (Zi/Noapte)**: Modul citește ora serverului. Când un jucător urcă, modul îl salută instant cu *"Bună ziua!"* sau *"Bună seara!"*, în funcție de caz.
* **Auto-Fare (Preț Inteligent)**: La urcarea clientului, setează automat prețul legal: `/fare 30` în intervalul de zi (08:00 - 20:00) și `/fare 50` în intervalul de noapte.
* **Auto-Goodbye**: Odată ce clientul coboară, modul îi trimite automat un mesaj politicos de despărțire.
* **Auto-SMS**: Trimitere automată de SMS ("Vin imediat spre tine!") atunci când dai `/accept taxi`.
* **Smart Auto-GPS**: Sistem unic! Dacă un coleg scrie pe chat-ul companiei `/tx Locație: Banca LS`, modul citește chat-ul și plasează **instant** checkpoint-ul pe harta ta, fără ca tu să scrii nimic.
* **Auto-FVR (Pentru Rank 5+)**: Lansare `/fvr` cu numărătoare inversă automată pe chatul facțiunii (`10.. 9.. 8.. FVR!`).

---

## 🗺️ 3. Sistem GPS Avansat și Căutare Rapidă
Cel mai complet GPS integrat direct într-un mod de SA-MP. Gata cu rătăcitul pe hartă!

<div align="center">
  <img src="images/gps_tab.png" alt="Tab-ul GPS" width="700"/>
  <p><i>Sistemul de GPS Avansat</i></p>
</div>

* **Categorii de Locații Sortate Vizual**:
  * 👥 Factions (HQ-uri) - *Roșu*
  * 💼 Jobs - *Verde*
  * 🏢 Important (CNN, Bănci, Primărie, PNS-uri) - *Albastru*
  * 🏷️ Custom (Adăugate de tine) - *Auriu*

* **Bară de Căutare (Live Search)**: Scrii ce cauți, iar locațiile se filtrează în timp real. (Ex: scrii "CNN" și ai direct pe ecran toate cele 3 locații).

<div align="center">
  <img src="images/gps_custom.png" alt="Adaugare Custom GPS" width="500"/>
  <p><i>Fereastra de Adăugare/Editare a punctelor Custom GPS</i></p>
</div>

* **Adăugare Locații Personalizate**: Ai un loc ascuns preferat sau casa unui prieten? Adaugă-l direct din joc, modului îi va fi salvat permanent.

---

## 📱 4. Modulul Live Taxi Requests
Fii primul care preia comenzile. 

<div align="center">
  <img src="images/live_requests.png" alt="Live Requests Panel" width="400"/>
  <p><i>Panoul cu comenzi live</i></p>
</div>

* **Live Requests (`/clearlive`)**: O listă afișată pe ecran cu toți jucătorii care au cerut un taxi, incluzând *numele*, *ID-ul*, și *distanța exactă* (în metri/km) de la tine până la ei.
* **Fără Spam de `/servicecalls`**: Monitorizezi pasiv piața, vezi imediat cine a dat apel și la ce distanță se află!

---

## 📖 5. Regulamentul B-Zone Integrat (`/brules`)
Ai uitat dacă poți pune NOS pe mașina facțiunii? Nu e nevoie să faci Alt-Tab!

<div align="center">
  <img src="images/brules.png" alt="B-Zone Rules" width="700"/>
  <p><i>Regulamentul complet B-Zone, direct în joc</i></p>
</div>

* Regulamentul complet integrat într-un meniu ImGui foarte fluid și organizat pe capitole.
* **Sistem de Căutare Instant**: Scrii "nos" sau "eject" și modul evidențiază automat paragrafele care conțin acele reguli. Te salvează din orice discuție contradictorie!

---

## 🏷️ 6. Sistemul de Alias (Nume -> ID)
Ai prieteni sau jucători cu care interacționezi des și nu vrei să le tot cauți ID-ul pe TAB?

<div align="center">
  <img src="images/alias_tab.png" alt="Tab-ul de Aliases" width="700"/>
  <p><i>Interfața pentru gestionarea Alias-urilor</i></p>
</div>

* Comanda `/alias` sau secțiunea din meniul principal îți permite să asociezi un Nume cu un ID (ex: Mapezi "Gigel" la ID-ul 15).
* Când folosești comenzi pe server (ex: `/w Gigel salut`), modul va trimite automat la ID-ul corect!

---

## 🎨 7. Selector de Facțiune (Personalizare Temă)
Ești în LS Taxi, dar mâine aplici la LV Taxi? Nicio problemă.

<div align="center">
  <img src="images/faction_select.png" alt="Selectie Fatiune" width="400"/>
  <p><i>Meniul de Selecție a Facțiunii (/selectfaction)</i></p>
</div>

* Folosind comanda `/selectfaction`, poți schimba tematica de text și HUD-urile să afișeze corect numele și culorile facțiunii tale curente (LS, LV sau SF Taxi).

---

## ⌨️ 8. BIND-uri și Zeci de Comenzi Scurte
Scurtăturile care îți salvează timpul în aglomerație:

### Comenzile Principale de Bază
| Comandă | Descriere |
|---------|-----------|
| `/tcmd` / `/taxiassist` | Deschide Meniul Principal (GPS, Setări, Categorii) |
| `/txc` | Deschide meniul cu lista tuturor comenzilor (Help Menu) |
| `/brules` | Deschide Regulamentul Facțiunii (B-Zone) |
| `/selectfaction` | Schimbă culorile și numele (LS/LV/SF Taxi) |
| `/alias` | Meniul rapid de asociere Nume-ID |

### Scurtături Utile (Tastate)
| Comandă scurtă | Acțiune (Comanda reală pe care o scrie modul) |
|----------------|----------------------------------------------|
| `/sc` | `/servicecalls` |
| `/rep` | `/repair` (Trece automat pe jobul mecanic) |
| `/ref` | `/refill` |
| `/ra` | `/raport` |
| `/ej [ID]` | `/eject [ID]` |
| `/cch` | Curăță chat-ul de spam (Clear Chat local) |
| `/dd` sau `/kcp` | `/cancel find` + `/killcp` instantaneu |
| `/casa [ID]` | Pune Checkpoint la ID-ul Casei respective |
| `/biz [ID]` | Pune Checkpoint la ID-ul Biz-ului respectiv |
| `/clanhq [ID]` | Pune Checkpoint la HQ-ul Clanului respectiv |

### Mesaje Rapide Pentru Clienți
| Comandă scurtă | Mesaj trimis automat pe chat |
|----------------|------------------------------|
| `/iau` | (Pe chatul `/tx`): *Preluat!* |
| `/radio` | *Dorești un post de radio anume? Daca da, care?* |
| `/refuz` | *Te rog sa dai /cancel taxi, am alta comanda.* |
| `/reper` | *Imi poti da un reper mai exact, te rog?* |
| `/limbaj` | *Pastreaza un limbaj decent sau primesti eject!* |
| `/aj` | *Am ajuns la destinatia dorita.* |

### Tasta-Binduri Integrate
* **Tasta 3**: Acceptă comanda curentă de taxi foarte rapid (echivalent `/accept taxi [ID]`)
* **Tasta 5**: Oferă `/repair` rapid
* **Tasta L**: Acceptă serviciul de Medic/Mecanic

---

## 📦 Instalare

1. Descarcă și instalează **CLEO**, **SAMPFUNCS** și **Moonloader 0.26** în folderul jocului.
2. Descarcă librăriile Moonloader necesare (`mimgui`, `ffi`, `encoding`, `samp.events`, `vkeys`).
3. Descarcă codul sursă sau ultima versiune de pe acest GitHub (din secțiunea Releases).
4. Adaugă fișierul `TaxiAssist.lua` în folderul `moonloader` din directorul GTA San Andreas.
5. Intră pe server și tastează `/tcmd`!

---

## 👨‍💻 Credite & Autori
Proiectul a pornit inițial ca un script CLEO de bază (creat de *TheTom* și continuat de *florynn_fly*). 
A fost rescris de la zero, tradus și transformat radical într-un sistem modern **LUA / ImGui** de către:
* 🏆 **SyLvy** 
* 🏆 **Gemini & Claude** (AI Assistance pentru UI, structură și algoritmi complecși)
* 🏆 **Antigravity** (Optimizări, ImGui, și funcții avansate)

Dacă vă place modul și vă face viața de taximetrist mai ușoară, nu uitați să lăsați un ⭐ **Star** pe GitHub!
