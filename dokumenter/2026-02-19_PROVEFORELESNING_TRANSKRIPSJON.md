# Prøveforelesning: Introduksjon til programmering

# Slides

## 1. Hei,

Navnet mitt er Joschua Thomas Simon-Liedtke. 
Utvikler og forsker innen IKT.

[Jeg har jobbet med programmering siden bachelorstudiene mine, og de siste årene har jeg også forsket innen universell utforming av IKT. 30 sekunder]

## 2. Introduksjon til programmering
Prøveforelesningen i PGR

Målet for i dag: 
* Forstå hva programmering innebærer.
* Forstå hva variabler og funksjoner er.

Du finner eksemplene på: https://github.com/digital-work/pgr102 

[Vi bruker JavaScript som et eksempel. 
I løpet av forelesningen skal dere se hvordan disse kan brukes i praksis for å lage et lite program. 30 sekunder]

## 3. Hva er et program?

Et program er et sett med instruksjoner som forteller en datamaskin hvordan den løser en oppgave steg for steg.

[Bilder]
* Bearbeide tekst
* Bearbeide bilder
* Interagere med brukeren

[Vi bruker programmer til å løse problemer eller utføre oppgaver.
Det kan være å lese og bearbeide tekst, tolke bilder, utføre beregninger eller styre funksjonalitet på en nettside.
I denne forelesningen skal vi fokusere på oppgaver som er relevante for webutvikling og næringsliv – altså ekte nettsteder og digitale løsninger.]

## 4. Hva er programmering?

* Å skrive presise instruksjoner til en datamaskin
* Slik at den kan utføre oppgaver og løse problemer

[ Slik at den kan utføre oppgaver, løse problemer og samhandle med mennesker,
En datamaskin tenker ikke selv.
Den gjør nøyaktig det vi skriver – ikke det vi mener.
Derfor må vi være presise når vi programmerer.
Disse presise instruksjonene skriver vi i et programmeringsspråk. 90 sekunder]

---

5. Hvordan forstår datamaskinen instruksjonene?

Datamaskinen forstår bare maskinspråk
Vi skriver kode i et programmeringsspråk
Programeringsspråk oversettes til maskinspråk før den utføres.

[En datamaskin forstår ikke norsk eller engelsk.
Den forstår maskinspråk.
Enkelt sagt består maskinspråk av nuller og ettall – slik dere kanskje har sett i filmer.
Men det er vanskelig for mennesker å lese og skrive.
Derfor bruker vi programmeringsspråk.
Disse oversettes til maskinspråk før programmet kjøres.]

## 6. JavaScript

Et programmeringsspråk som kan brukes i en nettleser.
Det brukes ofte sammen med HTML og CSS.

[I denne forelesningen bruker vi JavaScript som konkret eksempel på et programmeringsspråk.
JavaScript er mye brukt i webutvikling og i næringslivet.
På en nettside brukes HTML for struktur, CSS for design, og JavaScript for å styre hva som skjer når brukeren gjør noe.]


## 7. Eksempel 1

Statisk melding 

