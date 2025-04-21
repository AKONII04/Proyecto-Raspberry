# 💧 Proyecto Scratch: Alerta de Agua con Raspberry Pi 4 🚨

Este proyecto utiliza **Scratch** en la **Raspberry Pi 4** 🧠 junto con un **sensor de agua** 💦 y un **zumbador** 🔊 para detectar la presencia de agua y activar una alerta sonora. Ideal para aprender sobre sensores, GPIO y programación visual con bloques. 

### 🧠 AUTORES
- Iker Cupilla 
- Javi Rocha
- Ivan Palma
- Antonio Benitez
---

## 🧰 Componentes Necesarios

- 🧠 Raspberry Pi 4 (con sistema operativo Raspberry Pi OS)
- 💦 Sensor de agua (ej: YL-83 o FC-28)
- 🔊 Zumbador activo
- 🔌 Cables jumper macho-hembra
- 🔲 Protoboard (opcional)

---

## 🔌 Conexión de los Componentes
- VCC -> Pin 2 (5V) ⚡ GND -> Pin 6 (GND) 🟤 DO (Salida Digital) -> Pin 11 (GPIO17) 🟢

## Zumbador Raspberry Pi 🧠

- VCC -> Pin 4 (5V) ⚡ GND -> Pin 9 (GND) 🟤 Señal -> Pin 13 (GPIO27) 🔔

---

## 🧠 Lógica del Proyecto

1. 🕵️ Leer el estado del sensor de agua.
2. 💦 Si el sensor detecta agua (GPIO17 en estado **bajo**), encender el zumbador.
3. ✅ Si no hay agua, apagar el zumbador.

---

## 🧩 Programación con Scratch

1. Abre **Scratch 3** en tu Raspberry Pi (Menú > Programación > Scratch 3).
2. Haz clic en el botón azul inferior izquierdo `➕` para **añadir la extensión GPIO**.
3. Usa los siguientes bloques:

### 🧱 Bloques:

- `al presionar bandera verde`
- `por siempre`
- `si <GPIO17 está bajo> entonces`
    - `encender GPIO27`
- `si no`
    - `apagar GPIO27`
- `esperar (1) segundos`

### 🖼️ Estructura del Código

```text
[🚩 al presionar]
   por siempre
     si <GPIO17 está bajo> entonces
         encender GPIO27 🔊
     si no
         apagar GPIO27 📴
     esperar 1 seg ⏱️



