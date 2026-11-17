---
title: "Byta domän eller bygga om sajten utan att tappa i Google"
description: "En ny domän eller en ny sajt kan kosta åratal av synlighet i Google. Så planerar du flytten, sätter rätt omdirigeringar och följer upp efteråt."
pubDate: 2026-11-17
category: "Teknik"
author: "ELS Catalyst"
readingTime: 8
---

Många företag gör om sin sajt under vintern. Budgeten för nästa år är lagd, det är lugnare i verksamheten och den nya sajten ska vara på plats till våren. Ibland följer ett domänbyte med, efter ett namnbyte eller en sammanslagning.

Det som ofta glöms bort i planeringen är att Google har lärt sig den gamla sajten. Varje adress som rankar i dag har byggt upp sin plats över tid, med länkar från andra sajter och klick från besökare. Försvinner adressen utan att Google får veta vart den tog vägen, försvinner också den platsen. Den här genomgången visar hur du flyttar utan att börja om från noll.

## Varför tappar sajter trafik när de byggs om?

Trafiken försvinner nästan alltid av samma skäl: adresserna ändras och de gamla leder ingenstans. Google har indexerat varje sida på dess gamla adress. När den adressen plötsligt svarar med ett felmeddelande ser Google en sida som har slutat finnas, inte en sida som har flyttat. Länkarna som pekade dit slutar också göra nytta.

Det räcker att plattformen byts för att det ska hända. En sida som hette `/tjanster/redovisning.html` i det gamla systemet kan heta `/redovisning/` i det nya. För en besökare är det samma sida. För Google är det två olika adresser tills du berättar att de hör ihop.

## Vad är en 301-omdirigering, och varför spelar den roll?

En 301-omdirigering är serverns besked om att en adress har flyttat permanent. Den som besöker den gamla adressen skickas automatiskt vidare till den nya. Enligt [MDN:s beskrivning av statuskoden 301](https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Status/301) följer webbläsaren med direkt, och sökmotorer för över sidans värde till den nya adressen.

