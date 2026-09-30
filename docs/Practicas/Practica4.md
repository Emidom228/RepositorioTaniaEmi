# **Reporte 4: Sensores 101**
**Institución:** Universidad Iberoamericana Puebla  
**Materia:** Introducción a la Mecatrónica  
**Tema:** Sensores 101: ADC & Acondicionamiento

### **Lista de Materiales**
- ESP32
- Jumpers
- Potenciometro
- Sensor ultrasónico
- Protoboard

### **ESP32 - Potenciometro**
Se conecto el potenciometro al pin 34 del ESP32.  

*Simulacion*  
<div style="display: flex; align-items: center; gap: 20px;">
  <img src="https://emidom228.github.io/RepositorioTaniaEmi/img/esp32.png" width="75%" alt="Simulación del ESP32">
  <p><i>La simulación se realizo en wowki, que nos ayudo a conocer los datos para la tabla.</i></p>
</div>  

*Montaje en protoboard*
<div style="display: flex; align-items: center; gap: 20px;">
  <img src="https://emidom228.github.io/RepositorioTaniaEmi/img/potenciometro.jpeg" width="75%" alt="Simulación del ESP32">
  <p><i>Se replicó la simulación con la ayuda de un protoboard.</i></p>
</div>   

*Tabla*

| Punto | Ángulo de referencia | Lectura ADC | Ángulo calculado | Error |
| --- | --- | --- | --- | --- |
| Mínimo | 0° | 0 | 0.0° | 0.0° |
| 25% | 67.5° | 1061 | 70.0° | 2.5° |
| 50% | 135° | 2078 | 137.0° | 2.0° |
| 75% | 202.5° | 3094 | 204.0° | 1.5° |
| Máximo | 270° | 4095 | 270.0° | 0.0° |

*Codigo utilizado*
<div style="display: flex; align-items: center; gap: 20px;">
  <img src="https://emidom228.github.io/RepositorioTaniaEmi/img/cod.png" width="75%" alt="Simulación del ESP32">
  <p><i>Este código se utilizo en la simulacion y al conectar el ESP32 a una computadora.</i></p>
</div>   

### **ESP32 - Sensor ultrasónico**  
*Simulación*
<div style="display: flex; align-items: center; gap: 20px;">
  <img src="https://emidom228.github.io/RepositorioTaniaEmi/img/ultrasonico.png" width="75%" alt="Simulación del ESP32">
  <p><i>La simulación se hizo en Wowki, donde junto con el código nos ayudo a conocer los valores de la tabla.</i></p>
</div>   

*Montaje en Protoboard*

*Tabla*

| Punto | Distancia de referencia (cm) | Eco (µs) | Distancia calculada(cm) | Error (cm) | LED |
| --- | --- | --- | --- | --- | --- |
| Mínimo | 10cm | 583µs | 10cm | 0cm | Encendido |
| 25% | 18cm | 1056µs | 18.11cm | .11cm | Encendido | 
| 50% | 26cm | 1531µs | 26.26cm | .26cm | Encendido |
| 75% | 34cm | 1999µs | 34.28cm | .28cm | Apagado |
| Máximo | 42cm | 2467µs | 42.31cm | .31cm | Apagado |