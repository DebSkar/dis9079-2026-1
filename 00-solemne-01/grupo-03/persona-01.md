# persona-01

- antokiaraa

investigaciones individuales

## sobre adafruit i/o

Instalación y configuración:

Paso 1: en Arduino IDE busqué la biblioteca Adafruit IO Arduino y la instalé junto con sus dependencias

![instalar biblioteca](./imagenes/biblioteca_adafruit.png)

Paso 2: descargué el código subido en la carpeta de mi grupo "enviarGrupo03" y su .h

Paso 3: me creé una cuenta en <https://io.adafruit.com/> con mi correo UDP y desde ahí copié mi username y la active key

Paso 4: en el código de arduino modifiqué las líneas donde debe ir el username, la active key, mi WiFi y la contraseña, verificando que el arduino esté conectado mandé el código

Error 1: compiló pero en el serial monitor me daba un cáracter raro, lo busqué y encontré [en esta página](https://forum.arduino.cc/t/solucionado-ayuda-monitor-serial-con-caracteres-ilegibles/473044/5) que el número del serial begin debe coincidir con la cantidad de baudios (bits por segundo) en el serial monitor

![error por baudios](./imagenes/error1_baud.png)

Aquí lo edité: 

![baudios solucionado](./imagenes/solucionado_baud.png)

## sobre artista, diseñadora o producto que usa electrónica o computación inalámbricas
