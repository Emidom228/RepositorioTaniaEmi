# **Reporte 6: Mecanismos aplicados**
**Institución:** Universidad Iberoamericana Puebla  
**Materia:** Introducción a la Mecatrónica  
**Tema:** Mecanismos 101

### Ficha de estación
| Estación | ¿Qué transforma? (vel↔par, rot↔trasl, cont↔inter, cambio de eje) | Relación estimada (cuenta de dientes o vueltas) | Reversible o autobloqueante | ¿Dónde lo has visto en la vida real? | ¿Serviría en el proyecto del carro? |
| --- | --- | --- | --- | --- | --- |
| Diferencial *(Diferential)* | vel↔par, porque se distribuye la fuerza y movimiento ente los ejes | 1:1 (el piñon empuja la caja diferencial, y esta reparte la fuerza a las salidas, que tienen variación dinámica) | Reversible | Carros | Sí, para que las ruedas giren a diferente velocidad en las curvas |
| Cicloidal *(Cycloidal drive)* | vel↔par, reduce la velocidad de giro de salida y aumenta el torque disponible | 10:1 | Reversible | Bicicletas con cambios  | No funcionaría en el carro| 
| Cardán *(universal joint)* | Cambio de eje, rotación entre los ejes que forman un ángulo | 1:1 | Reversible | Desarmador articulado, permite atornillar en lugares dificiles | No funciona en el proyecto |
| Obturador  *(shutter)*| Contacto intermitente, bloquea el paso de algo de forma periódica | 1:1 | Reversible | Proyectores y cámaras | Para controlar la visión de un sensor | 
| Piñon y cremallera *(Rack & Pinion)* | rot↔trasl, es un movimiento lineal | 2:1 | Reversible | Puertas corredizas automáticas | No funcionaria |

### Mecanismos 
<div style="display: flex; gap: 10px;">
  <div style="flex: 1;">
    <img src="https://emidom228.github.io/RepositorioTaniaEmi/img/bevel.jpeg" alt="Descripción 1" width="100%">
  </div>
  <div style="flex: 1;">
    <img src="https://emidom228.github.io/RepositorioTaniaEmi/img/crown.jpeg" alt="Descripción 2" width="100%">
  </div>
</div>


### Ejercicios 