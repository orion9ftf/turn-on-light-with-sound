


```c++
int luz = 12;
int sensorSonido = 2;
int sonido = 0;
int var = 0;

void setup() {
  Serial.begin(9600);
  pinMode(sensorSonido, INPUT);
  pinMode(luz, OUTPUT);
}

void loop() {
  var  = digitalRead (sensorSonido);
  if (var == HIGH) {
    Serial.println ("encendido");
    digitalWrite (luz, HIGH) ;
    sonido = sonido+1;
    delay (90);
  }

  if (sonido == 2) {
    Serial.println ("apagado");
    digitalWrite (Luz, LOW);
    sonido = 0;
  }
}
```
