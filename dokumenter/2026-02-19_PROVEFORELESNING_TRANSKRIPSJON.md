# Prøveforelesning: Introduksjon til programmering

# Slides

## 1. Hallo!

Navnet mitt er Joschua Thomas Simon-Liedtke.  
Jeg er utvikler og forsker innen IKT.

[Jeg har jobbet med programmering siden bachelorstudiene mine.  
De siste årene har jeg forsket på universell utforming av IKT.]

## 2. Introduksjon til programmering

Prøveforelesningen i PGR102

Målet for i dag:  
* Forstå hva programmering innebærer.  
* Forstå hva variabler og funksjoner er.

Du finner eksemplene på: https://github.com/digital-work/pgr102  

[Vi bruker JavaScript som eksempel.  
Vi skal gå fra en enkel melding til et lite program.]

## 3. Hva er et program?

Et program er et sett med instruksjoner som forteller en datamaskin hvordan den løser en oppgave steg for steg.
* Bearbeide tekst  
* Bearbeide bilder  
* Samhandle med brukeren  

[Programmer brukes til å løse problemer eller utføre konkrete oppgaver.  
Det kan være oppgaver relatert til tekst, bilder, brukerinteraksjon eller beregninger.  
I dag fokuserer vi på oppgaver som er relevante for webutvikling.]

## 4. Hva er programmering?

* Å skrive presise instruksjoner til en datamaskin  
* Slik at den kan utføre oppgaver og løse problemer  

[En datamaskin tenker ikke selv.  
En datamaskin gjør nøyaktig det vi skriver.  
Ikke det vi mener.  
Derfor må vi være presise.  
Men en datamaskin forstår ikke norsk eller engelsk.]

## 5. Hvordan forstår datamaskinen instruksjonene?

Datamaskinen forstår bare maskinspråk  
Vi skriver kode i et programmeringsspråk  
Programmeringsspråk oversettes til maskinspråk før programmet utføres

[Maskinspråk består av nuller og ettall.  
Det er vanskelig for mennesker å lese.  
Derfor bruker vi programmeringsspråk.  
Programmeringsspråk oversettes til maskinspråk før programmet kjøres.]

## 6. JavaScript

Et programmeringsspråk som kan brukes i en nettleser.  
Det brukes ofte sammen med HTML og CSS.

