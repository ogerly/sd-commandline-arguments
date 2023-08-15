## Stable Diffusion Commandline Argumente für webui-user.sh & webui-user.bat

1. Öffne die Datei
```
	Linux: /webui-user.sh
	Windows:  /webui-user.bat
```
im Hauptverzeichnis in einem Editor deiner Wahl.

2. Passe **Zeile 13** an:

   Achte darauf das du immer **EINEN** _SPACE_ zwischen den einzelnen Befehlen hast, nicht mehr und nicht weniger!
   ![image](https://github.com/ogerly/sd-commandline-arguments/assets/1324583/07bebc57-e9b5-44f4-974d-6f9baac91dc1)



## Commandline Argumente

**--api-port**  
- Setzt einen benutzerdefinierten Port für die API
- Standard ist 7860

**--ckpt**
- Definiert Pfad zur Checkpoint Datei des Modells 
- Muss gesetzt werden um eigene Modelle zu laden

**--cpu**  
- Zwingt Stable Diffusion CPU statt GPU zu nutzen
- Sehr viel langsamer aber ermöglicht Ausführung ohne GPU

**--debug**
- Schaltet Debugging-Logs an
- Nützlich bei Problembehebung, erzeugt aber viel Output

**--debug-layers**
- Zeigt Layer Outputs in Browser an für Debugging
- Erhöht Speicher- und Performance-Verbrauch deutlich 

**--disable-legacy-checkpoint-detection**
- Deaktiviert Abwärtskompatibilität für alte Checkpoints
- Kann Probleme mit sehr alten Modellen verhindern

**--disable-safe-unpickle** 
- Deaktiviert Sicherheitsmaßnahmen beim Laden von Modellen
- Wird benötigt, um eigene Modelle zu laden
- Ansonsten nicht empfohlen für erhöhte Sicherheit

**--enable-insecure-content**
- Erlaubt das Laden von Inhalten über HTTP statt HTTPS
- Reduziert Sicherheit, kann aber für Entwicklung nützlich sein

**--enable-insecure-extension-access**
- Erlaubt den Zugriff auf unsichere Browser-Erweiterungen
- Wird gebraucht für bestimmte Extensions
- Erhöht aber Sicherheitsrisiken

**--enable-insecure-websockets**
- Erlaubt unsichere Websockets Verbindungen
- Wird für manche Setups benötigt, erhöht aber Risiken

**--headless**
- Startet die Anwendung im Headless-Modus
- Für Server-Setups ohne graphische Oberfläche

**--hide-model-details**
- Blendet Details zum geladenen Modell aus
- Kann sinnvoll sein zum Schutz von IPs

**--hide-model-options**
- Blendet Optionen zum Modell aus dem UI aus
- Kann sinnvoll sein, um Nutzern nur bestimmte Funktionen zu erlauben

**--hide-model-source**
- Blendet Herkunft/Quelle des Models aus
- In Kombination mit --hide-model-details für Anonymität

**--image-inference-speed**
- Testet und gibt die Inferenz-Geschwindigkeit aus
- Nützlich zum Messen der Performance

**--insecure-webdriver-download**
- Erlaubt unsicheres Herunterladen über WebDriver
- Wird von manchen Browser-Automationstools benötigt

**--listen**
- Definiert auf welchem Port der lokale Server laufen soll, standardmäßig 7888

**--locale**
- Setzt Locale, z.B. '--locale de' für Deutsch
- Ändert Sprache der Weboberfläche 

**--lock-weights**
- Verhindert Veränderung der Modell-Gewichte während Inferencing
- Kann Genauigkeit leicht verbessern

**--lowram** 
- Alternative zu --lowvram für Systeme mit wenig Arbeitsspeicher
- Verringert aber auch Qualität

**--lowvram**
- Reduziert den VRAM Verbrauch weiter  
- Verringert Qualität noch mehr als --medvram
- Für Systeme mit sehr wenig VRAM

**--medvram**  
- Verwendet nur 6GB VRAM für niedrigere Grafikkarten
- Sollte bei Karten mit wenig VRAM genutzt werden
- Reduziert aber auch Qualität der Generierungen

**--no-auto-open-browser**
- Deaktiviert automatisches Browser-Öffnen
- Nützlich wenn WebUI im Hintergrund laufen soll

**--no-clipboard**
- Deaktiviert Zugriff auf die Zwischenablage
- Verhindert potenziellen Missbrauch

**--no-gradients**
- Deaktiviert Anzeige von Hypernetworks  
- Kann bei langsamen Systemen Rendering beschleunigen
- Reduziert aber Möglichkeiten für künstlerische Kontrolle

**--no-half**
- Deaktiviert Halbauflösung für schnelleres Rendern
- Erhöht Qualität der Generierungen
- Sollte verwendet werden, wenn genug Rechenleistung vorhanden ist

**--no-jpeg**
- Deaktiviert JPG Format für generierte Bilder
- PNGs werden stattdessen verwendet

**--no-overflow-check**
- Deaktiviert Überlaufüberprüfung
- Kann bei manchen Modellen Out-of-Memory verhindern   

**--no-png**
- Deaktiviert PNG Format für generierte Bilder
- Reduziert CPU Verbrauch etwas
- JPGs werden stattdessen verwendet

**--no-statusbar** 
- Blendet den Statusbalken am unteren Rand aus
- Hilfreich für cleanere Screenshots

**--precision full**
- Wie --no-half für volle Präzision  
- Erhöht Qualität der Generierungen
- Benötigt mehr Rechenleistung

**--quiet**
- Unterdrückt informative Output-Meldungen 
- Nützlich für automatisierte Abläufe

**--reinstall**
- Setzt Installation und Cache zurück
- Sollte genutzt werden, wenn Probleme auftreten

**--reinstall-extensions**
- Setzt die Extensions/Plugins auf Default zurück
- Hilfreich wenn Probleme mit Extensions auftreten

**--reload-extensions**  
- Lädt Erweiterungen neu ohne kompletten Neustart
- Beschleunigt Testing von Extensions

**--sampler-name**
- Ermöglicht die Wahl des Samplers, z.B. DPM++
- Kann Qualität von Generierungen beeinflussen
- Standard ist K_LMS

**--seed**  
- Setzt den Seed für generative Zufälligkeit 
- Ermöglicht Reproduktion der selben Bilder
- Kann für Konsistenz und Debugging hilfreich sein

**--share**
- Erlaubt das Teilen der generierten Bilder mit anderen

**--shards**
- Ermöglicht verteiltes Inferencing auf mehreren GPUs
- Beschleunigt Generierung aber erfordert Mehr-GPU-Setup

**--skip-torch-cuda-test** 
- Überspringt CUDA Verfügbarkeitsüberprüfung
- Kann bei fehlerhafter Erkennung helfen

**--theme** 
- Ermöglicht das Setzen eines Dark/Light Themes
- Zum Beispiel '--theme dark'

**--trim-models**
- Lädt Modelle mit minimalen Metadaten
- Reduziert Speicherverbrauch, Features können fehlen

**--ttl**  
- Setzt Time-to-Live für das WebUI in Sekunden
- Nach Ablauf wird das WebUI automatisch geschlossen

**--web-tmp-directory**
- Erlaubt Setzen eines custom Web Temporary Verzeichnisses
- Kann helfen wenn Standardverzeichnis voll ist  

**--xformers**
- NVIDIA Only
- Leistung Steigerung
- VRAM Optimierung

formers ist Crosslayer Optimier und sollte immer benutzt werden, da es den Prozess schneller macht und VRAM Optimaler ausnutzt, wo durch du Effektive größer Bilder machen kannst (mehr VRAM im Prozess zu verfügung hast) 
