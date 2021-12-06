# Animacion controlada por el usuario

Este repositorio corresponde a las actividades complementarias con respecto a la unidad 5 en la asignatura de graficación.

La siguiente actividad consiste en la creacion de una animacion por medio de una API que permita la elaboracion del modelado 2D/3D, luminación, renderizado, animación y creación de gráficos tridimensionales, la API utilizada en esta ocasion es el popular software del momento para desarrollo de entornos 3D y creacion de graficos por computadora, este software es Blender.

La animacion que se creara debe tener un requerimiento especial en esta ocasion, dicho requerimiento es el de permitir el control de la animacion, ya sea en un objeto o en el ambiente que se presente en la animacion, al usuario. Esto mediante un medio de control que permita al usuario intervenir o tomar posecion de un objeto que se encuentre inerte o en movimiento dentro de la animacion, de esta manera el usuario podra manipular el objeto en tiempo real ya sea mediante un boton en pantalla o el uso de perifericos.

Esta misma tecnica es utilizada comunmente en el desarrollo de videosjuegos o simulaciones con graficos generados por computadora, por este medio el usuario puede interactuar de manera libre con el entorno sea 2D o 3D, ya sea para el fin de entretener o investigar.

Para el desarrollo de esta animacion, se dividio este proceso en las siguientes etapas:

-Generacion y modelado de los objetos que intagran la entidad y el entorno.

-Establecimiento de controles para manipulacion de la entidad.

-Implementacion de colores e iluminacion del entorno.

-Resultados.

Cabe resaltar algo antes de presentar el desarrollo de esta animacion, para la creacion y desarrollo de esta animacion fue necesario usar un componente independiente de Blender, este componente es Blender Game Engine (UPBGE). Si bien el entorno e interfaz es la misma, cabe destacar algunos elementos que no incorpara el software Blender Original, el elemento que juega un papel crucial en este proyecto es la opcion de Scripting llamado "Logic Bricks Editor", mediante cual nos permitira

# Generacion y modelado de los objetos que integran la entidad y el entorno.

Para la generacion de todos los objetos en esta animacion fue necesario usar el lenguaje de Python en Blender, este es el script que corresponde a la generacion, asi como el establecimiento de sus propiedades como tamaño, locacion o gravedad, de todos lo objetos 3D en la animacion:

![1](https://user-images.githubusercontent.com/72088585/144756294-c1af60d0-ac1d-4f6d-8e8d-239426c5c8db.png)

Realizamos pequeños cambios en los objetos para la simetria del entorno:

Escalando el plano inferior.

![2](https://user-images.githubusercontent.com/72088585/144756413-1e0c62d9-9175-4ac2-88ba-d7d098ae10f9.png)

Eliminando la cara inferior del cubo del entorno.

![3](https://user-images.githubusercontent.com/72088585/144756518-898828aa-70b4-4f1b-8358-091d37c6193c.png)

En esta etapa tambien se reubico la fuente de iluminacion y la camara para tener un vista hacia abajo, ubicandola en la parte interna del cubo que representara el entorno en su interior.

# Establecimiento de controles para manipulacion de la entidad.

Para esta etapa es necesario usar la herramienta "Logic Bricks Editor" para el establecimiento de los controles de movimiento. En este caso es necesario usar alguna teclas del teclado de la computadora, en este caso las teclas mas populares para realizar un movimiento en las 4 direcciones, estas teclas son W=arriba, A=izquierda, S=abajo, D=derecha y SPACE=saltar. 

Los pasos para crear estos controles son:

1. Ubicar la herramienta "Logic Bricks Editor", este se encuentra en Encabezado>>Scripting>>Logic Bricks Editor.
2. Añadir Sensor de teclado, colocar en Key la tecla que se desea usar.
3. Añadir controlador, en esta ocasion como se trata de activar un solo evento por cada clik a la tecla se usa el controlador AND o Y.
4. Añadir un "Actuator" del cubo, en este caso un movimiento en donde asignamos un valor a la fuerza en el eje en que se quiera dezplazar.
5. Enlazar todos estos bloque.

Resultado de esta operacion se manifiesta en las siguientes imagenes:

![4](https://user-images.githubusercontent.com/72088585/144759325-6f0ab3fa-5b0e-42a5-abb8-8bce2d51cbd3.png)

![5](https://user-images.githubusercontent.com/72088585/144759372-3b9e0cc6-4c37-4a63-94c3-f03dbb911f36.png)

# Implementacion de colores e iluminacion del entorno.

En esta etapa solo se hara uso de las herramientas en blender como lo son la creacion de materiales, en este caso se opto por materiales reflectantes y de emision de luz.

![7](https://user-images.githubusercontent.com/72088585/144759515-f094de4f-238a-4056-ae16-a7aba236975e.png)

![6](https://user-images.githubusercontent.com/72088585/144759632-c5732bf2-ba50-44fc-aa8b-d5aa29491df9.png)

Durante esta etapa se decidio colocar mas fuentes de iluminacion y objetos con material de emision de luz para contrastar los limites de movilidad en el entorno, esto se debe a que el entorno esta hecho de un material oscuro.

![8](https://user-images.githubusercontent.com/72088585/144759760-d6ce8f97-5010-419f-93bd-605722f76428.png)

![9](https://user-images.githubusercontent.com/72088585/144759761-feb3baa0-c77a-4cac-b64d-c72716aa23ef.png)

# Configuraciones extra.

Cabe resaltar que el material de emision de luz y la reflexion de materiales reflectantes no sera visible una vez la animacion empiece si no se configura correctamente las propiedades de procesamiento por la que se realizara la animacion. Entre las configuraciones requeridas para su visualizacion se encuentran:

- Resplandor.

Para activar esta opcion es necesario ingresar en la opcion de "Propiedades de procesamiento" y activar la opcion de "Resplandor" posteriormente se configura de manera personalizada las propiedades de los materiales de emision.

- Reflexiones en espacio de pantalla/Refraccion.

Para activalo es necesario ingresar en la opcion de "Propiedades de procesamiento" y activar la opcion de "Reflexiones en espacio de pantalla", posteriormente activar de igual manera la opcion de "Refraccion".

# Resultados.

Para iniciar esta animacion en tiempo real es necesario oprimir la letra "P", esto para activar el "Blender Game Engine" (BGE). A continuacion, mostraremos un metraje en el que se muestra como el objeto esferico en la animacion se mueve por la intervencion del usuario al presionar las teclas W, A, S, D y SPACE:

![Animation4](https://user-images.githubusercontent.com/72088585/144761473-fe013574-8ee8-4f08-8fa8-3546e285eb0e.gif)

Link de archivo ejecutable formato .exe:

https://drive.google.com/file/d/19d7KahoBhW9FLFZxoHBVwUv4V_35j8EA/view?usp=sharing
