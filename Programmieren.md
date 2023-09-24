<h1>Den ESP32 programmieren</h1>

Der ESP32 kann grundsätzlich in einer Vielzahl verschiedenster Programmiersprachen programmiert werden. Dieses Repository beschäftigt sich hauptsächlich mit der C-Programmierung, da diese am häufigsten beim ESP32 in Frage kommt. <br>
<br>
Der grundsätzliche Codeaufbau sieht folgender Maßen aus:
```
//globale Definitionen

int main(){
  //Statements
}
```
Das Hauptprogramm findet sich unter dem Abschnitt "**main()**" wieder. Darüber stehen sogenannte "**globale Definitonen**". In diesem Bereich können **globale**
Variablen definiert werden. 


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
