# Prøveforelesning: Introduksjon til programmering

# Slides

## 1. Hei,

Navnet mitt er Joschua Thomas Simon-Liedtke.  
Utvikler og forsker innen IKT.

[Jeg har jobbet med programmering siden bachelorstudiene mine.  
De siste årene har jeg også forsket innen universell utforming av IKT.]

## 2. Introduksjon til programmering

Prøveforelesningen i PGR102

Målet for i dag:  
* Forstå hva programmering innebærer.  
* Forstå hva variabler og funksjoner er.

Du finner eksemplene på:  
https://github.com/digital-work/pgr102  

[Vi bruker JavaScript som et eksempel.  
I løpet av forelesningen skal dere se hvordan dette kan brukes i praksis for å lage et lite program.]

## 3. Hva er et program?

Et program er et sett med instruksjoner som forteller en datamaskin hvordan den løser en oppgave steg for steg.

* Bearbeide tekst  
* Bearbeide bilder  
* Interagere med brukeren  

[Vi bruker programmer til å løse problemer eller utføre oppgaver.  
Det kan være å lese og bearbeide tekst.  
Det kan være å tolke bilder.  
Det kan være å interagere med en bruker.  
Det kan være å utføre beregninger.  
I denne forelesningen skal vi fokusere på oppgaver som er relevante for webutvikling og næringsliv.  
Altså ekte nettsteder og digitale løsninger.  
Vi skal også gjøre noen matematiske beregninger der det er relevant.]

## 4. Hva er programmering?

* Å skrive presise instruksjoner til en datamaskin  
* Slik at den kan utføre oppgaver og løse problemer  

[… og samhandle med mennesker.  

En datamaskin tenker ikke selv.  
Den gjør nøyaktig det vi skriver.  
Ikke det vi mener.  
Derfor må vi være presise når vi programmerer.  
Disse presise instruksjonene skriver vi i et programmeringsspråk.]

## 5. Hvordan forstår datamaskinen instruksjonene?

Datamaskinen forstår bare maskinspråk.  
Vi skriver kode i et programmeringsspråk.  
Programmeringsspråk oversettes til maskinspråk før det utføres.

[En datamaskin forstår ikke norsk eller engelsk.  
Den forstår maskinspråk.  
Enkelt sagt består maskinspråk av nuller og ettall.  
Slik dere kanskje har sett i filmer.  
Men det er vanskelig for mennesker å lese og skrive.  
Derfor bruker vi programmeringsspråk.  
Disse oversettes til maskinspråk før programmet kjøres.]

## 6. JavaScript

Et programmeringsspråk som kan brukes i en nettleser.  
Det brukes ofte sammen med HTML og CSS.

[I denne forelesningen bruker vi JavaScript som et konkret eksempel på et programmeringsspråk.  
JavaScript er mye brukt i webutvikling og i næringslivet.  
På en nettside brukes HTML for struktur.  
CSS brukes for design.  
JavaScript brukes for å styre hva som skjer når brukeren gjør noe.]

## 7. Eksempel 1

Statisk melding  

```
<button onclick="alert('Hallo Kristiania!')">
    Klikk her
</button>
```

[Her ser dere et veldig enkelt program skrevet i JavaScript.  
Det er integrert i en nettside.  
onclick forteller hva som skal skje når vi klikker.  
alert er selve handlingen som kjøres når vi klikker på knappen.  
Teksten i anførselstegn er verdien av meldingen som vises av alert.]

[I dette eksempelet har vi skrevet teksten direkte i koden.  
Men hva hvis vi vil bruke et annet navn?  
Hva hvis navnet brukes flere steder i programmet?  
Må vi da lete gjennom hele koden og endre teksten overalt?]

## 8. Eksempel 2

Bruk av variabel  

```
<script>
let navn = "Oslo";
</script>

<button onclick="alert('Hei ' + navn)">
   Klikk her
</button>
```

