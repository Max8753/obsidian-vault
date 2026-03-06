XML = eXtensible Markup Language (HTML = HyperText Markup Language)

#### Details:
- W3C hat diese Sprache in 1998 freigegeben
- Offizielle Doku: https://www.w3.org/TR/rdf12-xml/

Vorteile:
- Über ein sogenanntes XMLSD XML Schema Definition einigen sich zwei oder mehrere Partner, wie die XML Dateien genau formatiert sein soll.
	- Beispiel: Zentralbank (EZB) und regionale Banken wie die Sparkasse definieren ein Schema und jede XML Datei wird mit diesem Schema validiert. = Rechtssicherheit.
- ISO Standard 20022 Weltweiter Standard für Übermittlung von Finanzdaten (Überweisungen)

Beispiel:
``` 
<?xml version="1.0" encoding="UTF-8"?>

  

<!-- Die Tags zusammen bilden ein Element. In unserem Fall der Container -->

<benutzerliste> <!-- Opening Tag-->

    <benutzer id="101">

        <vorname>Harry</vorname>

        <nachname>Potter</nachname>

        <email>harry@hogwarts.com</email>

        <status>Aktiver Schüler</status>

    </benutzer>

</benutzerliste> <!-- Closing Tag-->
```