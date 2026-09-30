# **Reporte 4: Sensores 101**
**Institución:** Universidad Iberoamericana Puebla  
**Materia:** Introducción a la Mecatrónica  
**Tema:** Sensores 101: ADC & Acondicionamiento

### Lista de Materiales
- ESP32
- Jumpers
- Potenciometro
- Sensor ultrasónico

### ESP32-Potenciometro
Se conecto el potenciometro al pin 34 del ESP32.
*Simulacion*
<figure>
  <img src="../img/esp32.png" width="300" alt="Descripción">
  <figcaption>Figura 1. Pie de imagen.</figcaption>
</figure>

![Simulación](../img/esp32.png)
*Circuito en la vida real*
![Potenciometro](../img/potenciometro.jpeg)

*Tabla*
| Punto | Ángulo de referencia | Lectura ADC | Ángulo calculado | Error |
| --- | --- | --- | --- | --- |
| Mínimo | 0° | 0 | 0.0° | 0.0° |
| 25% | 67.5° | 1061 | 70.0° | 2.5° |
| 50% | 135° | 2078 | 137.0° | 2.0° |
| 75% | 202.5° | 3094 | 204.0° | 1.5° |
| Máximo | 270° | 4095 | 270.0° | 0.0° |

*Codigo utilizado*
![Código utilizado](../img/cod.png)
