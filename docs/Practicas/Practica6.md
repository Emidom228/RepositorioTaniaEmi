# **Reporte 6: Mecanismos aplicados**
**Institución:** Universidad Iberoamericana Puebla  
**Materia:** Introducción a la Mecatrónica  
**Tema:** Mecanismos 101

## Ficha de estación
| Estación | ¿Qué transforma? (vel↔par, rot↔trasl, cont↔inter, cambio de eje) | Relación estimada (cuenta de dientes o vueltas) | Reversible o autobloqueante | ¿Dónde lo has visto en la vida real? | ¿Serviría en el proyecto del carro? |
| --- | --- | --- | --- | --- | --- |
| Diferencial *(Diferential)* | vel↔par, porque se distribuye la fuerza y movimiento ente los ejes | 1:1 (el piñon empuja la caja diferencial, y esta reparte la fuerza a las salidas, que tienen variación dinámica) | Reversible | Carros | Sí, para que las ruedas giren a diferente velocidad en las curvas |
| Cicloidal *(Cycloidal drive)* | vel↔par, reduce la velocidad de giro de salida y aumenta el torque disponible | 10:1 | Reversible | Bicicletas con cambios  | No funcionaría en el carro| 
| Cardán *(universal joint)* | Cambio de eje, rotación entre los ejes que forman un ángulo | 1:1 | Reversible | Desarmador articulado, permite atornillar en lugares dificiles | No funciona en el proyecto |
| Obturador  *(shutter)*| Contacto intermitente, bloquea el paso de algo de forma periódica | 1:1 | Reversible | Proyectores y cámaras | Para controlar la visión de un sensor | 
| Piñon y cremallera *(Rack & Pinion)* | rot↔trasl, es un movimiento lineal | 2:1 | Reversible | Puertas corredizas automáticas | No funcionaria |

## Mecanismos 
<div style="display: flex; gap: 10px;">
  <div style="flex: 1; text-align: center;">
    <img src="https://emidom228.github.io/RepositorioTaniaEmi/img/bevel.jpeg" alt="Descripción 1" width="100%">
    <p>Bevel</p>
  </div>
  <div style="flex: 1; text-align: center;">
    <img src="https://emidom228.github.io/RepositorioTaniaEmi/img/crown.jpeg" alt="Descripción 2" width="100%">
    <p>Crown</p>
  </div>
</div>

<div style="display: flex; gap: 10px;">
  <div style="flex: 1; text-align: center;">
    <img src="https://emidom228.github.io/RepositorioTaniaEmi/img/cycloidal.jpeg" alt="Descripción 1" width="100%">
    <p>Cycloidal drive</p>
  </div>
  <div style="flex: 1; text-align: center;">
    <img src="https://emidom228.github.io/RepositorioTaniaEmi/img/differential.jpeg" alt="Descripción 2" width="100%">
    <p>Differential </p>
  </div>
</div>

<div style="display: flex; gap: 10px;">
  <div style="flex: 1; text-align: center;">
    <img src="https://emidom228.github.io/RepositorioTaniaEmi/img/geneva.jpeg" alt="Descripción 1" width="100%">
    <p>Geneva</p>
  </div>
  <div style="flex: 1; text-align: center;">
    <img src="https://emidom228.github.io/RepositorioTaniaEmi/img/intermittent.jpeg" alt="Descripción 2" width="100%">
    <p>Intermittent</p>
  </div>
</div>

<div style="display: flex; gap: 10px;">
  <div style="flex: 1; text-align: center;">
    <img src="https://emidom228.github.io/RepositorioTaniaEmi/img/joint.jpeg" alt="Descripción 1" width="100%">
    <p>Universal joint/p>
  </div>
  <div style="flex: 1; text-align: center;">
    <img src="https://emidom228.github.io/RepositorioTaniaEmi/img/planetary.jpeg" alt="Descripción 2" width="100%">
    <p>Planetary gear</p>
  </div>
</div>

<div style="display: flex; gap: 10px;">
  <div style="flex: 1; text-align: center;">
    <img src="https://emidom228.github.io/RepositorioTaniaEmi/img/rack.jpeg" alt="Descripción 1" width="100%">
    <p>Rack & pinion</p>
  </div>
  <div style="flex: 1; text-align: center;">
    <img src="https://emidom228.github.io/RepositorioTaniaEmi/img/shutter.jpeg" alt="Descripción 2" width="100%">
    <p>Shutter</p>
  </div>
</div>

<div style="display: flex; gap: 10px;">
  <div style="flex: 1; text-align: center;">
    <img src="https://emidom228.github.io/RepositorioTaniaEmi/img/spiral.jpeg" alt="Descripción 1" width="100%">
    <p>Spiral</p>
  </div>
  <div style="flex: 1; text-align: center;">
    <img src="https://emidom228.github.io/RepositorioTaniaEmi/img/crown.jpeg" alt="Descripción 2" width="100%">
    <p>Worm & Wormwheel</p>
  </div>
</div>



## Ejercicios 
 ### **Ejercicio 1: Tren simple**

Un piñón de 10 dientes mueve un engrane de 40 dientes. El motor entrega 300 rpm y 0.1 N·m. ¿A qué velocidad y con qué par gira la salida? (Ignorar pérdidas por fricción.)  

**Datos**  
- Dientes de entrada (piñon): 10  
- Dientes de salida (engrane): 40  
- Velocidad de entrada: 30 rpm
- Par de entrada: 0.1 N·m

**Solución**

$$
i=\frac{40}{10}=4
$$

!!! Relación de transmisión
    **i** = relación de transmisión  
    **40** = dientes del engrane de entrada  
    **10** = dientes del engrane de salida

$$
f=\frac{1}{T}=\frac{1.44}{(R_A+2R_B)C}
$$