[I stedet for å skrive teksten direkte i koden kan vi lagre den ett sted.  
Det vi lager kalles en variabel.  
Den kan gjenbrukes flere steder i programmet.  
Her har vi laget en variabel.  
Vi skriver let navn = "Oslo";  

let betyr at vi oppretter en variabel.  
navn er navnet vi gir den.  
= betyr at vi gir variabelen en verdi.  
"Oslo" er selve verdien som lagres.  

I stedet for å skrive teksten direkte i meldingen bruker vi variabelen navn.  
Da kan vi endre verdien ett sted.  
Den brukes automatisk der vi trenger den.  

JavaScript-kode må ligge inne i en <script>-blokk.]

## 9. Variabel

Et navn på en lagret verdi  
* Verdien kan brukes flere steder  
* Verdien kan endres  

[Fordelen med variabler er at verdien kan gjenbrukes flere steder i koden.  
En variabel gjør det også enklere å endre verdien.]

## 10. Eksempel 3

```
<script>
let navn = "Oslo";
navn = "Bergen";
</script>

<button onclick="alert('Hei ' + navn)">
   Klikk her
</button>

<button onclick="alert('Hei ' + navn)">
   Klikk her igjen
</button>
```

[Først setter vi variabelen navn til "Oslo".  
Så endrer vi verdien til "Bergen".  
Vi endrer ikke selve koden i knappen.  
Knappen gjør fortsatt det samme.  
Det eneste vi endrer er verdien som ligger i variabelen.  
Derfor får vi et annet resultat selv om knappen ser lik ut.  

Når vi klikker på knappen får vi "Hei Bergen".  
Det er fordi Bergen er den siste verdien vi har gitt til variabelen.  
Dette viser at en variabel kan endre verdi underveis i programmet.]

[Så langt har vi skrevet selve koden direkte i knappen.  
Det fungerer i små eksempler som dette.  
Men i ekte programmer er det ofte mer komplekst.  
Da har vi flere instruksjoner.  
Vi har også flere elementer på nettsiden.  
For eksempel flere knapper som skal gjøre det samme.  
Slik det er nå måtte vi skrevet koden i hver enkelt knapp.  

Da kan det fort bli rotete å ha alle instruksjoner direkte i HTML.]

## 11. Eksempel 4

Bruk av funksjoner  

```
<script>
let navn = "Oslo";

function siHei() {
    alert("Hei " + navn);
}
</script>

<button onclick="siHei()">
   Klikk her
</button>
```

[Nå har vi samlet instruksjonen i en egen blokk.  
Instruksjonen er samlet i noe som kalles en funksjon.  
siHei er navnet på funksjonen.  

Ordet function betyr at vi lager en funksjon.  
siHei er navnet vi gir den.  

() betyr at vi kan sende inn informasjon.  
Det vil si verdier som input.  
I dette eksempelet sender vi ikke inn noe informasjon.  
Derfor er parentesene tomme.  

Klammeparentesene {} markerer starten og slutten på koden som tilhører funksjonen.  

I knappen har vi bare én instruksjon.  
Den sier: kjør funksjonen siHei().  
Når vi skriver siHei() i knappen betyr det at funksjonen kjøres.  
Den gjør akkurat det samme som instruksjonen gjorde da den var skrevet direkte i knappen.]

## 12. Funksjon

En samling instruksjoner:  
* Utfører én bestemt oppgave  
* Kan kalles flere ganger når vi trenger den  

[En funksjon er en samling instruksjoner som utfører en bestemt oppgave.  
I vårt eksempel er oppgaven å vise en melding.  
Når vi kaller funksjonen kjøres instruksjonene inni den.  
Dette gjør koden mer strukturert.  
Det gjør den også lettere å lese.  

Selv om vi har brukt variabler og funksjoner har vi skrevet verdien statisk i koden.  
I ekte programmer har vi ofte brukerinput.  
For eksempel fra et input-felt.  

Da kan vi bruke JavaScript til å hente verdien brukeren har skrevet.  
Deretter kan vi bearbeide den.]

## 13. Eksempel 5

Input  

