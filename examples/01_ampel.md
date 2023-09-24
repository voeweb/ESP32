<h1>Beispiel 01:&emsp;Ampel</h1>

Besuche die Webseite <a href="https://wokwi.com/projects/new/esp32">Wokwi.com</a> und erstelle dort ein neues Projekt für den ESP32. 
Du kennst Ampelregelungen aus dem täglichen Straßenverkehr. Ziel dieser Übung soll nun sein, selbst eine Ampelsteuerung zu programmieren. 

Für die Projektumsetzung brauchen wir folgende Komponenten:
<ol>
  <li>ESP32</li>
  <li>LED rot</li>
  <li>LED gelb</li>
  <li>LED grün</li>
</ol>

Bei unserer Ampel unterscheiden wir zwischen folgenden Ampelphasen:

<table>
  <tr>
    <th>Id</th>
    <th>Zeitstempel [ms]</th>
    <th>Ampelphase</th>
  </tr>
  <tr>
    <td>0</td>
    <td>0</td>
    <td>ROT</td>
  </tr>
  <tr>
    <td>1</td>
    <td>2000</td>
    <td>ROT+GELB</td>
  </tr>
  <tr>
    <td>2</td>
    <td>3000</td>
    <td>GRÜN</td>
  </tr>
  <tr>
    <td>3</td>
    <td>6000</td>
    <td>GRÜN BLINKEN - AUS</td>
  </tr>
  <tr>
    <td>4</td>
    <td>6500</td>
    <td>GRÜN BLINKEN - EIN</td>
  </tr>
  <tr>
    <td>3</td>
    <td>6000</td>
    <td>GRÜN BLINKEN - AUS</td>
  </tr>
  <tr>
    <td>4</td>
    <td>6500</td>
    <td>GRÜN BLINKEN - EIN</td>
  </tr>
  <tr>
    <td>5</td>
    <td>7000</td>
    <td>GRÜN BLINKEN - AUS</td>
  </tr>
  <tr>
    <td>6</td>
    <td>7500</td>
    <td>GRÜN BLINKEN - EIN</td>
  </tr>
  <tr>
    <td>7</td>
    <td>8000</td>
    <td>GRÜN BLINKEN - AUS</td>
  </tr>
  <tr>
    <td>8</td>
    <td>8500</td>
    <td>GRÜN BLINKEN - EIN</td>
  </tr>
  <tr>
    <td>9</td>
    <td>9000</td>
    <td>GELB</td>
  </tr>
  <tr>
    <td>10</td>
    <td>10000</td>
    <td>ROT</td>
  </tr>
</table>
<br>
Zur Hilfe kannst du gerne folgende <a href="./Programming.md">Seite</a>benutzen.
