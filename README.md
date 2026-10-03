# Canistay – app-prototyp (arbetsnamn: Övernatta)

App-prototyp som avgör om husbilar och husvagnar får övernatta på en plats – baserat på svenska regelverk (nationella trafikföreskrifter, kommunala ordningsstadgor) och öppna geodata (SCB tätorter, Lantmäteriets detaljplaner).

## Kör prototypen

1. Klona repot.
2. Kör 'npx serve .' i mappen (eller öppna index.html direkt i webbläsaren).
3. Obs: prototypen laddar React, Babel och Tailwind från CDN, så internet krävs.

## Status (okt 2026)

- Fristående demo (en enda index.html) med 9 platser: Gävle, Halmstad, Göteborg, Stockholm, Gällivare, Landsort m.fl.
- Täckningsanalys per datalager: SCB tätorter 290/290, trafikföreskrifter (Transportstyrelsen) 290/290, detaljplaner i NGP 252/290, stadga med campingregel ~210/290 (uppskattning).

## Nästa steg

- Verklig GPS-position via geolocation-API:t.
- Server-side proxy mot SCB GeoServer (punkt-i-polygon mot tätorter).
- Wrapa som Android-app: Capacitor ger .apk utan Google Play; PWA är en enklare mellanlösning.

Koden är genererad i Vibe Work (Mistral AI).
