---
theme: jekyll-theme-minimal
title: "Materialer og betaling"
permalink: /materialer/
---
<a id="top"></a>

# DD Lab Materialer og betaling

Her kan du få et overblik over materialer i DD Lab og se, hvor mange enheder de koster. **1 enhed svarer til 1 kr.** Enhedsprisen gælder for ét styk af det viste materiale, eksempelvis én plade eller ét ark. Hvis materialet afregnes pr. gram, ml eller længde, står det i navnet.

**Oversigten er ikke en garanti for, at materialerne er på lager. Inden du betaler, skal du få en medarbejder i DD Lab til at bekræfte, at de ønskede materialer er tilgængelige i den mængde, du skal bruge.**

Materialerne udleveres i DD Lab og sendes ikke. Materialer til 3D-print er kun til brug på labbets maskiner.

Hvis du har spørgsmål om materialer eller betaling, så email Rasmus Lunding ([rasl@cc.au.dk](mailto:rasl@cc.au.dk)).

## Sådan betaler du

1. Få en medarbejder i DD Lab til at bekræfte, at de ønskede materialer og mængder er tilgængelige, inden du betaler.
2. Find materialet i oversigten og se enhedsprisen og den mængde, prisen gælder for.
3. Beregn, hvor mange enheder du skal betale for. <br> Gang enhedsprisen med antallet af styk eller den angivne mængde, du bruger. <br> For materialer, der afregnes efter vægt eller længde, deler du først dit forbrug med mængden i navnet. Bruger du flere materialer, lægger du enhederne sammen.
4. Gå til DD Labs [fælles betalingspost i AU's webshop](https://ddlab.au.dk/betaling). <br> Vælg det samlede antal enheder og betal i webshoppen.

Eksempel: En rød akrylplade på 25 × 25 cm koster 31 enheder. To plader koster derfor 62 enheder.

For akrylrester koster 25 gram 1 enhed, så 50 gram koster 2 enheder. For filament koster 4 gram 1 enhed, så 8 gram koster 2 enheder.

For materialer, der afregnes efter forbrug, såsom filament eller resin til 3d print, skal du først opgøre forbruget og derefter betale. 

[https://ddlab.au.dk/betaling](https://ddlab.au.dk/betaling)

<br/>

## Kategorier

<nav id="materialekategorier" aria-label="Materialekategorier"></nav>

<br/>

<label for="materialesoegning">Søg efter materiale, størrelse eller farve:</label>
<input id="materialesoegning" type="search" placeholder="Eksempelvis akryl, 25 × 35 eller rød" style="box-sizing: border-box; width: 100%; margin: 0.5em 0 1em;" />
<p id="materialestatus" role="status">Henter materialer …</p>
<!-- Billedplacering: Skift "venstre" til "over" nedenfor for at gendanne det tidligere layout.
På meget smalle skærme vises billederne fortsat over beskrivelsen. -->
<div id="tabelsetup" role="region" aria-label="Materialeoversigt" data-billedplacering="venstre"></div>

<style>
@media (min-width: 361px) {
    #tabelsetup[data-billedplacering="venstre"] .materiale-med-billede {
        display: grid;
        grid-template-columns: minmax(0, 30%) minmax(0, 1fr);
        column-gap: 20px;
        align-items: start;
    }
    #tabelsetup[data-billedplacering="venstre"] .materiale-med-billede > h3,
    #tabelsetup[data-billedplacering="venstre"] .materiale-med-billede > p {
        grid-column: 2;
    }
    #tabelsetup[data-billedplacering="venstre"] .materiale-med-billede > img {
        grid-column: 1;
        grid-row: 1 / span 3;
        max-height: 200px;
        object-fit: contain;
        object-position: top left;
    }
    #tabelsetup[data-billedplacering="venstre"] .materiale-med-billede > hr {
        grid-column: 1 / -1;
        width: 100%;
    }
}
</style>
<noscript>Slå JavaScript til for at se materialeoversigten, eller <a href="MaterialerTabel.csv">hent materialelisten som CSV</a>.</noscript>

