---
title: "Tillgänglighetslagen: gäller den din företagssajt?"
description: "Tillgänglighetslagen gäller sedan juni 2025 för webbutiker och andra tjänster till konsumenter. Så avgör du om din sajt omfattas och vad du rättar först."
pubDate: 2026-11-10
category: "UX"
author: "ELS Catalyst"
readingTime: 7
---

Sedan den 28 juni 2025 finns en lag som ställer krav på hur tillgängliga vissa företags webbplatser och appar ska vara. Många företagare har hört talas om den, färre vet om den gäller dem. Frågan är värd att reda ut, eftersom Post- och telestyrelsen, PTS, har tillsyn över e-handeln och kan ta ut avgifter av den som inte följer lagen.

Det här är en genomgång för dig som äger en företagssajt och vill veta två saker: omfattas jag, och vad gör jag i så fall först?

## Vad är tillgänglighetslagen?

Tillgänglighetslagen är det vardagliga namnet på [lag (2023:254) om vissa produkters och tjänsters tillgänglighet](https://www.riksdagen.se/sv/dokument-och-lagar/dokument/svensk-forfattningssamling/lag-2023254-om-vissa-produkters-och-tjansters_sfs-2023-254/). Den genomför EU:s tillgänglighetsdirektiv och trädde i kraft den 28 juni 2025. Lagen kräver att vissa tjänster till konsumenter, bland dem e-handel, bank- och betaltjänster och elektronisk kommunikation, går att använda för personer med funktionsnedsättning.

Det är alltså ingen allmän lag för alla webbplatser. Den gäller specifika tjänster. Offentliga aktörer har sedan tidigare en egen lag, lagen om tillgänglighet till digital offentlig service, som Digg ansvarar för. Den berör inte privata företag.

## Omfattas din företagssajt?

Det avgörande är vad sajten gör, inte vilken bransch du är i. [PTS skriver](https://pts.se/tillganglighetslagen/) att det är produkten eller tjänsten som avgör, inte typen av aktör. För de flesta företagssajter är frågan om sajten är en e-handelstjänst: en tjänst på distans, via webbplats eller app, där en konsument på eget initiativ kan ingå ett avtal med dig.

Säljer du till privatpersoner i en webbutik omfattas du med stor sannolikhet. Kan en konsument boka och betala en tjänst direkt på sajten ligger du också nära definitionen.

Har du däremot en ren presentationssajt, där besökaren läser om tjänsterna och sedan hör av sig via ett kontaktformulär, ingås inget avtal på sajten. Säljer du bara till andra företag riktar sig tjänsten inte till konsumenter. I båda fallen faller sajten sannolikt utanför. PTS lämnar dock inga förhandsbesked, så bedömningen är din egen. Skriv ner den och spara den.

## Hur små företag slipper kraven?

Lagen undantar mikroföretag som tillhandahåller tjänster. Enligt lagens definition är ett mikroföretag ett företag med färre än tio anställda och en årsomsättning eller en årlig balansomslutning som inte överstiger 2 miljoner euro. Uppfyller du det behöver din webbutik inte leva upp till tillgänglighetskraven, även om den annars hade omfattats.

Två saker är värda att tänka på. Undantaget gäller tjänster, och reglerna för den som säljer vissa produkter, till exempel datorer eller läsplattor, ser annorlunda ut. Och ett företag som växer förbi gränsen omfattas från den dagen. Bygger du en ny webbutik i dag och planerar att växa är det billigare att göra rätt från början än att bygga om senare.

## Vilka krav ställs på en webbutik?

Kraven handlar enligt PTS om information om tjänstens tillgänglighet, ett tillgängligt gränssnitt med en funktionell utformning och stödtjänster som går att använda. Sajten ska alltså fungera även för den som navigerar med tangentbord eller använder skärmläsare, och du ska berätta hur tillgänglig tjänsten är. Själva lagtexten pekar inte ut någon WCAG-nivå, utan de tekniska kraven hänger ihop med europeisk standard.

Standarden som används i EU heter EN 301 549. [EU-kommissionen beskriver](https://digital-strategy.ec.europa.eu/en/policies/web-accessibility-directive-standards-and-harmonisation) att den gällande versionen i hög grad bygger på WCAG 2.1, med några krav utöver. Enligt [W3C](https://www.w3.org/WAI/standards-guidelines/wcag/) bygger 2026 års version av EN 301 549 på WCAG 2.2. I praktiken är WCAG alltså måttstocken du och din utvecklare arbetar efter.

WCAG står för Web Content Accessibility Guidelines och delar in sina krav i tre nivåer: A, AA och AAA. Kraven vilar på fyra principer: innehållet ska gå att uppfatta, gå att hantera, vara begripligt och vara robust nog att fungera i olika webbläsare och hjälpmedel.

## Vad kontrollerar du själv först?

Du behöver inte kunna koda för att hitta de vanligaste bristerna. Fem kontroller tar en eftermiddag och ger dig en bra bild av läget.

**Använd bara tangentbordet.** Lägg undan musen och ta dig igenom ett helt köp med Tab, Enter och mellanslag. Ser du hela tiden var du befinner dig? Kommer du fram till kassan? Fastnar du i en meny eller en popup är det ett fel som stänger ute alla som inte kan använda mus.

**Titta på kontrasten.** WCAG kräver på nivå AA ett [kontrastförhållande på minst 4,5:1](https://www.w3.org/WAI/WCAG22/Understanding/contrast-minimum.html) mellan vanlig text och bakgrund, och 3:1 för stor text. Ljusgrå text på vit bakgrund och vit text på en bild är de vanligaste syndarna. Det finns gratis kontrastverktyg där du klistrar in två färgkoder och får svaret direkt.

**Läs formulären.** Varje fält ska ha en synlig etikett som är kopplad till fältet i koden. Står etiketten bara som grå platshållartext inne i fältet försvinner den när besökaren börjar skriva, och en skärmläsare har ofta inget att läsa upp. [MDN:s genomgång av tillgänglig HTML](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Accessibility/HTML) visar hur kopplingen ska se ut.

**Granska bilderna.** Produktbilder och bilder som bär information behöver en alternativtext som beskriver vad bilden visar. Rent dekorativa bilder ska ha en tom alternativtext så att skärmläsaren hoppar över dem. Text som bara finns inbakad i en bild går inte att läsa för den som inte ser.

**Kolla rubrikerna.** Sidan ska ha en riktig rubrikstruktur, inte bara text som ser stor ut. Skärmläsare låter användaren hoppa mellan rubriker ungefär som du skummar en sida med blicken. Utan struktur blir sidan ett enda långt textblock.

De här kontrollerna hittar inte allt, men de fångar mycket av det som oftast är fel. Flera av dem är dessutom samma sak som gör en sajt lättare att använda för alla, något vi skrivit om i [UX-misstag som tyst kostar dig kunder](/blogg/ux-misstag-som-kostar-kunder/).

## Vad händer om sajten inte uppfyller kraven?

PTS har tillsyn över e-handelstjänster och kan förelägga ett företag att rätta bristerna. Ett föreläggande kan förenas med vite. Lagen ger också möjlighet att ta ut en sanktionsavgift på lägst 10 000 och högst 10 000 000 kronor. I ringa fall ska ingen avgift tas ut.

Det finns även en möjlighet till undantag om kraven skulle innebära en oproportionerligt stor börda för företaget eller kräva en väsentlig förändring av tjänsten. Den bedömningen ska dokumenteras och meddelas tillsynsmyndigheten. Det är inget du kan hävda i efterhand när PTS hör av sig.

## Är tillgänglighet bara en kostnad?

Nej. Det mesta av det lagen kräver är samma saker som gör en sajt bättre för alla besökare: tydlig kontrast i solljus på mobilen, formulär som går att fylla i utan att gissa, knappar som fungerar oavsett hur man navigerar. Det hjälper konverteringen, inte bara efterlevnaden.

Det finns också en teknisk vinst. Riktig HTML med korrekta rubriker, etiketter och knappar är lättare för sökmotorer att tolka och oftast snabbare att ladda än lösningar som bygger allt med skript. Prestanda och tillgänglighet drar åt samma håll, något du ser i [hur laddtiden påverkar konverteringen](/blogg/laddtid-och-konvertering/).

## Vanliga frågor

### Gäller tillgänglighetslagen alla företags hemsidor?

Nej. Lagen gäller vissa tjänster till konsumenter, framför allt e-handel, banktjänster och elektronisk kommunikation. En presentationssajt där inget avtal ingås och en sajt som bara riktar sig till företag faller i regel utanför. Mikroföretag som tillhandahåller tjänster är undantagna.

### Vilken WCAG-nivå ska en webbutik uppfylla?

Lagtexten anger ingen nivå. Kraven kopplas till den europeiska standarden EN 301 549, som bygger på WCAG. Den som vill vara säker utgår från WCAG:s kriterier på nivå A och AA, där till exempel kraven på kontrast och tangentbordsnavigering finns.

### Räcker det med ett tillgänglighetsverktyg som läggs ovanpå sajten?

Ett skript som lägger till en meny för textstorlek och kontrast rättar inte grundfelen i koden. Saknade etiketter, bilder utan alternativtext och menyer som inte går att nå med tangentbordet finns kvar under ytan. Rätta själva sajten i stället.

### Vem kontrollerar att lagen följs?

PTS har tillsyn över e-handel, banktjänster och elektronisk kommunikation. Myndigheten tar också emot rapporter om brister i tjänster. För andra delar av lagen ansvarar bland andra Konsumentverket, Transportstyrelsen och Mediemyndigheten.

Driver du en webbutik och vill veta hur den står sig mot kraven, eller bygger du nytt och vill göra rätt från början? [Hör av dig](/#kontakt), så går vi igenom sajten tillsammans.
