# Dispensador Eléctrico - Sistemas Embebidos
## Luciano Savia y Bautista Moyano 6ºB

## Descripción del proyecto:

Es un sistema automático para la entrada de un establecimiento,
pensado para controlar el ingreso de personas y mantener la
higiene de manos. Funciona con una Raspberry Pi 4 que integra un
sensor de temperatura (GY-906), un sensor de proximidad 
(KY-032), una bomba de alcohol en gel accionada por un relé y
un monitor.

Cuando una persona acerca la muñeca, el sensor mide su
temperatura. Si el valor es menor a 37,5 °C, la
pantalla indica que puede ingresar. Si lo supera, indica que no
debe ingresar. Luego, cuando una persona acerca su mano al
dispensador de alcohol, el sensor de proximidad detecta la
mano y activa la bomba durante 1 segundo para dispensar alcohol
en gel.

Cada medición se guarda con fecha y hora, y se publica por MQTT,
para que un administrador pueda consultar los registros. Un
botón de emergencia corta la energía de la bomba por hardware,
sin depender del programa, y funciona incluso si el software
falla.

## Diagrama de bloques:
https://docs.google.com/drawings/d/1smf9OPjXyx_oO2xn_KdZvXEATnLpUi2ibBFbgCH5BaE/edit?usp=sharing

## Manual de Usuario:
https://docs.google.com/document/d/1sG95uO5_PX8IHS57GVqyP3_S4SRparlDSrSrrIaK6Io/edit?usp=sharing