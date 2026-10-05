# Canistay – app-prototyp (arbetsnamn: Övernatta)

App-prototyp som avgör om husbilar och husvagnar får övernatta på en plats – baserat på svenska regelverk (nationella trafikföreskrifter, kommunala ordningsstadgor) och öppna geodata.

## Kör prototypen

1. Klona repot.
2. Kör 'npx serve .' i mappen (eller öppna index.html direkt i webbläsaren).
3. Obs: React/Babel laddas från unpkg och stilar är inbäddade som fallback – internet krävs för CDN-biblioteken.

## Funktioner (okt 2026)

- Verdict per plats: Ja / Kontrollera / Nej, med förklaring, källor och paragrafer.
- Riktig GPS-position via geolocation-API:t + kommunuppslag via OpenStreetMap (Nominatim). Matchar positionen mot granskade kommuner.
- 12 platser i registret: 9 demo-platser samt tre manuellt granskade kommuner (okt 2026): Ockelbo (gratis parkering, inget känt campingförbud), Sandviken (camping = över en natt – en natt i husbilen/husvagnen är ok) och Hedemora (campingförbud inom detaljplan, Gävle-modellen).
- Karta med platser, regelverk-sammanställning, täckningsanalys och användarrapporter.
- Inbäddad fallback-CSS + ErrorBoundary (visar felmeddelande vid krasch).

## Täckningsanalys per lager

SCB tätorter 290/290, trafikföreskrifter 290/290, detaljplaner i NGP 252/290, stadga med campingregel ~210/290 (uppskattning).

## Nästa steg

- Server-side proxy mot SCB GeoServer (punkt-i-polygon mot tätorter, istället för Nominatim-proxy).
- Komplettera granskade kommuner (ordningsstadgor) – Ockelbo, Sandviken och Hedemora är klara.
- Wrapa som Android-app: Capacitor ger .apk utan Google Play; PWA är en enklare mellanlösning.

Koden är genererad i Vibe Work (Mistral AI).
