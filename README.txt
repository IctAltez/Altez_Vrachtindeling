ALTEZ VRACHTKLEUREN A3 - 3D Viewer Extensie
============================================

INSTALLEREN
1. Maak een GitHub repo ALTEZ_Vrachtplanner aan onder ictaltez of gebruik de bestaande repo.
2. Upload index.html, manifest.json en icon.png naar de root van de repo.
3. GitHub Settings > Pages > Deploy from branch > main / (root).
4. Gebruik dit manifest in Trimble Connect (projectinstellingen > apps/extensions):
   https://ictaltez.github.io/ALTEZ_Vrachtplanner/manifest.json
5. Open de app in de 3D Viewer met de IFC-model(len) geladen.

WERKING
1. Upload een doorzoekbare PDF-laadbrief met vrachtkoppen en tabel 'Nr ElementNr'.
   LG-BETON Hydroos is een reeds getest formaat. Alternatief: CSV/JSON.
   In deze ZIP zit ook HYDROOS_voorbeeld.csv voor test / fallback.
2. Klik Model scannen en inkleuren.
3. Elke vracht krijgt een kleur; selecteer / focus een vracht via de legenda.
4. Kies je 3D-kijkhoek in Trimble.
5. Klik 'Maak A3 met 3D-model + legenda' en daarna 'Afdrukken / Opslaan als PDF'.
   In het afdrukvenster: A3, liggend, schaal 100%, achtergrondkleuren aan.

VOORBEELD
De knop 'Voorbeeld: Hydroos' laadt de 72 echte merken HYD001-HYD072 verdeeld over 12 vrachten
uit de aangeleverde LG-BETON-laadbrief OR20250240 (eerste pagina zijn losse artikelen).
HYD501 bestaat in het aangeleverde IFC-bestand maar staat niet op de vrachtlijst.

BEPERKINGEN
- Een PDF moet selecteerbare tekst bevatten; OCR voor gescande PDF's is niet inbegrepen.
- PDF-tabelvormen verschillen; controleer aantal en groep voordat je op afdrukken klikt.
- De app gebruikt de actuele viewer-snapshot, geen offline IFC-rendering.
- Als pop-ups geblokkeerd worden, downloadt de app een A3 HTML-printblad.
  Open dat bestand en kies vervolgens Afdrukken / Opslaan als PDF.
- Labels worden op de A3-legenda afgedrukt, niet op individuele 3D-objecten.
- De API/printflow moet nog worden bevestigd in jullie echte Trimble Connect-project.
- Projectinformatie/kleuren worden niet automatisch in Trimble of IFC opgeslagen.
- Voor PDF.js is netwerktoegang tot cdnjs.cloudflare.com of jsdelivr.net vereist.
- Dit is een eerste testversie; gebruik 'Reset kleuren' na afloop.

BRONNEN
Trimble Workspace API: https://components.connect.trimble.com/trimble-connect-workspace-api/index.html
PDF.js: https://mozilla.github.io/pdf.js/
