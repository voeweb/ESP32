<h1>Den ESP32 programmieren</h1>

Der ESP32 kann grundsätzlich in einer Vielzahl verschiedenster Programmiersprachen programmiert werden. Dieses Repository beschäftigt sich hauptsächlich mit der C-Programmierung, da diese am häufigsten beim ESP32 in Frage kommt.

<h2>Code-Aufbau</h2>
Der grundsätzliche Codeaufbau sieht folgender Maßen aus:

```
//globale Definitionen

void setup(){
  //Statements
}

int loop(){
  //Statements
}
```
Das Programm beginnt mit dem Abschnitt "**setup**". Hier werden Instruktionen eingefügt, die zu Beginn ausgeführt werden sollen. Nachdem der setup-Abschnitt abgearbeitet wurde, geht es hinein den "**loop**". Statements innerhalb des Loops werden in einer Endlosschleife wiederholt. Im oberen Bereich gibt es sogenannte "**globale Definitonen**". In diesem Bereich können **globale** Variablen definiert werden. 

<h2>Basis-Befehle</h2>

<table>
  <tr>
    <th>Funktion</th>
    <th>Syntax</th>
    <th>Beispiel</th>
  </tr>
  <tr>
    <td>Initialisieren einer Variable</td>
    <td>DATENTYP+VARIABLENNAME;</td>
    <td>int variable;</td>
  </tr>
  <tr>
    <td>Einer Variable einen Wert zuweisen</td>
    <td>VARIABLE+"="+WERT;</td>
    <td>variable = 3;</td>
  </tr>
  <tr>
    <td>Definieren einer Variable</td>
    <td>DATENTYP+VARIABLENNAME+"="+WERT;</td>
    <td>int variable = 3;</td>
  </tr>
  <tr>
    <td>Einen Pin als Eingang bzw. Ausgang definieren</td>
    <td>pinMode(PIN,INPUT/OUTPUT);</td>
    <td>pinMode(3,OUTPUT);</td>
  </tr>
  <tr>
    <td>Einen Digital-Pin auf "HIGH" bzw. "LOW" schalten</td>
    <td>digitalWrite(PIN,HIGH/LOW);</td>
    <td>digitalWrite(3,HIGH);</td>
  </tr>
  <tr>
    <td>Einen Digital-Pin auslesen</td>
    <td>digitalRead(PIN);</td>
    <td>variable = digitalRead(3);</td>
  <tr>
    <td>Timeout / "Delay"</td>
    <td>delay(VERZÖGERUNG[ms]);</td>
    <td>delay(1000);</td>
  </tr>
  <tr>
    <td>Einzeiliges Kommentar</td>
    <td>//KOMMENTAR</td>
    <td>//Pin schalten</td>
  </tr>
  <tr>
    <td>Mehrzeiliges Kommentar</td>
    <td>
      /* KOMM- <br>
         ENTAR */
    </td>
    <td>
      /* Blinklicht <br>
         Ver.1.00   */
    </td>
  </tr>
</table>

<h2>Beispielcode</h2>
Zur besseren Vorstellung ein kleines Code-Beispiel für ein einfaches Blinklicht:

```
//BLINKLICHT
int pin = 12;

void setup(){
  pinMode(pin,OUTPUT);
}

void loop(){
  digialWrite(pin,HIGH);
  delay(1000);
  digialWrite(pin,LOW);
  delay(1000);
}
```
Um diesen Code besser zu verstehen, probiere dich doch an folgendem Beispiel:
<a href="examples/01_ampel.md">LINK</a>