<!--
MaterialerTabel.csv er UTF-8 og semikolonsepareret med én række pr. materiale.
Kolonner: Navn;Beskrivelse;Billede;Enhedspris;Kategori;Skjul
Tilføj et materiale ved at kopiere en række i samme kategori og rette felterne.
Siden opdaterer oversigten og kategorierne automatisk fra CSV-filen.
- Navn: Skriv materialets navn, størrelse og eventuelle farve. Prisen gælder
  ét styk, medmindre navnet angiver andet, fx "Filament – pr. 4 gram" eller
  "Smart Vinyl – pr. 10 cm". Skriv afregningsmængden her, ikke i et ekstra felt.
- Beskrivelse: Supplerende oplysninger om brug, varianter og særlige vilkår.
- Billede: Et filnavn i materialer/images eller en https-adresse.
  Et tomt felt eller et billede, der ikke kan indlæses, viser automatisk
  images/placeholder.png med teksten "Intet billede".
  Standardbilledet er hentet fra https://placehold.co og gemt lokalt.
- Enhedspris: Skriv antallet af betalingsenheder som et helt tal, fx 4 eller 31.
  Prisen gælder den mængde, navnet beskriver.
  1 enhed svarer til 1 kr. Rund kroneprisen til nærmeste hele tal.
  Halve tal rundes op, fx 12,50 til 13. For materialer med lave priser pr. gram
  vælges en større mængde i navnet, så enhedsprisen bliver et positivt helt tal.
  AFVENTER kan bruges til nye materialer, hvis prisen endnu ikke er kendt.
- Kategori: Danner kategorierne automatisk i rækkefølgen fra CSV-filen.
- Skjul: Lad feltet være tomt for at vise materialet. Skriv ja for at skjule det
  fra oversigten og søgningen. JA og Ja virker også. Fjern ja for at vise
  materialet igen. Kategorier uden synlige materialer vises ikke.
Felter med semikolon, linjeskift eller anførselstegn skal omsluttes af
anførselstegn. Anførselstegn inde i et sådant felt skrives dobbelt.
Kildeudvalg og viste kronepriser kontrolleret 22. september 2026 (36 produkter).
Enhedspriserne er webshoppens viste priser afrundet til nærmeste hele tal.
Akrylrester og filament er omregnet til henholdsvis 25 gram og 4 gram pr. enhed
for at bevare de oprindelige grampriser på 0,04 kr. og 0,25 kr.:

https://auwebshop.au.dk/udstyr?cat=24&hks_subdepartment_id=8&product_list_limit=75
-->

