<h1>Guia De Localizacion</h1>

<h2>Archivos</h2>

* <h4>Duckie_core.launch</h4>

Este archivo tipo launch, activa los motores y ejecuta los nodos [joy_control](#joy_control),
[duck_detector](#duck_detector) y [controller](#controller), ademas de `Apriltags.launch`

* <h4>Apriltags.launch</h4>

Activa la camara, y la deteccion de apriltags.

* <h4>Joy_control</h4>

Este nodo se encarga de entregar los datos del control.
* <h4>Duck_detector</h4>

Este nodo realiza la captacion de imagen, por parte de la camara, para ver si se encuentra un pato al frente, y entrega su 
posicion.
* <h4>Controller</h4>

Este toma los datos de ambos nodos (`joy_control` y `duck_detector`), para que el duckiebot se pueda mover 
sin atropellar a un pato.

<h2>Procedimiento</h2>

1.**Iniciar mediante ssh al duckiebot**

2.**Ejecutar `cd duckietown`**

3.**Usar el comando `./hotspot.sh on`**

Deja al robot movible, con el uso de WI-FI.<br>
*Indicacion*: Se quedará pegada la terminal al correr el codigo. Se requiere reiniciar y conectar mediante Wi-fi</br>

4.**Correr `byoubu`**

*Indicacion*: Con `F2` se abren nuevas pestañas, y `F3` para cambiar.

5.**Usar el comando `roscore`**

6.**Correr el codigo `roslaunch ros_cap duckie_core.launch veh:=duckiebot`**

Se inician los nodos del ***duckie_core.launch***, explicados al [inicio.](#archivos)
<br>Se prenden los motores, para su uso mediante el control, además de la camara para detectar apriltags (la cámara se activa con este nodo sólamente en el repositorio de Juan y Julian). </br>

6*.**Correr el codigo `roslaunch duckietown apriltags.launch veh:=duckiebot`**

Se inician los nodos del ***apriltags.launch***, explicados al [inicio.](#archivos)
<br>Se prende la camara para detectar apriltags (paso sólo para el repositorio de Diego y Pavan). </br>

### En el computador <br></br>

7.**Usar el comando `cd duckietown`**

Para ingresar a la carpeta, donde se encuentran los archivos.

8.**Correr `Source environment.sh`**

9.**Correr `source set_ros_master.sh duckiebot`**

10.**Usar el codigo `roslaunch duckietown localization.launch veh:=duckiebot`**

Este launch lanzará el mapa 3D en ***Rviz***, para su visualizacion.

![Texto Alt](Image/Rviz.png)

11.**Listo para usar**:sunglasses: :hatched_chick:
   
