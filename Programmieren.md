<h1>Den ESP32 programmieren</h1>

Der ESP32 kann grundsätzlich in einer Vielzahl verschiedenster Programmiersprachen programmiert werden. Dieses Repository beschäftigt sich hauptsächlich mit der C-Programmierung, da diese am häufigsten beim ESP32 in Frage kommt.

<h2>Code-Aufbau</h2>
Der grundsätzliche Codeaufbau sieht folgender Maßen aus:

```
//globale Definitionen

int main(){
  //Statements
}
```
Das Hauptprogramm findet sich unter dem Abschnitt "**main()**" wieder. Darüber stehen sogenannte "**globale Definitonen**". In diesem Bereich können **globale**
Variablen definiert werden. 

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
    <td>Einen Pin auf "HIGH" bzw. "LOW" schalten</td>
    <td>digitalWrite(PIN,HIGH/LOW);</td>
    <td>digitalWrite(3,HIGH);</td>
  </tr>
  <tr>
    <td>Timeout / Delay</td>
    <td>delay(VERZÖGERUNG[ms]);</td>
    <td>delay(1000);</td>
  </tr>
</table>

<h2>Beispielcode</h2>
Zur besseren Vorstellung ein kleines Code-Beispiel für ein einfaches Blinklicht:

```
//BLINKLICHT
int pin = 12;

int main(){
  pinMode(pin,OUTPUT);
  while(true){
    digialWrite(pin,HIGH);
    delay(1000);
    digialWrite(pin,LOW);
    delay(1000);
  }
}
```
