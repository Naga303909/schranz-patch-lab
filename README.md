# Schranz Patch Lab — Beta 2.0 (Android PWA)

Gecombineerde Eurorack-patchtrainer en interactieve Web Audio-simulator. De **actuele kabelverbindingen** bepalen nu de audioroute: BIA/VCO → VCF → VCA → Output Mixer. GATE, envelope en sequencer-CV sturen de bijbehorende gesimuleerde functies. De vier patches bevatten hardware-instructies. Patches worden lokaal opgeslagen.

## Starten

In deze map: `python3 -m http.server 8080` en bezoek `http://localhost:8080`. Voor Android: host de hele map via HTTPS, open in Chrome en kies *App installeren*. Voor een echte APK is een afzonderlijke Android-build (bijvoorbeeld Capacitor + Android Studio) nodig; **dit ZIP-bestand is geen APK**.

## Testen

1. Laad Industrial Kick en start audio: hoor de kick.
2. Verwijder BIA AUDIO → MIX IN1: geen geluid meer na het uitklinken.
3. Herstel de kabel: geluid keert terug.
4. Laad Acid Bass: SQ-1 CV verandert de toonhoogte per stap en SQ-1 GATE stuurt ENV → VCA.
5. Verwijder ENV → VCA CV: de VCA wordt stil.
6. Probeer een AUDIO OUT op een GATE IN: verbinding wordt geweigerd.

## Grenzen en veiligheid

Dit is een **functionele, beperkte** Web Audio-modulaire engine, geen accurate BIA-, LXR-, Behringer- of SQ-1-emulatie. Alleen expliciet ondersteunde routes zijn hoorbaar. Geen realtime externe MIDI/CV, geen volledige polyfone patchmatrix, geen reverb/delay-rumble, geen native APK. Hardware-patchbeschrijvingen zijn startpunten: controleer altijd de daadwerkelijke jacknamen en signaalniveaus. Begin met laag monitorvolume en sluit Eurorack-audio niet zonder geschikte interface/attenuatie direct op consumentenapparatuur aan.
