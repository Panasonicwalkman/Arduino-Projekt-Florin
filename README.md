# Arduino-Projekt-Florin
Projektplan--------------------------------------------------------------------------------------------------------------------------------------------

Hühnerklappe
Es soll eine Hühnerklappe automatisiert werden. Die klappe wird über ein Seil das von einem Schrittmotor aufgewickelt wird Bewegt. Die Position wird durch sensoren erkannt. Über einen Handmodus soll die Klappe per Taster bewegt werden. Die Position der Modus und Fehler sollen mit LED,s Signalisiert werden.


Muss Kriterien:
-Schrittmotor bewegt Klappe
-Zwei Positionen werden erkannt
-Schalter für Handmodus funktioniert
-Taster für Handmodus funktioniert
-Lichtsensor für Automodus funktioniert
-LED Signalisierung funktioniert

Wunsch Kriterien:
-Wie besprochen gibt es keine Wunschkriterien

Aufgabenaufteilung-------------------------------------------------------------------------------------------------------------------------------------

Da ich dass Projrkt alneine gmacht habe müssen keine Aufgaben verteilt werden.

Beschreibbung des Lösungsansatzes----------------------------------------------------------------------------------------------------------------------

Verwendetes Material:

Generell habe ich versucht das material aus dem gelieferten Sett zu verwenden. Bis auf die Sensoren und einige verbrauchsmaterialien (Widerstände Kabel) habe ich dies auch gemacht.

-Microcontroller
Arduino UNO R3

