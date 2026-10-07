# Canistay – app-prototyp (arbetsnamn: Övernatta)

App-prototyp som avgör om husbilar och husvagnar får övernatta på en plats – baserat på svenska regelverk (nationella trafikföreskrifter, kommunala ordningsstadgor) och öppna geodata.

## Kör prototypen

1. Klona repot.
2. Kör 'npx serve .' i mappen (eller öppna index.html direkt i webbläsaren).
3. Obs: React/Babel laddas från unpkg och stilar är inbäddade som fallback – internet krävs för CDN-biblioteken.

## Funktioner (okt 2026)

- Verdict per plats: Ja / Kontrollera / Nej, med förklaring, källor och paragrafer.
- Riktig GPS-position via geolocation-API:t + kommunuppslag via OpenStreetMap (Nominatim). Matchar positionen mot granskade kommuner.
- 17 platser i registret: 9 demo-platser, fyra manuellt granskade kommuner (okt 2026): Ockelbo (gratis parkering, inget känt campingförbud), Sandviken (camping = över en natt – en natt är ok), Hedemora (campingförbud inom detaljplan, Gävle-modellen) och Avesta (avgiftsfri parkering, ingen känd campingregel, P-förbudszon i tätort) – samt fyra manuellt granskade skyddade områden (okt 2026): Trollberget naturreservat (Ockelbo), Lundbosjön naturreservat (Ockelbo/Gävle, 21FS 2019:16), Västerhällarna naturreservat (Sandviken, 21FS 2021:6) och Färnebofjärdens nationalpark (Avesta/Sandviken, NFS 2014:16). Reservatens föreskrifter presenterar även regler för eldning, hund och tillträdesförbud.
- Karta med platser, regelverk-sammanställning, täckningsanalys och användarrapporter.
- Inbäddad fallback-CSS + ErrorBoundary (visar felmeddelande vid krasch).

## Täckningsanalys per lager

SCB tätorter 290/290, trafikföreskrifter 290/290, detaljplaner i NGP 252/290, stadga med campingregel ~210/290 (uppskattning).

## Nästa steg

- Server-side proxy mot SCB GeoServer (punkt-i-polygon mot tätorter, istället för Nominatim-proxy).
- Komplettera granskade kommuner (ordningsstadgor) – Ockelbo, Sandviken, Hedemora och Avesta är klara.
- Wrapa som Android-app: Capacitor ger .apk utan Google Play; PWA är en enklare mellanlösning.

Koden är genererad i Vibe Work (Mistral AI).
