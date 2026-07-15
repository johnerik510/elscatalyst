---
title: "Så påverkar laddtiden din konvertering, och vad du gör åt det"
description: "Varje sekund en sida laddar kostar besökare och affärer. Här är siffrorna som spelar roll och de åtgärder som faktiskt flyttar dem."
pubDate: 2026-06-24
category: "Prestanda"
author: "ELS Catalyst"
readingTime: 6
---

Laddtid är inte en teknisk detalj som lever i bakgrunden. Den är en av de första sakerna en besökare känner, långt innan de läst en rubrik eller sett en produkt. En sida som dröjer skapar tvivel. En sida som kommer direkt skapar förtroende.

Prestanda är en av de första sakerna vi mäter när vi tittar på en sajt. Här går vi igenom vad siffrorna faktiskt säger och vilka åtgärder som ger störst effekt.

## Varför varje sekund räknar

Google har mätt sambandet mellan laddtid och avhopp på mobil. När laddtiden går från en till tre sekunder ökar sannolikheten för avhopp med 32 procent. Går den från en till fem sekunder ökar den med 90 procent. Vid tio sekunder är risken för avhopp mer än fördubblad.

Det handlar inte bara om tålamod. En långsam sida signalerar slarv. Besökaren drar en snabb slutsats: om företaget inte orkar få sin egen sida att fungera, hur ser resten av leveransen ut? Det är en orättvis bedömning, men den sker på under en sekund och den är svår att argumentera bort i efterhand.

## De tre mätvärden du bör känna till

Google samlar prestanda i tre så kallade Core Web Vitals. De är rimliga att förstå även om du inte skriver kod.

**LCP (Largest Contentful Paint)** mäter hur snabbt sidans största innehåll blir synligt, oftast hjältebilden eller rubriken. Målet är under 2,5 sekunder.

**CLS (Cumulative Layout Shift)** mäter hur mycket layouten hoppar medan sidan laddar. Du känner igen det: du ska trycka på en knapp och så flyttar sig allt när en bild dyker upp. Målet är under 0,1.

**INP (Interaction to Next Paint)** mäter hur snabbt sidan svarar när du klickar eller skriver. Målet är under 200 millisekunder.

Alla tre går att mäta gratis i Googles verktyg PageSpeed Insights. Kör din egen sida där innan du läser vidare, siffrorna säger ofta mer än en hel rapport.

## Fyra åtgärder som ger mest per timme

Det finns hundra saker man kan optimera. De flesta ger marginell effekt. Dessa fyra ger nästan alltid mest.

1. **Komprimera och rätt-dimensionera bilder.** Oftast den enskilt största boven. En bild på 3 megabyte som visas i ett litet kort borde vara 80 kilobyte. Använd modernt format som WebP och ladda inte bilder under sidans veck förrän de behövs.

2. **Ta bort skript du inte använder.** Många sajter drar in fem chattverktyg, tre analysverktyg och en bannerlösning som ingen längre minns varför den finns. Varje skript kostar. Rensa hårt.

3. **Servera statiska sidor.** En sida som byggs färdig i förväg och ligger klar på en server är alltid snabbare än en som byggs på nytt vid varje besök. Det är därför vi bygger i Astro, där utgångsläget är ren, statisk HTML.

4. **Använd ett content delivery network.** Ett CDN lägger kopior av din sida nära besökaren geografiskt. En besökare i Malmö hämtar då sidan från en server i närheten istället för en i USA. Cloudflare gör det gratis.

## Prestanda är en färskvara

En snabb sida vid lansering blir långsam med tiden om ingen håller efter den. Ny funktionalitet läggs till, bilder laddas upp utan komprimering, ett plugin till installeras. Efter ett år är sidan tillbaka där den började.

Boka in en enkel kontroll varje kvartal. Kör PageSpeed Insights, titta på de tre mätvärdena och åtgärda det som glidit iväg. Det tar en timme och det håller sajten på rätt sida av gränsen där besökare stannar istället för att lämna.
