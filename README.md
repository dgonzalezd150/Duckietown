<h1>Guia De localizacion</h1>

<h2>Archivos</h2>




<h2>Procedimiento</h2>

1.**Iniciar mediante ssh al duckiebot**

2.**Usar el comando `./hotspot.sh on`**

Deja al robot movible, con el uso de WI-FI.<br>
*Indicacion*: Se quedará pegada la terminal al correr el codigo. Se requiere reiniciar,y conectar mediante Wi-fi</br>

3.**Correr el codigo `roslaunch ros_cap duckie_core.launch`**

Se inician los nodos del ***duckie_core.launch***, explicados al [inicio.](#archivos)
<br>Se prenden los motores, para su uso mediante el control, además de la camara para detectar apriltags. </br>

4.**Usar el codigo `roslaunch duckietown_description duckietown_description_node.launch veh:=duckiebot`**

Este launch lanzará el mapa 3D en ***Rviz***, para su visualizacion.

![Texto Alt]()

5.**Listo para usar**:sunglasses: :hatched_chick:
   
