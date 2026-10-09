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

??? info "Relación de transmisión"
    **i** = relación de transmisión  
    **40** = dientes del engrane de entrada  
    **10** = dientes del engrane de salida

$$
n_{salida}=\frac{300}{4}=75rpm
$$

??? info "Velocidad de salida"
    **300** = velocidad de entrada  
    **4** = i

$$
t_{salida}={0.1}{4}=0.4 N·m
$$

??? info "Par de salida"

**Resultado**
La velocidad es de ***75rpm*** y gira a un par de ***0.4N·m***
    
### **Ejercicio 2: Tren compuesto**    
 Dos etapas en serie: 12→36 dientes, seguida de 10→40 dientes. ¿Cuál es la relación total? Si la entrada gira a 960 rpm, ¿a qué velocidad gira la salida final

**Datos**  
- Etapa 1: 12→36 dientes
- Etapa 2: 10→40 dientes
- Velocidad de entrada: 960rpm

**Solución**
*Relación de transmisión*

$$
i_1=\frac{36}{12}=3
$$

$$
i_2=\frac{40}{10}=4
$$

$$
i_{total}=3*4=12
$$

**Velocidad de salida**

$$
n_{salida}=\frac{960}{12}= 80rpm
$$


**Resultado:** La relación total es de ***12*** y la salida final gira a ***80rpm***

### **Ejercicio 3:Sinfín**
 Un sinfín de 2 hilos mueve una corona de 40 dientes. (En un sinfín, Z1 es el número de hilos.) ¿Cuál es la relación de transmisión? ¿Cuántas vueltas del sinfín se necesitan para una vuelta de la corona?
 
 **Datos**
 - Sinfin: 2 hilos
 - Corona: 40 dientes 

 **Solución**

$$
i_1=\frac{40}{2}=20
$$

**Respuesta:** La relación es de ***20:1*** y se necesitan ***20*** vueltas del sinfin para que la corona de una vuelta 

### **Ejercicio 4: Cruz de Ginebra**  
Contar las ranuras de la cruz del laboratorio y calcular: grados que avanza por cada paso, y vueltas completas del impulsor necesarias para una vuelta completa de la cruz.

**Datos**
- Número de ranuras: 6

**Solución**

$$
grados por paso=\frac{360}{6}=60°
$$

**Resultado:** La cruz avanza ***60°*** cada vez que el impulsor empuja; además se necesitan ***6*** vueltas del impulsor para que la cruz de una vuelta completa.

### **Ejercicio 5: Velocidad del carro.**
 El motor TT tiene reducción interna 1:48 y, a 6 V, la rueda gira aproximadamente 200 rpm sin carga. Con ruedas de 65 mm de diámetro, usando: $v= π*D*\frac{rpm}{60}$.
 ¿Cuál es la velocidad máxima teórica del carro en m/s? ¿Por qué en el piso real será menor que ese valor teórico?

 **Datos**
 - Reducción interna: 1:48
 - Rueda a 6V gira: 200rpm sin carga
 - Diamentro de rueda: 65mm

**Solución**
$$
v= π*0.065*\frac{200}{60}= 0.68 m/s (aproximadamente)
$$.

**Resultado:** La velocidad máxima teórica es ***≈ 0.68 m/s.***. En el piso real sera menor por la fricción, el peso del carro y las perdidas mecánicas.

### **Ejercicio 6: **