[Eksempel 1](https://digital-work.github.io/pgr102/02_eksempler_grunnleggende-begreper.html?example=1)

```
<button onclick="alert('Hallo Kristiania!')">
    Klikk her
</button>
```

[Her ser dere et veldig enkelt program skrevet i JavaScript, integrert i en nettside.
onclick forteller hva som skal skje når vi klikker.
alert er selv handlingen som kjøres når vi klikker på knappen.
Teksten i anførselstegn er verdien av meldingen som vises av alert. 60 sekunder]

[I dette eksempelet har vi skrevet teksten direkte i koden.
Men hva hvis vi vil bruke et annet navn?
Hva hvis navnet brukes flere steder i programmet?

Pause.

Må vi da lete gjennom hele koden og endre teksten overalt?

I stedet for å skrive teksten direkte i koden, kan vi lagre den ett sted.

Det vi lager heter en variabel og kan gjenbrukes flere steder i programmet.]

## 8. Eksempel 2

Bruk av variabel

[Eksempel 2](https://digital-work.github.io/pgr102/02_eksempler_grunnleggende-begreper.html?example=2)

```
<script>let navn = "Oslo";</script>

<button onclick="alert('Hei ' + navn)">
   Klikk her
</button>
```

[Her har vi laget noe som kalles en variabel.
Vi skriver let navn = "Oslo";.

let betyr at vi oppretter en variabel.
navn er navnet vi gir den.
= betyr at vi gir variabelen en verdi.
"Oslo" er selve verdien som lagres.

I stedet for å skrive teksten direkte i meldingen, bruker vi variabelen navn.
Da kan vi endre verdien ett sted, og den brukes automatisk der vi trenger den.

JavaScript-kode må ligge inne i en <script>-blokk.]

## 9. Variabel

Et navn på en lagret verdi
* Verdien kan brukes flere steder
* Verdien kan endres

[Fordelen med variabler er at verdien kan gjenbrukes flere steder i koden.
En variabel gjør det også enklere å endre verdien.]

## 10. Eksempel 3

Variabler kan endres og gjenbrukes

[Eksempel 3](https://digital-work.github.io/pgr102/02_eksempler_grunnleggende-begreper.html?example=3)

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
Så kan vi endre verdien til "Bergen".
Vi endrer ikke selve koden i knappen.
Knappen gjør fortsatt det samme.
Det eneste vi endrer, er verdien som ligger i variabelen.
Derfor får vi et annet resultat, selv om knappen ser lik ut.

Pause.

Når vi da klikker på knappen, får vi "Hei Bergen".

Pause.

Dette viser at en variabel kan endre verdi underveis i programmet.]

[Så langt har vi skrevet selve koden direkte i knappen.
Det fungerer her med disse små eksmeplene.
Men hva hvis programmet blir større? For eksempel med flere instruksjoner.
Hva hvis vi har flere knapper som skal gjøre den samme verdien?
Slik det er nå hadde vi skrevet koden i enhver enkel knapp. 

Pause

Da kan det fort bli rotete å ha alle instruksjoner direkte i HTML. 
Fordi på komplekse sider, har vi flere HTML tag kombinert med CSS instrukser.]

## 11. Eksempel 4

Bruk av funksjon

[Eksempel 4](https://digital-work.github.io/pgr102/02_eksempler_grunnleggende-begreper.html?example=4)

[For å unngå rotet kan vi samle kode i større blokker som dere kan se her.]

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

[[Nå har vi samlet instruksjonen i en egen blokk et sted.
Instruksjonen er samlet i noe som kalles for funksjon.
siHei er navnet på funksjonen.

Ordet function betyr at vi lager en funksjon.
siHei er navnet vi gir den.

() betyr at vi kan sende inn informasjon, verdier som input.
I dette eksempelet sender vi ikke inn noe informasjon, derfor er parentesene tomme.

Klammeparentesene {} markerer starten og slutten på koden som tilhører funksjonen.

I knappen har vi bare en instruksjon som sier kjør funkjsonen siHei().
Når vi skriver siHei() i knappen, betyr det: kjør funksjonen.
Den gjør akkurat det samme som instruksjonen gjorde da den var skrevet direkte i knappen.]

## 12. Funksjon

En samling instruksjoner:
* utfører én bestemt oppgaver
* kan kalles flere gang når vi trenger den

[En funksjon er en samling instruksjoner som utfører en bestemt oppgave.
I vårt eksempel er oppgaven å vise en melding.
Når vi kaller funksjonen, kjøres instruksjonene inni den.
Dette gjør koden mer strukturert og lettere å lese.]

## 13. Eksempel 5

Input

[Eksempel 5](https://digital-work.github.io/pgr102/02_eksempler_grunnleggende-begreper.html?example=5)

[I ekte programmer har vi ofte en form for brukerinput, for eksempel fra et input-felt.

Her bruker vi JavaScript til å hente verdien som brukeren har skrevet, og så bearbeide den.]

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

[Når vi trykker på knappen, kjøres funksjonen siHei().

Den første linjen i funksjonen henter verdien fra input-feltet.
Deretter bruker vi verdien i meldingen som vises.]

[Så langt har programmet alltid gjort det samme:
Det tar et navn og viser en hilsen.

Men hva hvis brukeren ikke skriver inn noe navn?

Da vil vi kanskje at programmet skal reagere annerledes.]

## 14. Eksempel 6

Bruk av betingelser (if)

[Eksempel 6](https://digital-work.github.io/pgr102/02_eksempler_grunnleggende-begreper.html?example=6)

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

Vi sjekker om variabelen navn er tom.
=== brukes for å sjekke om to verdier er like.
"" betyr en tom tekststreng – altså at brukeren ikke har skrevet noe.

I parentesene etter if skriver vi en betingelse.
Hvis betingelsen er sann, kjøres koden i blokken under.
Hvis ikke, hopper programmet videre – eller kjører else-delen hvis den finnes.

Pause.

I vårt eksempel sjekker vi om variabelen er tom.

Hvis feltet er tomt, viser vi en feilmelding.
Hvis ikke, viser vi hilsenen.

Pause.

Dette gjør at programmet kan ta et valg.]

## 15. Betingelse (if)

Lar programmet ta valg
* Utfører ulik kode avhengig av en betingelse

[ Programmer reagerer forskjellig avhengig av situasjonen.
Uttrykket i parentesene må være sant for at koden skal kjøres.]

## 16. Oppsummering

Hva vi har forstått:
* Hva et program er
* Hva programmering innebærer

Hva vi har brukt:
* Variabler – lagre og gjenbruke verdier
* Funksjoner – samle og strukturere kode
* Betingelser – la programmet ta valg

[I dag har vi først sett på hva programmering er.

Så har vi brukt noen av de mest grunnleggende byggesteinene i et program.

Vi har gått fra en enkel melding
til et lite program som kan ta imot input og reagere forskjellig avhengig av situasjonen.

Vi har brukt JavaScript som eksempel,
men prinsippene gjelder for programmering generelt.]

## 17. Hva skjer videre?

* Mer om variabler og datatyper
* Parametere og returverdier i funksjoner
* Flere typer betingelser
* Løkker og gjentakelse

[I dette kurset vil vi bygge videre på disse grunnleggende begrepene.

Vi skal se nærmere på hvordan vi kan strukturere større programmer,
håndtere mer kompleks input
og skrive mer robust kode.

Programmering handler om å bryte problemer ned i mindre deler
og beskrive løsningene presist.]

## 18. Takk for oppmerksomheten!

Kom med spørsmål eller send e-post til xxx@gmail.com.

# Referanser

* [Shaun Bebbington (2014) What is programming](https://yearofcodes.tumblr.com/what-is-programming)
* [Downey (2015) Think Java](https://greenteapress.com/thinkjava6/thinkjava.pdf)