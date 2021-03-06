# DanaRS pomp

*Deze instructies zijn voor het instellen van de app en pomp, en gelden voor een DanaRS uit 2017 of jonger. Als je een oudere pomp hebt, ga dan naar de instructies voor de [DanaR insulinepomp](./DanaR-Insulin-Pump).*

**DanaRS with new firmware v3 cannot currently be used with AndroidAPS!**

* De app gebruikt het profiel "BASAL A" op de pomp. Jouw huidige instellingen van jouw basaalstanden op de pomp zullen worden overschreven.

* In AndroidAPS ga naar Configurator en selecteer 'DanaRS'

* Klik op het wieltje achter DanaRS. Je komt nu in de instellingen.

* Selecteer 'Koppel nieuwe pomp' en klik op het serienummer van jouw DanaRS.
  
      ![AAPS pair Dana RS](../images/AAPS_DanaRSPairing.png)
      

* Selecteer 'Pomp wachtwoord' en voer jouw wachtwoord in. (Standaardwachtwoord is 1234)   
  **Je moet de koppeling bevestigen dmv de OK knop op de pomp** Net zoals bij andere bluetooth-apparaten (bijv. smartphone en autoradio).
  
      ![Dana RS confirmation pairing](../images/DanaRS_Pairing.png)
      

* Selecteer 'Bolus snelheid' om de standaardsnelheid te wijzigen die de pomp gebruikt bij een bolus (12sec per Eenheid, 30sec per Eenheid of 60sec per Eenheid).

* Herstart je telefoon.

* Stel de stapgrootte van de basaal in op 0.01 E/uur via het artsen menu (Zie de handleiding van de pomp)

* Activeer de vertraagde bolus-functie (Extended bolus) op de pomp

## Foutmeldingen specifiek voor de DanaRS

### Foutmelding tijdens toedienen insuline

In case the connection between AAPS and Dana RS is lost during bolus insulin delivery (i.e. you walk away from phone while Dana RS is pumping insulin) you will see the following message and hear an alarm sound.

![Alarm insulin delivery](../images/DanaRS_Error_bolus.png)

* In de meeste gevallen krijg je deze foutmelding omdat de communicatie werd verbroken, en is gewoon de juiste hoeveelheid insuline gegeven.
* Controleer in de geschiedenis van je pomp (op de pomp zelf, of in de app op het Dana tabblad > Historiek > Bolussen > VERNIEUW) of de juiste bolus werd gegeven.
* Wanneer je wilt kun je de foutmelding weghalen via Behandelingen tabblad > Careportal.
* De werkelijke hoeveelheid insuline wordt uitgelezen uit de pomp en opgeslagen in de app tijdens de eerstvolgende keer dat ze verbinding maken. Om handmatig te laten verbinden, kun je op het Bluetooth-icoon drukken op het Dana tabblad. Of gewoon afwachten tot de app en pomp vanzelf weer verbinding maken.

## Een andere telefoon gebruiken

When switching to a new phone the following steps are neccessary:

* **Exporteer instellingen** op je oude telefoon
  
  * Hamburgermenu (3 horizontale strepen in linkerbovenhoek)
  * Onderhoud
  * Exporteer instellingen
    
    ![Exporteer AAPS instellingen](../images/AAPS_ExportSettings.png)

* Instellingen **overzetten** van oude naar nieuwe telefoon

* **Handmatig koppelen** van de DanaRS met je nieuwe telefoon 
  * Omdat ook de instellingen voor het verbinden met je pomp zijn mee-geïmporteerd, zal jouw nieuwe telefoon denken dat hij de pomp al "kent" en dus geen Bluetooth verbindingsverzoek doen. Daarom moeten nieuwe telefoon en pomp handmatig gekoppeld worden.
* **Installeer AndroidAPS** op je nieuwe telefoon.
* **Importeer instellingen** op je nieuwe telefoon 
  * Hamburgermenu (3 horizontale strepen in linkerbovenhoek)
  * Onderhoud
  * Importeer instellingen

## Wisselen van tijdzone met de DanaRS

Lees alles over reizen in verschillende tijdzones op de pagina [Wisselen van tijdzone](../Usage/Timezone-traveling#danarv2-danars).