```
<script>
function siHei() {
    let navn = document.getElementById("navnInput").value;

    alert("Hallo " + navn + "! Jeg ønsker deg en fin dag!");
}
</script>

<input type="text" id="navnInput">
<button onclick="siHei()">Send</button>
```

[I dette eksempelet legger vi et tekstfelt ved siden av knappen.  
Tekstfeltet har id navnInput.  

Når vi trykker på knappen kjøres fortsatt funksjonen siHei.  
Men instruksjonen i funksjonen er litt annerledes.  

Den første linjen i funksjonen henter verdien fra input-feltet.  
Programmet finner elementet som har id navnInput.  
Deretter henter det verdien fra elementet.  
Altså teksten brukeren har skrevet.  
Så bruker vi verdien i meldingen som vises.  

Så langt har programmet alltid gjort det samme.  
Det tar et navn og viser en hilsen.  

Men hva hvis brukeren ikke skriver inn noe navn?  
Da vil vi kanskje at programmet skal reagere annerledes.]

## 14. Eksempel 6

Bruk av betingelser (if)  

```
<script>
function siHei() {
    let navn = document.getElementById("navnInput").value;
    
    if (navn === "") {
        alert("Du må skrive inn et navn.");
    } else {
        alert("Hallo " + navn + "! Jeg ønsker deg en fin dag!");
    }
}
</script>

<input type="text" id="navnInput">
<button onclick="siHei()">Send</button>
```

[Nå introduserer vi en betingelse.  

if betyr: hvis noe er sant, gjør dette.  
I parentesene etter if skriver vi en betingelse.  
Her sjekker vi om variabelen navn er tom.  

=== brukes for å sjekke om to verdier er like.  
"" betyr en tom tekst.  
Det vil si at brukeren ikke har skrevet noe.  

Hvis betingelsen er sann kjøres koden i blokken under.  
Hvis ikke hopper programmet videre.  
Eller det kjører else-delen hvis den finnes.  

I vårt eksempel sjekker vi om variabelen er tom.  
Hvis feltet er tomt viser vi en feilmelding.  
Hvis ikke viser vi hilsenen.  

Dette gjør at programmet kan ta et valg.]

## 15. Betingelse (if)

Lar programmet ta valg  
* Utfører ulik kode avhengig av en betingelse  

[Med if kan programmet reagere forskjellig avhengig av situasjonen.  
Uttrykket i parentesene må være sant for at koden skal kjøres.]

## 16. Oppsummering

Hva vi har forstått:  
* Hva et program er  
* Hva programmering innebærer  

Hva vi har brukt:  
* Variabler – lagre og gjenbruke verdier  
* Funksjoner – samle og strukturere kode  
* Betingelser – la programmet ta valg  

[I dag har vi først sett på hva et program er.  
Vi har også sett hva programmering innebærer.  
Det vil si å skrive presise instruksjoner som setter datamaskinen i stand til å utføre oppgaver.  

Så har vi brukt noen av de mest grunnleggende byggesteinene i et program.  
Variabler.  
Funksjoner.  
Betingelser.  

Vi har gått fra en enkel melding.  
Til et lite program som kan ta imot input og reagere forskjellig avhengig av situasjonen.  

Vi har brukt JavaScript som eksempel.  
Men prinsippene gjelder for programmering generelt.]

## 17. Hva skjer videre?

* Mer om variabler og datatyper  
* Parametere og returverdier i funksjoner  
* Flere typer betingelser  
* Løkker og gjentakelse  

[I dette kurset vil vi bygge videre på disse grunnleggende begrepene.  

Vi skal se nærmere på hvordan vi kan strukturere større programmer.  
Vi skal håndtere mer kompleks input.  
Og vi skal skrive mer robust kode.]

## 18. Takk for oppmerksomheten!

Kom med spørsmål eller send e-post til xxx@gmail.com.

# Referanser

* [Shaun Bebbington (2014) What is programming](https://yearofcodes.tumblr.com/what-is-programming)
* [Downey (2015) Think Java](https://greenteapress.com/thinkjava6/thinkjava.pdf)
