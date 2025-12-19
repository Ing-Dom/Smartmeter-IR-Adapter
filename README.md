# Smartmeter-IR-Adapter
IR Schreib-Lesekopf für D0 / SML UART / TTL 3.3 - 5V

## Beschreibung der Hardware
Beim Ing-Dom Smartmeter-IR-Adapter handelt es sich um einen bi-direktionalen Umsetzer von Infratorsignalen auf 3.3V / 5V Logikpegel, vor allem um die sog. D0 oder SML Schnittstelle von Stromzählern in Deutschland zu nutzen.  
Mit TTL-Pegel UART ist der Adapter dafür gedacht an Mikrocontrollerboards wie Arduino oder Raspberry PiPico aber auch an Raspberry GPIOs abgeschlossen zu werden.  Über UART-USB Adapter kann er auch über USB an diverse Endgeräte angeschlossen werden.
Der Adapter setzt den über UART-Tx (Sendesignal) empfangenen Pegel in ein leuchten der IR-Sendediode um. Dabei wird invertiert, d.h. wenn UART-Tx HIGH ist, ist die IR-LED aus, ist das Signal LOW, leichtet die IR-LED.  
Auf der Empfangsseite wird über einen IR-Phototransistor ein von der Gegenstelle empfangene IR-Pulse umgesetzt, auch hier wird invertiert: Im Ruhezustand (kein IR Signal empfangen) wird HIGH ausgegeben, wird ein IR-Signal empfangen, wird UART-Rx LOW angesteuert.  

## Technische Daten

### Elektronische Daten
Vcc: 3.3 - 5V  
Logikpegel: wie Vcc  
max. Baudrate: 9600bit/s

### Elektro-Mechanische Daten
Anschlusskabel mit 4poligen Westernstecker 4P4C "RJ9 / RJ10 / RJ22"

Die Belegung kann grundsätzlich beim Aufbau des Bausatzes variiert werden, ist aber für folgende Belegung vorgesehen:

1: Vcc
2: Tx (Senden zum Zähler)
3: Rx (Empfangen vom Zähler)
4: Gnd

Kontakt-Nr. Stecker von vorne:


### Mechanische Daten
Größe: D=30mm, H=12mm  
Magnetische Halterung (Haltekraft abhängig vom Aufbau der Gegenseite)

## Aufbauanleitung
