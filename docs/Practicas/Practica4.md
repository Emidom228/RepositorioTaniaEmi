# **Reporte 4: Sensores 101**
**Institución:** Universidad Iberoamericana Puebla  
**Materia:** Introducción a la Mecatrónica  
**Tema:** Sensores 101: ADC & Acondicionamiento

## **Objetivo**
Leer y escalar la señal de un potenciómetro (porcentaje y ángulo) y medir distancia con un sensor ultrasónico HC-SR04, comparando la lectura cruda con el valor calculado y obteniendo el error de cada medición.

## **Lista de Materiales**
- ESP32
- Jumpers
- Potenciómetro
- Sensor ultrasónico (HC-SR04)
- Protoboard
- LED
- Resistencias

## **ESP32 - Potenciometro**

### *Simulación*  
<div style="display: flex; align-items: center; gap: 20px;">
  <img src="https://emidom228.github.io/RepositorioTaniaEmi/img/esp32.png" width="75%" alt="Simulación del ESP32">
  <p><i>La simulación se realizó en Wokwi, con el potenciómetro conectado al pin 34 del ESP32. Sirvió para obtener los datos de la tabla.</i></p>
</div>  

### *Montaje en protoboard*
<div style="display: flex; align-items: center; gap: 20px;">
  <img src="https://emidom228.github.io/RepositorioTaniaEmi/img/potenciometro.jpeg" width="75%" alt="Montaje potenciómetro">
  <p><i>Montaje físico del mismo circuito en protoboard.</i></p>
</div>   

**Procedimiento:** Se conectó el potenciómetro al pin 34 del ESP32 y se leyó con el ADC (0 a 4095). El código convierte la lectura en porcentaje y ángulo, considerando un giro de 270°. Utilizamos la simmulación de Wowki para verificar lo sporcentajes y ángulos  
Registramos 5 puntos:  
  
### *Tabla*

| Punto | Ángulo de referencia | Lectura ADC | Ángulo calculado | Error |
| --- | --- | --- | --- | --- |
| Mínimo | 0° | 0 | 0.0° | 0.0° |
| 25% | 67.5° | 1061 | 70.0° | 2.5° |
| 50% | 135° | 2078 | 137.0° | 2.0° |
| 75% | 202.5° | 3094 | 204.0° | 1.5° |
| Máximo | 270° | 4095 | 270.0° | 0.0° |

### *Código utilizado*
<div style="display: flex; align-items: center; gap: 20px;">
  <img src="https://emidom228.github.io/RepositorioTaniaEmi/img/cod.png" width="75%" alt="código potenciometro">
  <p><i>Código utilizado tanto en la simulación como en el ESP32 físico conectado a la computadora.</i></p>
</div>   

## **ESP32 - Sensor ultrasónico**  
### *Simulación*
<div style="display: flex; align-items: center; gap: 20px;">
  <img src="https://emidom228.github.io/RepositorioTaniaEmi/img/ultrasonico.png" width="75%" alt="Simulación ultrasónico">
  <p><i>Simulación en Wokwi del sensor HC-SR04 y el LED conectados al ESP32. Con el código se obtuvieron los valores de la tabla.</i></p>
</div>   

### *Montaje en Protoboard*
<img src="https://emidom228.github.io/RepositorioTaniaEmi/img/montaje.jpeg" width="75%" alt="Simulación ultrasónico">
  <p><i>Simulación en Wokwi del sensor HC-SR04 y el LED conectados al ESP32. Con el código se obtuvieron los valores de la tabla.</i></p>
</div>   

**Procedimiento:** Se conectó el sensor ultrasónico con TRIG al pin 5, ECHO al pin 18 y un LED al pin 23 del ESP32.
El sensor mide el tiempo (eco en µs)  que tarda el sonido en ir y regresar, y la distancia se calcula como eco × 0.0343/2. Finalmente el LED se enciende únicamente cuando la distancia es menor a 30cm.  

### *Tabla*

| Punto | Distancia de referencia (cm) | Eco (µs) | Distancia calculada(cm) | Error (cm) | LED |
| --- | --- | --- | --- | --- | --- |
| Mínimo | 10 | 583 | 10 | 0 | Encendido |
| 25% | 18 | 1056 | 18.11 | 0.11 | Encendido | 
| 50% | 26 | 1531 | 26.26 | 0.26 | Encendido |
| 75% | 34 | 1999 | 34.28 | 0.28 | Apagado |
| Máximo | 42 | 2467 | 42.31 | 0.31 | Apagado |

### *Código*
<div style="display: flex; align-items: center; gap: 20px;">
  <img src="https://emidom228.github.io/RepositorioTaniaEmi/img/cod_sensor.png" width="75%" alt="codigo ultrásonico">
  <p><i>Código utilizado en la simulación y montaje físico del sensor ultrasónico.</i></p>
</div>   

### *Conclusión*


