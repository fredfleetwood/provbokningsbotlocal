# provbokning_trafikverket
Ett skript som automatiskt söker efter förarprov och reserverar dem i 15 minuter alternativt bokar dem åt dig.  

---

## Donationer & Hjälp
Om du vill vara lite snäll, Swisha gärna en slant :) 073 554 71 85  
Ring eller smsa INTE utan hör av dig via Discord Daky#6387 om du skulle behöva hjälp med något  
Vill du att jag hittar en tid åt dig så kan jag lösa det för en slant. Kontakt via discord  

---

## Senast testad
Senast testad 2025-05-20

---

## Bot.py - Helt automatisk provbokning
Kort förklarat så kommer den logga in med BankID. Du kommer scanna QR koden i början och sen kör den på självständigt.  
Den kommer att boka första bästa tid med alternativt "Betala senare"  
Du kan avboka gratis om det är mer än 24 timmar till provtillfället så undvik att leta tider inom 24 timmar om du inte är helt hundra på att du kan vilken tid som helst på dagen.  
Den kommer automatiskt boka en tid som uppfyller kraven med betala senare alternativt. Trafikverket kommer maila m.m. om du lyckas boka en tid
Du behöver logga in på trafikverkets hemsida och lägga till ditt telefonnummer och mail innan du kör skriptet, annars kommer den inte kunna boka en tid.


---

## Installation (Windows)

### 1. Ladda ner alla filer
1. Ladda ner alla filer här: [master.zip](https://github.com/Daky60/provbokning_trafikverket/archive/master.zip)  
2. Packa upp mappen och lägg den på skrivbordet

### 2. Installera Python
1. Ladda ner Python här: https://www.python.org/downloads/  
2. Öppna CMD i provbokning_trafikverket-master 
> SHIFT + Högerklick + W (gör detta i provbokning_trafikverket-master)  

Alternativ lösning: öppna cmd och skriv:  
> cd desktop/provbokning_trafikverket-master  
3. Skriv nedanstående kommando i CMD för att installera alla nödvändiga paket  
> pip install -r requirements.txt

### 4. Fyll i config.py
Döp om config.sample.py till config.py  
Texten måste matcha som det står på trafikverkets hemsida.  
Gå igenom sidan manuellt från https://fp.trafikverket.se/boka/#/licence och kontrollera, alternativt,  
Kör skriptet och ändra allteftersom

### 5. Kör skriptet
1. Skriv nedanstående kommando i CMD (Se #3 om du stängde ned rutan)  
> python bot.py
2. Skripten kan avbrytas med CTRL + C

---

## config.py

### 1. license_type
Lägg till behörigheten du vill boka prov inför (ex. B, B96, Buss etc)

### 2. exam
Lägg till vilket prov du vill boka (ex. Körprov, Kunskapsprov)

### 3. rent_or_language
Beroende på ifall du ska boka körprov eller kunskapsprov kommer det finnas alternativ för antingen språk eller hyrbil.  
Ange exakt vad som står som alternativ (ex. "Svenska" eller "Ja, manuell") för att det ska fungera ordentligt.
Om du ska boka ett prov utan någon av alternativen som exempelvis MC kort, ta bort eller kommentera ut raden med #

### 4. dates
Lägg till datum i par i ISO 8601 format (yyyy-mm-dd)  
Skriptet kommer leta efter tider mellan de två datumen  
Fler tidsperioder kan läggas till (ex. dates = ['2020-07-22', '2020-07-25', '2020-08-05', '2020-08-30'])

### 5. locations
Lägg till de orterna du vill boka provet vid (ex. locations = ['Järfälla', 'Sollentuna'])

---

## License

[![License](http://img.shields.io/:license-mit-blue.svg?style=flat-square)](http://badges.mit-license.org)

- **[MIT license](http://opensource.org/licenses/mit-license.php)**
- Copyright 2020 © Daky
