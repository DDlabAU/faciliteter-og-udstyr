# Github page med overblik over DD Labs og Audiodesigns Faciliteter og Udstyr

Dette er et en github page med et overblik over tilgængeligt udstyr og tilgængelige faciliteter i DD Lab og på audiodesign.

Link: https://ddlabau.github.io/faciliteter-og-udstyr/

## Guide for ansatte

Her er en guide til at tilføje udstyr eller faciliteter til siden.

Siden er opdelt mellem DD Lab og Audiodesign.

For at tilføje udstyr til listen med DD Lab faciliteter og udstyr skal det skrives ind i .csv-filen under [*dd-lab -> DDLabTabel.csv*](/dd-lab/DDLabTabel.csv)

For at tilføje udstyr til listen med audiodesign faciliteter og udstyr skal det skrives ind i .csv-filen under [*audiodesign -> AudiodesignTabel.csv*](/audiodesign/AudiodesignTabel.csv)

(Hvis du ser på .csv-filerne i den online github-viewer skal du ikke tænke på de fejlmeddelelser github skriver, for den tror filerne er komma-sepererede, men de er **semikolon-sepererede**, og det kan githubs online viewer ikke læse.)

Informationerne i disse .csv-filer importeres og sættes op gennem et script i markdown-filerne for hhv. forsiden, DD lab oversigten og audiodesign oversigten. For at ændre alt andet end selve udstyret eller faciliteterne gøres det ved at ændre i filerne:
- Forside: [index.md](/index.md)
- Forside på engelsk: [en.md](/english/en.md)
- Venstre sidebar: [_config.yml](/_config.yml)
- DD Lab oversigt: [dd-lab.md](/dd-lab/dd-lab.md)
- Audiodesign oversigt: [audiodesign.md](/audiodesign/audiodesign.md)

## .csv-filerne:

Der er altså to .csv-filer: Én for DD Lab og én for Audiodesign. Overskrifter samt faciliteter/udstyr bliver sat ind på overblikket i den rækkefølge de har i .csv-filerne.

**Eksempel:** Følgende række i .csv-filerne

|Titel| Billede|Kommentar|Udlån|
|---|---|---|---|
|Olympus LS-14 Linear PCM Recorder|OlympusLS-14.jpg|Inklusiv pose, usb-kabel, vindhætte og stand|Kan lånes fra DD Lab|

Giver følgende fremvisning i overblikket:

![Samlet](/assets/img/ddLabOverblik.PNG)

### Overskrifter/Kategorier

Overskrifter/Kategorier er den interaktive indholdsfortegnelse der er i toppen af hvert overblik (som det kan ses på billedet nedenfor).

![Kategorier](/assets/img/kategorier.PNG)

Disse kategorier er også hentet ind fra .csv-filerne, og indsættes ved at lave en række, hvor *"overskrift"* skrives under titel-kolonnen og navnet på kategorien indsættes i billed-kolonnen, efterfulgt af en *"-"* i både kommentar- og udlån-kolonnen.

Dvs. en overskrift tilføjes som i tabellen nedenfor:

|Titel| Billede|Kommentar|Udlån|
|---|---|---|---|
|overskrift|*[Din overskrift]* (eksempelvis: 3D Printere og Scannere)|-|-|

### Titel-kolonnen

Er den titel, der placeres som markeret med rødt på billedet nedenfor:

![Titel](/assets/img/ddLabOverblikTitel.png)

Navnet på faciliteten eller udstyret skrives i denne kolonne, med model-information, hvis vi har flere forskellige slags. Dette felt SKAL udfyldes.

### Billede-kolonnen

Er det billede, der placeres som markeret med rødt på billedet nedenfor:

![Billede](/assets/img/ddLabOverblikBillede.png)

Indsæt billede i "images"-mappen (enten audiodesign -> images eller dd-lab -> images).

Skriv filnavn med filtype ind i denne kolonne i .csv filen.

Links til billeder kan også indsættes, men for at undgå at links'ne forældes og bliver ugyldige, bør billederne uploades til mappen i stedet.

Dette felt kan efterlades tom, men det foretrækkes at der tilføjes et billede.

### Kommentar-kolonnen

Er den lille beskrivelse, der placeres som markeret med rødt på billedet nedenfor:

![Kommentar](/assets/img/ddLabOverblikKommentar.png)

Hvis faciliteten eller udstyret kræver supplerende beskrivelser eller kommentarer, skriv dem i denne kolonne. Dette er ikke nødvendigt for alt udstyr, så feltet kan godt efterlades tomt.

### Udlån-kolonnen

Er den status for udlån, der placeres som markeret med rødt på billedet nedenfor:

![Udlån](/assets/img/ddLabOverblikUdlån.png)

Detaljer angående hvorhvidt udstyret eller faciliteten udlånes skrives i denne kolonne. Dette felt SKAL udfyldes, og kan på nuværende tidspunkt være en af følgende muligheder:

- ```Kan benyttes i DD Lab```
- ```Kan benyttes i DD Lab. KRÆVER KØREKORT FOR AT FÅ TILLADELSE TIL AT BENYTTE!```
- ```Kan benyttes i DD Lab. Spørg en ansat til råds før du benytter den første gang.```
- ```Kan lånes fra DD Lab```
- ```Skriv til <a href='mailto:rasl@cc.au.dk'>rasl@cc.au.dk</a>  angående udlån.```
