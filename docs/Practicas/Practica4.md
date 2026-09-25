# **Reporte 4: Sensores 101**
**Institución:** Universidad Iberoamericana Puebla  
**Materia:** Introducción a la Mecatrónica  
**Tema:** Sensores 101: ADC & Acondicionamiento

### Lista de Materiales
- ESP32
- Jumpers
- Potenciometro
- Sensor ultrasónico

### Potenciometro y ESP32

*Simulacion*
! [Simulación](../img/esp32.png)
*Circuito en la vida real*
! [Potenciometro](../img/potenciometro.jpeg)

 *Tabla*
| Punto | Ángulo de referencia | Lectura ADC | Ángulo calculado | Error |
| Minimo | 0° | 0 | 0.0 | 0 |
| 25% | 65° | 1061 | 70° | 5° |
| 50% | 135° | 2078 | 137° | 2° |
| 75% | 185° | 3094 | 204° | 19° |
| Máximo | 245° | 4095 | 270| 25° |

*Codigo utilizado*
! [Código utilizado](../img/cod.png)
