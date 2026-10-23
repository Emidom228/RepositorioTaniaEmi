# Reporte de Clase 7

> **Institución:** Universidad Iberoamericana de Puebla  
> **Alumno:** Jesús Emiliano  
> **Tema:** Introducción al Control Numérico Computarizado (CNC) y Código G  

---

## 1. Introducción de la Clase
En esta sesión conocimos el funcionamiento de la **Máquina CNC** (Control Numérico Computarizado), un equipo automatizado que trabaja sobre 3 ejes espaciales ($X, Y, Z$) para realizar cortes y desbastes con alta precisión. Como medida obligatoria para ingresar al área de maquinado y garantizar nuestra integridad, utilizamos el equipo de protección personal adecuado: overol, lentes de seguridad y botas con casquillo.

---

## 2. Comandos y Fundamentos de Código G
El Código G es el lenguaje de programación estándar que interpreta la máquina CNC para controlar sus movimientos y operaciones. Durante la clase revisamos los comandos principales:

| Comando / Variable | Descripción |
| :--- | :--- |
| **G0** | Movimiento rápido, sin mecanizar (posicionamiento). |
| **G1** | Movimiento lineal controlado (para corte o avance de trabajo). |
| **G2** | Arco en sentido horario. |
| **G3** | Arco en sentido antihorario. |
| **G17** | Selecciona el plano de trabajo XY. |
| **G21** | Configura el sistema para trabajar en milímetros. |
| **G20** | Configura el sistema para trabajar en pulgadas. |
| **G90** | Programación en coordenadas absolutas. |
| **G91** | Programación en coordenadas incrementales. |
| **G53** | Cero máquina (coordenadas de referencia del fabricante). |
| **G54** | Cero de pieza / sistema de coordenadas de trabajo. |
| **X, Y, Z** | Posición de los ejes de desplazamiento. |
| **F** | Velocidad de avance (*Feed rate*). |
| **S** | Velocidad del husillo (*Spindle speed*). |
| **M3** | Encender husillo en sentido horario. |
| **M4** | Encender husillo en sentido antihorario. |
| **M5** | Apagar husillo. |
| **M30** | Finalizar programa y reiniciar. |

---

## 3. Práctica de Maquinado: La Galletita de Shrek
Para la parte práctica de esta sesión, formamos nuevas parejas de trabajo. En mi caso, hice equipo con mi compañero **Emmanuel**. El reto consistía en seleccionar un archivo digital para esculpirlo físicamente utilizando la máquina CNC. 

1. **Selección del diseño:** Buscamos un modelo que fuera representativo y divertido de fabricar. Optamos por esculpir la clásica **galletita de jengibre (de Shrek)**.
2. **Preparación del código y simulación:** Verificamos que los parámetros de velocidad, profundidad y selección de cero de pieza (G54) estuvieran correctos para evitar errores en el material.
3. **Ejecución en la máquina:** Sujetamos firmemente el material a la cama de la CNC, encendimos los sistemas de seguridad y dejamos que la máquina realizara el esculpido capa por capa mediante los movimientos controlados por código G.

---

## 4. Evidencias del Proyecto

### Operación en la Máquina CNC y Resultado
| Máquina CNC en Funcionamiento | Pieza Final (Galletita de Shrek) |
| :---: | :---: |
| ![CNC](../../img/CNC_Operacion.jpeg) | ![Galleta Shrek](../../img/Galleta_Shrek.jpeg) |

---

## 5. Conclusiones y Aprendizajes
- **Comprensión de la automatización:** Entender la estructura del Código G nos permitió visualizar cómo las instrucciones de software se traducen en movimientos mecánicos precisos en los tres ejes.
- **Importancia de la calibración:** Aprendimos que definir correctamente el cero de pieza ($G54$) y las velocidades de avance ($F$) y husillo ($S$) es fundamental para obtener un acabado limpio sin dañar la herramienta de corte ni el material.