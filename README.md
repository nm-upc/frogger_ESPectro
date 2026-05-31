# 🐸 Frogger

Implementación del clásico Flappy Bird para la consola portátil ESPectro (ESP32-S3).

Parte del proyecto ESPectro — [base_espectro](https://github.com/bf-upc/base_espectro)
## 📖 Descripció

Aquesta plantilla proporciona una base completa per desenvolupar videojocs per a la consola **ESPectro**, basada en un **ESP32-S3** amb pantalla TFT, joystick, botons físics, àudio I2S, sistema de rècords persistents, dashboard web i actualització OTA mitjançant Game Loader.

Inclou tota la infraestructura necessària perquè el desenvolupador només hagi d'implementar la lògica del joc.

---

# ✨ Característiques

- Pantalla TFT 320×480 amb LovyanGFX
- Joystick analògic i botons físics
- Àudio digital via I2S
- Splash screen d'inici
- Sistema de rècords persistents (NVS)
- Historial de partides
- Dashboard web integrat
- Actualització OTA mitjançant fitxers `.bin`
- Punt d'accés WiFi automàtic
- Suport MCP (Model Context Protocol)
- Multitasca amb FreeRTOS

---

# 🕹 Controls

| Control | Funció |
|----------|---------|
| Joystick | Moviment |
| Botó A | Acció principal |
| Botó B | Sortir / Game Loader |

---

# 📺 Maquinari Utilitzat

## Pantalla

- Controlador: ILI9488
- Resolució: 320×480
- Biblioteca: LovyanGFX

## Entrades

| Senyal | Pin |
|----------|------|
| JOY_X | GPIO 5 |
| JOY_Y | GPIO 4 |
| JOY_SW | GPIO 42 |
| BTN_A | GPIO 40 |
| BTN_B | GPIO 41 |

## Àudio

Sistema I2S amb amplificador extern.

| Senyal | Pin |
|----------|------|
| BCLK | GPIO 8 |
| LRCLK | GPIO 16 |
| DIN | GPIO 18 |

Freqüència de mostreig:

```cpp
44100 Hz