Det är just det permanenta som är poängen. [Google skriver i sin guide om omdirigeringar](https://developers.google.com/search/docs/crawling-indexing/301-redirects?hl=sv) att en permanent omdirigering är en signal om att den nya adressen ska visas i sökresultaten. En tillfällig omdirigering, som 302, gör att Google behåller den gamla adressen som huvudversion. Det är ett vanligt misstag: tekniken fungerar för besökaren, men Google får fel besked.

Statuskoden 308 fungerar på samma sätt som 301 för Google. Skillnaden är teknisk och handlar om formulär som skickas, något din utvecklare kan avgöra.

## Hur förbereder du flytten?

Börja med en lista över alla adresser sajten har i dag. Det är det viktigaste förarbetet och det som oftast hoppas över. Google rekommenderar i sin [guide om att flytta en webbplats med ändrade adresser](https://developers.google.com/search/docs/crawling-indexing/site-move-with-url-changes?hl=sv) att du hämtar adresserna från flera håll: sajtkartan, analysverktyget, serverns loggar och publiceringssystemet.

Lägg sedan till en kolumn med den nya adressen för varje gammal. Det kallas en omdirigeringskarta, och den är grunden för allt som kommer efter. Tre saker är bra att tänka på när du fyller i den:

- **Peka till den mest likartade sidan.** Den gamla sidan om redovisning ska leda till den nya sidan om redovisning, inte till startsidan. Google varnar för att många adresser som omdirigeras till en sida utan samband, till exempel startsidan, kan behandlas som sidor som inte finns.
- **Glöm inte bilder och filer.** Prislistor i pdf, produktbilder och andra filer som har länkar till sig behöver också en ny adress om de flyttas.
- **Bestäm vad som inte ska följa med.** Innehåll du tar bort ska svara med att sidan inte finns, alltså statuskoden 404 eller 410. Det är bättre än att tvinga in det på en sida där det inte hör hemma.

Prioritera sidorna med mest trafik och flest länkar. I Search Console ser du vilka sidor som får klick, något vi går igenom i [Google Search Console för företagare](/blogg/search-console-for-foretagare/).

## Hur sätter du upp omdirigeringarna rätt?

Lägg omdirigeringarna på servern, inte i sidans kod. Google tolkar serverns 301 och 308 mest pålitligt. En omdirigering som görs med JavaScript fungerar bara om Google lyckas köra skriptet, och Google skriver själv att den bara ska användas när inget annat går.

Peka varje gammal adress direkt till sitt slutmål. Har sajten byggts om flera gånger finns det ofta kedjor där en adress leder till en annan som leder till en tredje. Google kan följa upp till tio steg, men rekommenderar att du håller dig till högst tre och aldrig fler än fem. Varje steg gör det långsammare för besökaren och osäkrare för sökmotorn.

Uppdatera också sajtens egna länkar. Menyn, sidfoten och länkarna i texterna ska peka direkt på de nya adresserna, inte gå omvägen via en omdirigering. Detsamma gäller kanoniska taggar, som ska peka på den nya sidan själv.

## Vad gör du på flyttdagen?

Slå på omdirigeringarna samtidigt som den nya sajten publiceras. Testa sedan ett urval av gamla adresser, särskilt de viktigaste från listan, och kontrollera att var och en leder till rätt sida med statuskoden 301.

Kontrollera att den nya sajten inte är spärrad för sökmotorer. Under utveckling stängs testsajter ofta av med en noindex-tagg eller en rad i robots.txt. Följer den spärren med till den skarpa sajten syns ingenting i Google, hur bra omdirigeringarna än är.

Skicka sedan in den nya sajtkartan i Search Console. Google rekommenderar att du under en övergångsperiod har en sajtkarta för de gamla adresserna och en för de nya, så att Google hittar omdirigeringarna snabbare. Den gamla tar du bort när flytten är klar.

## Vad gäller när du byter domän?

Vid ett domänbyte finns ett verktyg till: Adressändring i Search Console. Där talar du om för Google att hela den gamla domänen har flyttat till den nya. Enligt [Search Console-hjälpen om verktyget för adressändring](https://support.google.com/webmasters/answer/9370220?hl=sv) måste du vara verifierad ägare av båda domänerna med samma Google-konto, och den gamla startsidan ska ha en 301-omdirigering till den nya.

Verktyget används bara för byte av domän eller underdomän. Det används inte för ett byte från http till https, inte för att flytta enskilda sidor och inte för ett byte mellan www och utan www på samma domän. Har du verifierat flera varianter av den gamla domänen, till exempel med och utan www, gör du adressändringen för var och en.

Google skickar signaler från den gamla domänen till den nya i 180 dagar efter att adressändringen har startats. Säg därför aldrig upp den gamla domänen i samband med flytten. Förnya den och låt omdirigeringarna ligga kvar.

## Hur länge ska omdirigeringarna ligga kvar?

Så länge som möjligt, och i regel minst ett år. Det är Googles egen rekommendation i guiden om flytt av webbplatser. Länkar från andra sajter, gamla bokmärken och adresser i utskick fortsätter att peka på de gamla adresserna i många år. Varje gång någon klickar på en sådan länk ska den leda rätt.

Omdirigeringarna kostar nästan ingenting att låta vara. Att ta bort dem i förtid kan däremot göra att värdet från länkarna som fortfarande pekar på de gamla adresserna går förlorat.

## Hur vet du att flytten har lyckats?

Räkna med att rankingen svajar en tid. Google skriver att det är normalt medan sajten genomsöks och indexeras på nytt, och att en medelstor sajt kan behöva några veckor eller mer innan flytten är klar. Större sajter tar längre tid. Flytten räknas som klar först när Google har besökt varje gammal och ny adress minst en gång.

Följ tre saker varje vecka under de första två månaderna:

1. **Indexeringen.** Rapporten Sidor i Search Console ska visa att de nya adresserna blir indexerade och att de gamla försvinner i takt med det.
2. **Felen.** Leta efter adresser som svarar med 404. Varje sådan som borde ha haft en omdirigering är en miss att rätta direkt.
3. **Trafiken.** Klick och visningar på den gamla sajten ska sjunka i samma takt som de ökar på den nya.

En ny sajt är också ett bra tillfälle att göra den snabbare. Varför det påverkar både ranking och affärer går vi igenom i [hur laddtiden påverkar konverteringen](/blogg/laddtid-och-konvertering/).

## Vanliga frågor

### Tappar man alltid placeringar när man byter domän?

En tillfällig svängning är normal medan Google läser in sajten på nytt. Med en fullständig omdirigeringskarta, permanenta omdirigeringar och adressändring i Search Console brukar placeringarna komma tillbaka. Det som ger bestående förluster är saknade omdirigeringar och omdirigeringar till fel sida.

### Räcker det att omdirigera allt till den nya startsidan?

Nej. Google kan behandla många omdirigeringar till en sida utan samband som sidor som inte finns, och då förs inget värde över. Varje gammal sida ska leda till den nya sida som bäst motsvarar den.

### Ska man byta domän och bygga om sajten samtidigt?

Det går, men det blir svårare att se vad som orsakar ett tapp om något går fel. Kan du dela upp det, byt plattform först och domän när den nya sajten har satt sig. Måste allt ske samtidigt är omdirigeringskartan ännu viktigare.

### Behöver jag göra något om bara designen ändras?

Om alla adresser är desamma behövs inga omdirigeringar. Kontrollera ändå att rubriker, texter och interna länkar finns kvar, eftersom det är innehållet som rankar. En ny design som tar bort text kan kosta placeringar även när adresserna står still.

Planerar du en ny sajt eller ett domänbyte och vill att flytten görs rätt från början? [Hör av dig](/#kontakt), så går vi igenom planen tillsammans.
