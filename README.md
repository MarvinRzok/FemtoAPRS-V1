
# Smallest Lora-APRS tracker available in the world
<img src="./IMG_78267.jpg" width="1000"> 

Femto-APRS ist das kleinste und leichteste Lora-APRS Board auf dem Markt.
Ein 2m-APRS Sender in der selben Größe ist geplant, allerdings ist die Verfügbarkeit von 70 cm LoRa-APRS in Deutschland um einiges besser.
Geräte um Lora APRS zu empfangen sind außerdem weiter verbreitet und viel günstiger.

## Was kann das Board?

Das Board sendet in einem vorher programmierten Intervall APRS Nachrichten aus.
Diese bestehen aus dem Rufzeichen, Koordinaten, Höhe, Temperatur, Luftdruck und einer eigenen eingestellt Nachricht.
Die Aussendungen werden entweder von der eigenen Empfangsstation oder von öffentlichen Empfangsstationen empfangen und auf aprs.fi hochgeladen.
Das eigene Gerät ist dann auf dieser Website zum verfolgen sichtbar.

## Was ist alles auf der Platine verbaut?

- Arduino (ATMEGA328PB)
- GPS
- RFM98W Sendemodul 
- Neopixel RGB LEDs
-BMP280/BME280 Temperatur/Luftdruck Sensor
- Spannungsteilerzur spannungsmessung (in der Testphase)
- diverse Kleinigkeiten

## Technische Informationen
Programmiert wird das Board über den Stecker auf der Vorderseite, auf den ein Adapter für ein USB FTDI Board gesteckt wird. Es ist ein reines 3,3 Volt Board!
Die Stromaufnahme beträgt weniger als 50mA, bei einer 10mW Aussendung unter 100mA.
Die maximale Sendeleistung beträgt 100 mW, für Ballonflüge reichen 10mW im Regelfall aus. 
Mit 10mW habe ich aus dem 9. Stockwerk (Hochhaus) mehrere I-gates in über 100Km Entfernung erreicht.
Ich weiß nicht was die Community mit den Boards vorhat, aber das sollte reichen :-)

## Wie wird das Bort programmiert?

Programmiert wird das Board über die Arduino IDE. Wenn ihr schon einmal einen Arduino programmiert habt oder euch damit auseinandergesetzt habt,
sollte das ganze kein Problem darstellen. Auch für Anfänger ist die Einrichtung sehr simpel.

1. Arduino IDE installieren 
2. Minicore Boards Extension installieren
3. ATMEGA328PB (8MHz inernal) (2,7V BOD) auswählen.
4. Arduino Code öffnen und in den ersten Zeilen des Programmcodes eigenes Rufzeichen und eigene Statusnachricht eintragen.
5. Code hochladen und testen.

<img src="./B1.png" width="400">
