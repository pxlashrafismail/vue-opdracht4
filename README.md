# Vue - Opdracht 4

### Deel 1 - Vue app
Vul het main.js bestand aan met de juiste code om een vue app aan te maken. Vul ook de ontbrekende code in het index.html bestand in.

Zorg er met npm install voor dat je de dependencies uit het package.json bestand installeert. Met npm run dev kan je de app dan runnen.

### Deel 2 - Data
Definieer 2 eigenschappen in het root-component van de Vue app:
- Titel (*Vue Fundamentals*)
- Intro (*Lorem ipsum...*) 

### Deel 3 - Interpolation
Zorg ervoor dat de 2 eigenschappen die je in de vorige opdracht hebt aangemaakt linkt aan de HTML code:
- h1-element voor de titel
- p-element voor de intro

### Deel 4 - Attribute binding
- Voeg een hyperlink toe aan de template, maak gebruik van een data-eigenschap “linkUrl” om het href attribuut van een waarde te voorzien.
- Voorzie een image als inhoud van de hyperlink, maak gebruik van een data-eigenscahp “imageUrl” om het src attribuut van een waarde te voorzien. Gebruik de verkorte notatie!

### Deel 5 - Methods & functions
Maak een methode die op een dynamische manier de tekst van een paragraaf aanpast. Doe dit op basis van de absolute waarde van een getal:

let randomNumber = Math.random()

- De random methode zal een decimaal getal tussen 0 en 1 genereren.
  - Wanneer het getal kleiner is dan 0.5 geef je de string 
    => “Wij verkopen je de beste producten die je op de markt kan vinden”. 		
  - Is het getal groter van 0.5 dan geef je de string 
    => “Wie zoekt die vindt” terug.
- Toon het resultaat van de methode in een paragraaf.

### Deel 6 - Summary
- Toon jouw volledige naam in een heading element van niveau 2 (*fullName*)
- Toon jouw leeftijd in een paragraaf (*age*)
- Toon jouw leeftijd + 5 jaar in een paragraaf
- Gebruik een methode om een willekeurig getal tussen 0 en 1 te tonen (*showRandom()*)
- Gebruik een anchor-tag om te linken naar de website van Vue.js (*url: 'https://vuejs.org'*)
- Zorg ervoor dat jouw naam standaard ingevuld staat in een input element van type tekst (Tip: value attribuut)

**Breng deze opdracht tot een goed einde door gebruik te maken van data-eigenschappen. Je gebruikt dus geen hard gecodeerde waardes binnen het template gedeelte!**
