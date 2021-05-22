# ArduinoButtonLED
### Wiring

![header image](https://github.com/KKKirilov/ArduinoButtonLED/blob/master/IMG_20200717_205238.jpg)
### Update on the wiring
![header image](https://github.com/KKKirilov/ArduinoButtonLED/blob/master/IMG_20200903_173809.jpg)

### Code

```
const int ledPin = 10;
const int buttonPin = 7;
int buttonState = 0; 

void setup() {

  Serial.begin(9600);
  pinMode(ledPin, OUTPUT);
  pinMode(buttonPin, INPUT);
}

void loop() {

  buttonState = digitalRead(buttonPin);

  if (buttonState == HIGH) { 
    digitalWrite(ledPin, HIGH);  
    Serial.println("LED ON +++++++"); 
  }
  else {
    digitalWrite(ledPin, LOW);
    Serial.println("LED OFF -------");
  }

}
```