<script type="text/javascript">
(function () {
    var oversigt = document.getElementById("tabelsetup");
    var kategorier = document.getElementById("materialekategorier");
    var status = document.getElementById("materialestatus");
    var soegning = document.getElementById("materialesoegning");
    var materialer = [];

    function laesCSV(tekst) {
        var raekker = [], raekke = [], felt = "", citeret = false;
        tekst = tekst.replace(/^\uFEFF/, "").replace(/\r\n?/g, "\n");
        for (var i = 0; i < tekst.length; i++) {
            var tegn = tekst[i];
            if (tegn === '"') {
                if (citeret && tekst[i + 1] === '"') {
                    felt += '"';
                    i++;
                } else {
                    citeret = !citeret;
                }
            } else if (!citeret && (tegn === ";" || tegn === "\n")) {
                raekke.push(felt);
                felt = "";
                if (tegn === "\n") {
                    if (raekke.some(function (vaerdi) { return vaerdi.trim(); })) raekker.push(raekke);
                    raekke = [];
                }
            } else {
                felt += tegn;
            }
        }
        if (citeret) throw new Error("Uafsluttet CSV-felt");
        raekke.push(felt);
        if (raekke.some(function (vaerdi) { return vaerdi.trim(); })) raekker.push(raekke);
        var kolonner = raekker.shift() || [];
        var paakraevet = ["Navn", "Beskrivelse", "Billede", "Enhedspris", "Kategori"];
        if (paakraevet.some(function (navn) { return kolonner.indexOf(navn) === -1; })) {
            throw new Error("Manglende CSV-kolonner");
        }
        return raekker.map(function (vaerdier) {
            if (vaerdier.length !== kolonner.length) throw new Error("Ugyldig CSV-række");
            var materiale = {};
            kolonner.forEach(function (navn, i) { materiale[navn] = vaerdier[i].trim(); });
            if (!materiale.Navn || !materiale.Kategori) {
                throw new Error("Manglende materialeoplysninger");
            }
            return materiale;
        });
    }

    function tilfoej(parent, tag, tekst) {
        var element = document.createElement(tag);
        element.textContent = tekst;
        parent.appendChild(element);
        return element;
    }

    // Ignorer accenter i søgningen, men bevar den oprindelige tekst i oversigten.
    function normaliserSoegning(tekst) {
        return tekst.toLocaleLowerCase("da").normalize("NFD").replace(/[\u0300-\u036f]/g, "");
    }

    function visMaterialer() {
        oversigt.textContent = "";
        kategorier.textContent = "";
        var soegeord = normaliserSoegning(soegning.value).trim().split(/\s+/);
        var viste = materialer.filter(function (materiale) {
            var tekst = normaliserSoegning([materiale.Navn, materiale.Beskrivelse, materiale.Kategori].join(" "));
            return soegeord.every(function (ord) { return tekst.indexOf(ord) !== -1; });
        });
        var grupper = new Map();
        viste.forEach(function (materiale) {
            if (!grupper.has(materiale.Kategori)) {
                var sektion = document.createElement("div");
                var id = "kategori-" + materialer.map(function (m) { return m.Kategori; }).indexOf(materiale.Kategori);
                tilfoej(sektion, "h2", materiale.Kategori).id = id;
                oversigt.appendChild(sektion);
                var link = tilfoej(kategorier, "a", materiale.Kategori);
                link.href = "#" + id;
                kategorier.appendChild(document.createElement("br"));
                grupper.set(materiale.Kategori, sektion);
            }
            var post = document.createElement("article");
            grupper.get(materiale.Kategori).appendChild(post);
            tilfoej(post, "h3", materiale.Navn);
            var kilde = materiale.Billede || "placeholder.png";
            var url = new URL(/^https:\/\//i.test(kilde) ? kilde : "images/" + kilde, window.location.href);
            if (url.protocol === "https:" || url.origin === window.location.origin) {
                var billede = document.createElement("img");
                billede.alt = materiale.Billede ? materiale.Navn : "Intet billede af " + materiale.Navn;
                billede.onerror = function () {
                    // Forsøg kun én gang, hvis standardbilledet også mangler.
                    this.onerror = null;
                    this.alt = "Intet billede af " + materiale.Navn;
                    this.src = new URL("images/placeholder.png", window.location.href).href;
                };
                billede.src = url.href;
                billede.loading = "lazy";
                billede.style.cssText = "max-width: 200px; width: 100%; height: auto;";
                post.appendChild(billede);
                post.className = "materiale-med-billede";
            }
            tilfoej(post, "p", materiale.Beskrivelse);
            var pris = materiale.Enhedspris.replace(",", ".");
            var prisTekst = "Afventer";
            if (/^\d+(\.\d+)?$/.test(pris) && Number.isFinite(Number(pris))) {
                var antal = Number(pris);
                prisTekst = antal.toLocaleString("da-DK", { maximumFractionDigits: 10 }) + (antal === 1 ? " enhed" : " enheder");
            }
            tilfoej(tilfoej(post, "p", ""), "strong", "Pris: " + prisTekst);
            post.appendChild(document.createElement("hr"));
        });
        status.textContent = !materialer.length ? "Der er ingen materialer at vise i øjeblikket." :
            viste.length ? "Viser " + viste.length + " af " + materialer.length + " materialer." : "Ingen materialer matcher din søgning.";
    }

    soegning.addEventListener("input", visMaterialer);
    fetch("MaterialerTabel.csv")
        .then(function (svar) {
            if (!svar.ok) throw new Error("Materialelisten kunne ikke hentes");
            return svar.text();
        })
        .then(function (tekst) {
            materialer = laesCSV(tekst);
            if (!materialer.length) throw new Error("Materialelisten er tom");
            // Filtrer skjulte poster fra før søgning, kategorier og optælling.
            materialer = materialer.filter(function (materiale) {
                return (materiale.Skjul || "").trim().toLocaleLowerCase("da") !== "ja";
            });
            visMaterialer();
        })
        .catch(function () {
            status.textContent = "Materialelisten kunne ikke indlæses. Prøv at genindlæse siden, eller kontakt DD Lab.";
        });
}());
</script>

<a href="#top">Gå til toppen</a>
