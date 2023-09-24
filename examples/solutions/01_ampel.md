<h1>Beispiel 01:&emsp;Ampel (Lösung)</h1>

<h2>Szenario</h2>
<img style="width:300px;"src="https://github.com/voeweb/ESP32/assets/145892303/fb1cc128-87f9-4329-95b2-2381d1de53ad"></img>


<h2>Programmcode</h2>

```
//Ampel ESP32 (2023-09-24)

int red = 21;
int yellow = 4;
int green = 15;

void setup() {
  pinMode(red, OUTPUT);
  pinMode(yellow, OUTPUT);
  pinMode(green, OUTPUT);
}

void loop() {
  digitalWrite(red, HIGH);
  delay(2000);
  digitalWrite(yellow, HIGH);
  delay(1000);
  digitalWrite(red, LOW);
  digitalWrite(yellow, LOW);
  digitalWrite(green, HIGH);
  delay(2500);
  for(int i=0;i<=4;i++){
    digitalWrite(green, HIGH);
    delay(500);
    digitalWrite(green, LOW);
    delay(500);
  }
  digitalWrite(yellow, HIGH);
  delay(1000);
  digitalWrite(yellow, LOW);
}
```

<h2>Wokwi</h2>
<ul>
  <li>
    <a href="https://wokwi.com/projects/376768177794329601">https://wokwi.com/projects/376768177794329601</a>
  </li>
</ul>
