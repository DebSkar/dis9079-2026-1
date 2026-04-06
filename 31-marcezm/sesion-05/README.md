# sesion-05

lunes 06 abril 2026

## avance solemne 1

para actualizar/resetear el arduino, en la parte de arriba entro al tools y ahi a firmware update

recordar instalar adafruit que es lo que usaremos para la solemne

con mi user de github y luego un guion 

### codigo para enviar datos

#include <WiFiS3.h>
#include "AdafruitIO_WiFi.h"

#define WIFI_SSID "si"
#define WIFI_PASS "mailo6192"

#define IO_USERNAME  "udpmontoyamoraga"
#define IO_KEY       "aio_oMzo060dhHDsYpOqmbEbDEbp5hgz"

AdafruitIO_WiFi io(IO_USERNAME, IO_KEY, WIFI_SSID, WIFI_PASS);
AdafruitIO_Feed *brillo = io.feed("nicolasvaldesgreve-potenciometro");

int potPin = A0;

void setup() {
  Serial.begin(9600);
  io.connect();

  while(io.status() < AIO_CONNECTED) {
    delay(500);
  }
}

void loop() {
  io.run();

  int valor = analogRead(potPin);
  int valorMap = map(valor, 0, 1023, 0, 100);

  brillo->save(valorMap);

  

  delay(1000);
}
