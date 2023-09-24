<h1>Den ESP32 programmieren</h1>

Anbei ein kleines Code-Beispiel für ein einfaches Blinklicht:
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
