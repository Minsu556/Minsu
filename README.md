#include "DHT.h"

#define DHTPIN 27

#define DHTTYPE DHT11

DHT dht(DHTPIN, DHTTYPE);

void setup() {

Serial.begin(115200);

dht.begin();

}

void loop() {

delay(2000);  

float h = dht.readHumidity();

float t = dht.readTemperature();

Serial.print("My Name Is Minsu\n");

Serial.print(F("Humidity: "));

Serial.print(h);

Serial.print(F("% Temperature: "));

Serial.print(t);

Serial.println(F("°C "));

}