[Eksempel](https://digital-work.github.io/pgr102/01-html-css-js-demo.html)

[JavaScript er et programmeringsspråk som er mye brukt i webutvikling og i næringslivet.  
I nettleseren brukes HTML for struktur.  
CSS for design.  
JavaScript for logikk og interaksjon.]

## 7. Eksempel 1

Statisk melding  

[Eksempel 1](https://digital-work.github.io/pgr102/02_eksempler_grunnleggende-begreper.html?example=1)

```
<button onclick="alert('Hallo Kristiania!')">
    Klikk her
</button>
```

[Her ser dere et enkelt program skrevet i JavaScript,  
integrert i en nettside.  
onclick bestemmer hva som skjer når vi klikker.  
alert viser en melding på skjermen.  
Teksten i anførselstegn er verdien som vises i meldingen.  

Her har vi skrevet teksten direkte i koden.  
Hvis vi vil bruke et navn flere steder eller endre det,  
må vi gå gjennom koden for å endre overalt.  
Det er upraktisk.]

## 8. Eksempel 2

Bruk av variabel  

[Eksempel 1](https://digital-work.github.io/pgr102/02_eksempler_grunnleggende-begreper.html?example=2)

```
<script>
let navn = "Oslo";
</script>

<button onclick="alert('Hei ' + navn)">
   Klikk her
</button>
```

[Vi kan lagre teksten i en variabel –  
et navn på en verdi som kan brukes flere steder.  

Her skriver vi: let navn = "Oslo";  
let oppretter variabelen,  
navn er navnet,  
= tildeler verdien,  
og "Oslo" er selve verdien.  

Når vi bruker variabelen i meldingen,  
kan vi endre verdien ett sted,  
og den oppdateres automatisk gjennom hele programmet.  

JavaScript-kode må ligge i en <script>-blokk.]

## 9. Variabel

Et navn på en lagret verdi  
* Verdien kan brukes flere steder  
* Verdien kan endres  

[Variabler gjør koden enklere å vedlikeholde.  
Det er enklere å endre verdien.  
Verdien kan gjenbrukes.  ]

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

[Her endrer vi bare verdien i variabelen.  
Koden i knappen er uendret, men resultatet blir annerledes.  

Først setter vi navn til "Oslo",  
så endrer vi det til "Bergen".  
Når vi klikker, får vi "Hei Bergen"  
fordi den siste verdien brukes.  

Dette viser at en variabel kan endres underveis i programmet.
Vi ser også at samme variabel kan brukes på to ulike knapper.]

[Så langt har vi skrevet koden direkte i knappen.  
Det fungerer i små eksempler,  
men i større programmer med flere elementer  
blir det fort rotete.  
Da trenger vi en bedre struktur.]

## 11. Eksempel 4

Bruk av funksjoner  

[Eksempel 4](https://digital-work.github.io/pgr102/02_eksempler_grunnleggende-begreper.html?example=4)

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

[Nå har vi samlet instruksjonen i en funksjon.  
function betyr at vi oppretter en funksjon,  
og siHei er navnet.  

() kan ta imot input,  
men her er de tomme fordi vi ikke har noen input.  
{} markerer koden som hører til funksjonen.  

I knappen skriver vi bare siHei().  
Da kjøres funksjonen,  
og gjør det samme som koden gjorde tidligere.]

## 12. Funksjon

En samling instruksjoner:  
* utfører én bestemt oppgave  
* kan kalles flere ganger  

[En funksjon er en samling instruksjoner som utfører en oppgave.  
Her viser den en melding.  
Når vi kaller funksjonen, kjøres koden inni den.  
Det gjør koden mer strukturert, oversiktlig og lettere å lese.  
I praksis brukes funksjoner for å dele opp større systemer  
slik at flere utviklere kan jobbe på samme kodebase.  

Så langt har verdien vi brukte vært statisk.  
I ekte programmer får vi ofte input fra brukeren.  

Da kan vi bruke JavaScript for å hente og bearbeide verdien.]

## 13. Eksempel 5

Input  

[Eksempel 5](https://digital-work.github.io/pgr102/02_eksempler_grunnleggende-begreper.html?example=5)

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

[I dette eksempelet legger vi til et tekstfelt med id navnInput.  
Når vi trykker på knappen, kjøres fortsatt funksjonen siHei,  
men nå henter den verdien fra input-feltet  
og bruker teksten brukeren har skrevet i meldingen.  

Så langt viser programmet bare en hilsen basert på navnet.  
Men hva skjer hvis feltet er tomt?
Da vil vi at programmet skal reagere annerledes.]

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

En if-setning betyr:  
Hvis betingelsen i parentesene er sann,  
kjører vi koden i blokken under.  

Her sjekker vi om variabelen navn er tom.  
=== betyr at vi tester om to verdier er like.  
"" representerer en tom tekst.  

Er betingelsen sann,  
kjøres koden i if-blokken, altså feilmeldingen.  
Er den ikke sann,  
kjøres koden i else-blokken, altså hilsenen.

Dette gjør at programmet kan ta et valg  
basert på situasjonen.]

## 15. Betingelse (if)

Lar programmet ta valg  
* Utfører ulik kode avhengig av en betingelse  

[Med if kan programmet reagere forskjellig avhengig av situasjonen.  
Koden kjøres bare når betingelsen i parentesene er sann.]

## 16. Oppsummering

Hva vi har forstått:
* Hva et program er  
* Hva programmering innebærer  

Hva vi har brukt:
* Variabler – lagre og gjenbruke verdier  
* Funksjoner – samle og strukturere kode  
* Betingelser – la programmet ta valg  

[I dag har vi sett hva et program er,  
og hva programmering innebærer – å skrive presise instruksjoner.  

Vi har brukt tre grunnleggende byggesteiner:  
variabler, funksjoner og betingelser.  

Vi har gått fra en enkel melding  
til et program som tar imot input og tar valg.  

Vi brukte JavaScript som eksempel,  
men prinsippene gjelder generelt.]

## 17. Hva skjer videre?

* Variabler og datatyper  
* Parametere og returverdier  
* Flere typer betingelser  
* Løkker og gjentakelse

[I  dette kurset bygger vi videre på disse begrepene.  
Vi skal lage større programmer, håndtere mer kompleks input,  
og lære å skrive kode som andre kan lese, forstå og videreutvikle.  

I arbeidslivet jobber man sjelden alene.  
Koden skal fungere – men den skal også være forståelig for andre i teamet.]]

## 18. Takk for oppmerksomheten!

Kom med spørsmål eller send e-post til drjthsl@gmail.com.

# Referanser

* [Shaun Bebbington (2014) What is programming](https://yearofcodes.tumblr.com/what-is-programming)
* [Downey (2015) Think Java](https://greenteapress.com/thinkjava6/thinkjava.pdf)
