# Tasmota Basissetup

Basis-Setup nach der Erstinstallation von Tasmota

### Wifi einrichten

* Gerät anschließen, nach dem WLAN (tasmota-XXXX) suchen und verbinden
* 4-stellige Kennung (XXXX) merken
* http://192.168.4.1/ öffnen
* WLAN SSID und Passwort vergeben

### Gerät einrichten

* http://tasmota-XXXX/ eingeben (wenn die Kennung nicht mehr bekannt ist, im Router nachschauen, welchen Namen oder welche IP das Gerät hat
* Einstellungen -> Sonstige Konfiguration -> Vorlage
    * Gerätespezifische Vorlage einstellen
    * Häkchen bei "aktivieren" setzen
* Das Wifi-Hostname-Template lässt sich nicht ändern (https://github.com/arendst/Tasmota/issues/142) und besteht immer aus MQTT-Topic + DeviceID. Workaround: Topic generisch lassen, Device-ID in "Full Topic" eintragen
* Einstellungen -> MQTT-Settings
    * Host, Port, Benutzer, Passwort des MQTT-Servers
    * Client: GERÄTETYP-XXXX (z.B. steckdose-1234)
    * Topic: GERÄTETYP (z.B. steckdose)
    * Full Topic: %topic%-XXXX/%prefix%/
* ggf. weitere Einstellungen über die Konsole-> https://tasmota.github.io/docs/#/Commands
