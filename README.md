# 🐸 Frogger

Implementación del clásico Flappy Bird para la consola portátil ESPectro (ESP32-S3).

Parte del proyecto ESPectro — [base_espectro](https://github.com/bf-upc/base_espectro)
## Descripción

Ayuda a la rana a cruzar la carretera y el río para llegar a la zona segura superior.

Deberás evitar los vehículos de la carretera y utilizar los troncos flotantes para cruzar el agua sin caer.

Cada vez que alcanzas la meta consigues un punto y vuelves a empezar desde la posición inicial.

La partida termina cuando pierdes todas las vidas.

---

## Controles

| Control | Acción |
|----------|----------|
| Joystick eje X | Mover izquierda/derecha |
| Joystick eje Y | Mover arriba/abajo |
| Botón A | Realizar movimiento |
| Botón B | Abrir Game Loader / salir de la partida |

---

## Sistema de juego

- Empiezas con **3 vidas**.
- Debes alcanzar la fila superior para sumar puntos.
- Los coches eliminan una vida al colisionar contigo.
- Caer al agua sin estar sobre un tronco también elimina una vida.
- Tras perder una vida, la rana vuelve a la posición inicial.
- La partida termina al perder las 3 vidas.

---

## Puntuación

- +1 punto por cada vez que alcanzas la meta.
- El récord se guarda automáticamente en la memoria flash (NVS).
- El historial de las últimas 20 partidas es visible desde el dashboard.
- Las estadísticas permanecen almacenadas incluso después de apagar la consola.

---

## Dashboard

Con la consola encendida, conéctate a la red WiFi **ESPectro** (contraseña: **gameloader**) y abre:

http://192.168.4.1

Desde el dashboard podrás:

- Consultar récords.
- Ver estadísticas de las partidas.
- Revisar el historial de puntuaciones.
- Instalar nuevas versiones del juego mediante OTA.
- Gestionar todos los juegos instalados en la consola.

---

## Compilar y flashear

```bash
git clone https://github.com/bf-upc/base_espectro

cd base_espectro

pio run --target upload
```

---

## Requisitos

- PlatformIO
- Librería `lovyan03/LovyanGFX @ ^1.1.12`
- ESP32-S3 (RYMCU ESP32-S3 DevKitC-1)

---

## Binario compilado

El firmware generado se encuentra en:

```text
.pio/build/rymcu-esp32-s3-devkitc-1/firmware.bin
```

Este archivo puede cargarse directamente desde el Game Loader sin necesidad de conectar la consola por USB.

---

## Características técnicas

- Pantalla TFT ILI9488 320×480
- Control mediante joystick analógico
- Sistema de audio I2S para efectos sonoros
- Guardado persistente de récords mediante NVS
- Dashboard web integrado
- Actualización OTA mediante Game Loader
- WiFi Access Point integrado (ESPectro)
- Gestión automática de historial de partidas
- Soporte FreeRTOS para tareas en segundo plano

---

## Escenario de juego

| Zona | Descripción |
|--------|-------------|
| Meta | Zona segura superior |
| Río | Debes utilizar los troncos para cruzarlo |
| Zona segura | Descanso entre obstáculos |
| Carretera | Evita los vehículos |
| Inicio | Posición inicial de la rana |

---

## Autores

**Noel Medina**  
**Bernat Figuerola**

UPC · 2026
