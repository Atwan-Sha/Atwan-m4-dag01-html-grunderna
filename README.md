# Dag 1 · HTML-grunderna

*Modul 4, UI/UX & Frontendutveckling, Lexicon IT-Proffs*

## Vad du ska göra idag

Du bygger HTML-strukturen för startsidan till det fiktiva kaféet **Kafé Kardemumma**. Ingen CSS idag. Sidan ska se enkel ut, men vara **rätt uppbyggd**.

## Bakgrund

HTML beskriver vad innehållet *är*: en rubrik, ett stycke, en lista, en länk. Utseendet kommer med CSS på dag 3. Idag tränar du på att välja rätt element. Texten du ska använda ligger i `innehall.md`, så du slipper hitta på egna texter.

## Så arbetar du (varje dag)

Du använder Git från första dagen. Du behöver inte förstå allt bakom kommandona än, det gör vi på dag 9. Tills dess använder du dem som ett recept.

### Engångsinställning (bara dag 1)

Öppna terminalen i VS Code (Ctrl+ö) och kör, med ditt eget namn och din e-post från GitHub:

```
git config --global user.name "Ditt Namn"
git config --global user.email "din@epost.se"
```

### Flödet

1. **Forka repot.** Klicka på *Fork* uppe till höger på GitHub, sedan *Create fork*. Du får en egen kopia under ditt användarnamn.
2. **Klona din fork.** Klicka på den gröna knappen *Code*, fliken *HTTPS*, och kopiera adressen. I terminalen: gå till den mapp där du vill ha dina projekt (till exempel `cd Documents`) och skriv `git clone ` följt av adressen.
3. **Öppna den nya mappen i VS Code** (*File → Open Folder*). Starta *Live Server* (högerklicka på `index.html` → *Open with Live Server*).
4. **Gör uppgiften.** Spara ofta. Webbläsaren uppdateras av sig själv.
5. **Spara i Git och skicka upp.** I terminalen, i projektmappen:
   ```
   git add .
   git commit -m "Dag 1: bygger sidans struktur"
   git push
   ```
   Meddelandet mellan citattecknen ska beskriva vad du gjorde. Första gången du kör `git push` öppnas ett fönster där du loggar in på GitHub via webbläsaren. Det görs bara en gång.
6. **Kontrollera på GitHub.** Ladda om din fork. Din commit syns under *Commits*.
7. **Lämna in i Microsoft Forms** (länk finns i kanalen). Du klistrar in länken till din fork.

Fastnar du: skriv ner exakt var och vad du försökt, och ta det först i nästa handledda pass.

## Uppgiften steg för steg

### Steg 1. Skapa dokumentets skelett

Öppna `index.html`. Skriv `<!DOCTYPE html>`, ett `<html lang="sv">`-element, ett `<head>` med `<meta charset="UTF-8">`, `<meta name="viewport" content="width=device-width, initial-scale=1.0">` och en `<title>`, samt ett `<body>`. Spara och öppna med Live Server. Fliken ska visa din titel.

### Steg 2. Bygg sidhuvudet

I `<body>`: lägg ett `<header>` med en `<h1>` (kaféets namn) och en `<nav aria-label="Huvudmeny">` som innehåller en `<ul>` med tre `<li>`, var och en med en länk (`<a>`). Länkarna ska peka på `#meny`, `#om-oss` och `kontakt.html`.

### Steg 3. Bygg huvudinnehållet

Lägg ett `<main>` med tre `<section>`-element med id `hero`, `meny` och `om-oss`. Varje section får en `<h2>`. Hero får ett stycke och en länk till menyn. Använd texterna i `innehall.md`.

### Steg 4. Bygg menyn

Lägg en `<div class="meny-lista">` under rubriken. I den är varje maträtt ett eget `<article>` med bild (`<img>` **med alt-text**), en `<h3>`, ett stycke och priset. Tre rätter ska finnas. Bilderna ligger i mappen `images/`.

### Steg 5. Bygg Om oss och sidfoten

I `om-oss`: en bild med alt-text och två stycken. Sist på sidan ett `<footer>` med copyrightrad och en `<address>` med adress och en `mailto:`-länk.

### Steg 6. Kontrollera din kod

Gå till validator.w3.org, välj *Validate by direct input*, klistra in din kod och klicka *Check*. Rätta tills det står "Document checking completed. No errors". Kontrollera också att rubrikerna följer hierarkin: en `<h1>`, sedan `<h2>`, sedan `<h3>` utan hopp.

## Kontrollista: så vet du att du är klar

- [ ] Dokumentet har `<!DOCTYPE html>`, `lang="sv"`, charset, viewport och en egen titel.
- [ ] Det finns exakt en `<h1>` och rubrikhierarkin hoppar inte.
- [ ] Sidan använder `<header>`, `<nav>`, `<main>`, `<section>`, `<article>` och `<footer>`, inte `<div>` i onödan.
- [ ] Alla bilder har en beskrivande `alt`-text.
- [ ] Menyn är en `<ul>`-lista med länkar. Länkarna fungerar.
- [ ] W3C-validatorn ger inga fel.
- [ ] Du har gjort commit och push till din fork och skickat in länken i Forms.

## Tips om du fastnar

- Glömt stänga en tagg? Varje `<section>` behöver en `</section>`. Rätta indenteringen så ser du var det saknas.
- Bilden syns inte? Kontrollera sökvägen: `images/bulle.svg`, med små bokstäver, utan mellanslag.
- Sidan ser tråkig ut? Det är meningen. Utseendet kommer dag 3.
- Osäker på vilket element du ska använda? Fråga dig: "Vad ÄR det här?" Inte "Hur ska det se ut?"

## Inlämning

**Deadline: imorgon klockan 09.00.** Allt lämnas in i Microsoft Forms. Du behöver inte redovisa något muntligt.

I formuläret fyller du i:

1. Länk till din fork av det här repot.
2. Reflektion: Vilket HTML-element var nytt för dig idag, och vad tror du att det gör för användare som använder skärmläsare?

## Vill du mer? (frivilligt)

- Lägg till en fjärde maträtt med eget `<article>`.
- Lägg till en `<button>` någonstans och förklara med en kommentar i koden varför det är bättre än en `<div>` som ser ut som en knapp.