![image](https://github.com/user-attachments/assets/6d12e702-9cd9-459d-953d-860e141284f0)

-Schrittmotor
 28BYJ-48
 
 ![Motoranschluesse](https://github.com/user-attachments/assets/2b8889b9-5922-4b87-973b-dc400074144c)

 -Treiberplatine Schrittmotor
 ULN2003
 
![Platinenanschluesse](https://github.com/user-attachments/assets/268f0aa4-8ffd-46ee-aaa8-9de1bf0a8755)

LED's

![image](https://github.com/user-attachments/assets/1ace0dfe-84a3-4789-b388-045add65c387)

Taster

![Screenshot 2025-01-03 155550](https://github.com/user-attachments/assets/dcc8cbbb-ffea-46b5-85c1-0ea80276b9ff)

Photoressistor

![Screenshot 2025-01-03 155725](https://github.com/user-attachments/assets/4587366a-98b7-4d29-8cee-7cd70cabea44)

Sensoren
mk04-1a66b-500w

![Screenshot 2025-01-03 160841](https://github.com/user-attachments/assets/d6d70d0d-95da-40cb-bfa9-f6e6d0ce7469)


Mein Ansatz:

Zu aller erst wahr es wichtig die benötigten Funktionen des Projoktes zu definieren. Da mein Projekt eine hühnerklappe für meine Eltern ist wahr es wichtig zualler erst absprache mit ihnen zu halten. 
Die grundlegende idee Wahr ein Motor einzusetzen welcher durch drehung in Uhrzeiger oder in Gegenuhrzeigersinn eine Schnur welche an der hühnerklappe befestigt ist auf und abzuwickeln. Dies soll das Öffnen und Schliessen der Hühnerklappe ermöglichen. 
Um den Motor zu Stoppen wenn die Klappe Offen oder Geschlossen ist, sollten zusätzlich Sensohren verwendet werden welche die position der Hühnerklappe detektieren. Diese Position wird jeweils mit einer Weissen LED Signalisiert. 
Die Klappe soll sich in Zwei unterschiedlichen Modis öffnen und schliessen. Standardmässig soll mittels eines Photoressistors erkannt werden ob tag oder nacht ist. Bei Tag öffnet sich die Klappe und bei Nacht schliesst sie sich so automatisch. Dies Ist der Automatikmodus, wessen aktivierung mit einer Blauen LED signalisiert wird. 
Mit einer weiteren Blauen LED wird signalisiert, dass der Handmodus aktiv ist, in welchem durch drücken eines Tasters die Position der Klappe jeweils in die andere Wechselt (offen zu geschlossen und umgekehrt). Zwischen den beiden Modi kann mit einem Weiteren Taster hin und her gewechselt werden. Falls die Klappe zbsp. abreisst und für eine zu lange zeit nicht die andere Position erreicht, wird der Motor gestoppt und die Rote LED aktiviert sich. 


Flussdiagramm------------------------------------------------------------------------------------------------------------------------------------------

![Screenshot 2025-01-03 171013](https://github.com/user-attachments/assets/527ae509-e84e-4499-9c64-cc12a40ea6ed)


Testen-------------------------------------------------------------------------------------------------------------------------------------------------
Muss
Muss Kriterien:


Schrittmotor bewegt Klappe------------------------------


Um zu testen Muss sich der Motor entweder durch Statusänderung des Photoressistors oder durch Betätigung des Positionstasters und aktivieren. Die Bewegung muss entsprechend der Logik entweder in Uhrzeigersinn oder im Gegenuhrzeigersinn erfolgen. Zusätzlich muss sich der motor nach erreichen der Zweiten Position stoppen.


Kriterien Start------------------------------


Automodus (Modus 1)------------


Drehung Uhrzeigersinn (Öffnen)--------

Modus 1 = True

Licht = Tag

Sensor Unten = True

Sensor Oben = False


Drehung Gegenuhrzeigersinn (Schliessen)--------

Modus 1 = True

Licht = Nacht

Sensor Unten = False

Sensor Oben = True


Handmodus (Modus 2)------------


Drehung Uhrzeigersinn (Öffnen)--------

Modus 2 = True

Taster Position = True

Sensor Unten = True

Sensor Oben = False


Drehung Gegenuhrzeigersinn (Schliessen)--------

Modus 2 = TrueTaster 

Position = True

Sensor Unten = False

Sensor Oben = True


Kriterien Stop------------------------------


Drehung Uhrzeigersinn (Öffnen)
Motor Status = Drehung Uhrzeigersinn
Sensor Oben = True


Drehung Gegenuhrzeigersinn (Schliessen)
Motor Status = Drehung Gegenuhrzeigersinn
Sensor Unten = True


Zwei Positionen werden erkannt------------------------------


Erreicht die Klappe die Beiden Sensohren, müssen diese die Position erkennen und das entsprechende Signal an die Steuerung weitergeben.


Schalter für Handmodus funktioniert------------------------------


Stadt wie anfang angedacht habe ich eine Taster verwendet welcher zwischen den beiden modis hihn und her wechselt. Der Taster muss bei betätigung den Modus in den jeweils anderen wechseln. 


Taster für Handmodus funktioniert------------------------------


Im Hand Modus muss der Taster für den Positionswechsel funktionieren und die Klappe öffnen und wider schliessen.


Lichtsensor für Automodus funktioniert------------------------------


Der Photoressistor muss detektiern ob Tag oder Nacht ist und das entsprechende Signal an die Steuerung weiter geben.


LED Signalisierung funktioniert------------------------------


Die entsprechenden Modi, Positionen und die Zeitüberschreitung müssen mittels LED's signalisiert werden.


Komentiertercode---------------------------------------------------------------------------------------------------------------------------------------

Videos-------------------------------------------------------------------------------------------------------------------------------------------------







Hühnerklappe
Es soll eine Hühnerklappe automatisiert werden. Die klappe wird über ein Seil das von einem Schrittmotor aufgewickelt wird Bewegt. Die Position wird durch sensoren erkannt. Über einen Handmodus soll die Klappe per Taster bewegt werden. Die Position der Modus und Fehler sollen mit LED,s Signalisiert werden.


Muss Kriterien:
-Schrittmotor bewegt Klappe
-Zwei Positionen werden erkannt
-Schalter für Handmodus funktioniert
-Taster für Handmodus funktioniert
-Lichtsensor für Automodus funktioniert
-LED Signalisierung funktioniert

Wunsch Kriterien:
-Wie besprochen gibt es keine Wunschkriterien
