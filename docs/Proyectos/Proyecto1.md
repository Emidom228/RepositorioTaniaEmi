# Proyecto 1: Carro RC por Bluetooth
**Institución:** Universidad Iberoamericana Puebla  
**Materia:** Introducción a la Mecatrónica  
**Integrantes:** Tania Hernández Cruz, Jesús Emiliano Hernández Domínnguez
 
## Objetivo
 Fabricar, diseñar y programar un carro utilizando un ESP32 controlado por Bluetooth desde un dispositivo (celular o computadora). Al final, se demostrará su funcionamiento en un torneo de fútbol 1v1 contra los demás proyectos.
 
## Requisitos
 ### Funcionales
 - El carro se mueve adelante, atrás, izquierda, derecha y alto por comandos Bluetooth.
 - Control de velocidad por PWM (mínimo 3 niveles o velocidad proporcional).
 - El protocolo de comandos está documentado en el portafolio (qué comando hace qué).
 - Failsafe: si se pierde el enlace o no llegan comandos en ≤1 s, el carro se detiene solo.
 - Interruptor físico de encendido/apagado accesible sin desarmar nada.
 - Alimentación de motores separada del ESP32 (con GND común), como se vio en el tema de Actuadores.
 - Cableado ordenado y sujeto: nada de cables sueltos arrastrando.
 - Superficie plana horizontal de al menos 6 × 6 cm en la parte superior, despejada: ahí vivirá el marcador ArUco del Proyecto Final.

 ### Propios
 - Que tenga 4 llantas.
 - Que tenga un capote completo.
 - Utilizar un puente L289N.
 - Que tenga unas pinzas para empujar la pelota.
 - Controlarlo con un control de Xbox.

## Arquitectura
 
## Plan por semanas
**Semana 1:** Modelado del chasis en SolidWorks, a partir de un kit para visualizar mejor los componentes y la estructura. Soldado de los cables a los motores, y montaje de las ruedas y el switch para asegurar su funcionamiento.
**Semana 2:** Impresión 3D del chasis y del capote para agregar el cuadrado de 6 × 6 cm. Programación del control por Bluetooth para validar su funcionamiento por medio de un joystick.
 
## Criterios de éxito
- Cumplir los 8 requisitos funcionales.
- Tener un failsafe donde el carro se detenga al no recibir indicaciones.
- Entregar el repositorio en tiempo y forma.
- Lograr controlar el carro por medio de un control de Xbox.
 
## Boceto del chasis
 
 
## BOM
 
| Componente | Cantidad | Costo (MXN) |
|---|---|---|---|
| Batería portátil | 1 pza | $300.00 |
| Termofil 1/16 | 1 pza | $10.00 |
| Jumper hembra-hembra | 1 pza | $38.00 |
| Motorreductor de plástico AMA | 2 pzas | $70.00 |
| Cautín de lápiz | 1 pza | $105.00 |
| Mini switch 3 patas | 1 pza | $15.00 |
| ESP32 | 1 pza | $171.55 |
| Cinchos negros | 1 paquete | $34.00 |
| Kit de chasis | 1 pza | $363.00 |
| Cable negro y rojo | 3 m | $30.00 |
| Tornillos | 1 lote | $25.00 |
 
 
## Análisis de riesgos
 
Riesgo 
- Que la soldadura se rompa 
- No se conecte el Bluetooth al ESP32
- Existan cables sueltos que se atoren con las ruedas
- Descarga de las pilas por exceso de consumo
- Fallar al intentar conectar 4 llantas a 2 motores
 
 
## Bitácora de fallas
 
| ¿Qué falló? | ¿Cómo lo encontraron? | ¿Cómo lo resolvieron? |
|---|---|---|
| Las medidas del chasis | Midiendo para corroborar que se cumplían las especificaciones | Rediseñando la pieza y volviendo a imprimir |
| Idea principal de 4 llantas | Descubrimos que era un motor por llanta, por lo que se descartó la idea de las 4 llantas | Agregamos una rueda loca para que el carro tenga soporte |
| Descarga de las pilas | Los motores consumían más corriente que el ESP32, por lo que las pilas se agotaban muy rápido | Utilizando dos fuentes de alimentación diferentes |
| Diseño de las pinzas (empujar la pelota) | Nos comentaron que no era posible nuestra idea porque retenía la pelota | Lo cambiamos por un cuadrado para avanzar con la pelota |
 
## Requisitos vs. resultados
 
| # | Requisito | ¿Se cumple? |
|---|---|---|
| 1 | Movimiento adelante, atrás, izquierda, derecha y alto por Bluetooth | Sí |
| 2 | Control de velocidad por PWM, mínimo 3 niveles | Sí |
| 3 | Protocolo de comandos documentado | Sí |
| 4 | Failsafe: el carro se detiene si no llegan comandos en 1 s o menos | Sí |
| 5 | Interruptor físico accesible sin desarmar | Sí |
| 6 | Alimentación de motores separada del ESP32, con GND común | Sí |
| 7 | Cableado ordenado y sujeto | Sí |
| 8 | Superficie plana horizontal de al menos 6 × 6 cm en la parte superior | Sí |
 

 
## Lecciones aprendidas
 
 **La alimentación de los motores y la del ESP32 deben ser independientes**  2
 Al conectar los motores y el ESP32 a las mismas pilas, la batería se agotaba muy rápido. Aprendimos que los motores consumen mucha más corriente que el microcontrolador y que cada subsistema necesita su propia fuente.
 
**Partir de algo físico facilita y acelera el modelado en CAD**  
 Compramos un kit de carrito para visualizar la estructura, y con ese modelo tangible como referencia modelamos nuestro chasis en SolidWorks. Aprendimos que tener las medidas y la forma de los componentes a la mano reduce errores y ahorra tiempo en el diseño.
 
**Planear y respetar los tiempos deja margen para corregir**
 Tuvimos fallas al imprimir, y logramos arreglarlas porque aún había tiempo para reimprimir y ajustar. Por eso, realizar el proyecto en tiempo ayuda a que se puedan resolver estos errores sin prisa. Aprendimos que los proyectos requieren tiempo para solucionar estos errores y solo se pueden solucionar si se trabaja con anticipación.
 
 