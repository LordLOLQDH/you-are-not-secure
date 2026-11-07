# YOU ARE NOT SECURE.

Eine verständliche Website zum Thema Datenschutz. Sie zeigt, welche Informationen ein Browser bei einem normalen Website-Besuch preisgeben kann und was sich nach einer Anmeldung ändern kann.

## Funktionen

- Live-Bericht mit Browser-, Geräte-, Sprach-, Zeit- und Bildschirmdaten.
- Live-Anzeige des Online-/Offline-Status.
- Optionale IPv4-Überwachung mit erneuter Prüfung alle 30 Sekunden. Der externe Dienst api4.ipify.org erhält dabei die öffentliche IP-Adresse.
- Anzeige ausgewählter Browser-Berechtigungen, ohne Kamera, Mikrofon oder Standortzugriff anzufordern.
- Verständliche Erklärungen zu Anmeldungen und „Mit Google anmelden“, einschließlich zusätzlicher Berechtigungen für Kontakte, Drive oder Kalender.
- Lokaler URL-Analysator. Er besucht die eingegebene Website nicht.
- Simulator für Daten, die ein Registrierungsformular abfragt. Keine echten persönlichen Daten eingeben.
- Responsive Darstellung und helle Oberfläche.

## Starten

Die Datei `index.html` im Browser öffnen oder GitHub Pages für den Branch `main` und das Repository-Verzeichnis aktivieren.

## Datenschutz und Grenzen

Der Browser-Bericht wird lokal im Browser erstellt. Die Website lädt ihn nicht auf einen eigenen Server hoch. Für die optionale IPv4-Überwachung wird der externe Dienst `api4.ipify.org` kontaktiert. Dieser Dienst sieht dadurch die öffentliche IP-Adresse des Besuchers. Die Abfrage startet erst nach einem Klick und kann danach angehalten werden.

Die Online-/Offline-Anzeige basiert auf `navigator.onLine` und den Browser-Ereignissen `online` und `offline`. Das zeigt den vom Browser gemeldeten Verbindungsstatus, garantiert aber nicht, dass eine bestimmte Website erreichbar ist.

Eine normale Website kann nicht einfach Passwörter, private Dateien, Nachrichten oder Kontakte auslesen. Google-Anmeldungen geben nicht automatisch Zugriff auf das gesamte Google-Konto. Zusätzliche Daten wie Kontakte, Kalender oder Drive-Dateien erfordern gesonderte Berechtigungen, die vor der Freigabe geprüft werden sollten.

Der URL-Analysator zerlegt nur den eingegebenen Text lokal. Er scannt keine fremden Server. Eine echte Website-Prüfung benötigt einen abgesicherten Backend-Dienst mit Schutz vor SSRF, Zugriff auf interne IP-Bereiche, gefährlichen Weiterleitungen, übergroßen Antworten und Missbrauch. Zugangsdaten dürfen niemals gesammelt oder Zugriffskontrollen umgangen werden.
