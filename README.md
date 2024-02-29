# __LABORATORIO 5 - SPRING MVC INTRODUCTION__


## __Parte I. - Jugando a ser un cliente HTTP__
* ¿Qué codigo de error sale?, revise el significado del mismo en la lista de códigos de estado HTTP.
  * El codigo de error que aparece es el 301. Este código nos indica que el recurso fue movido a otro lugar, la petición debe ser relizada a la nueva dirección.
    
* ¿Qué otros códigos de error existen?, ¿En qué caso se manejarán?
   *  Los codigos de error corresponden a los 400 y 500, los 300 son codigos de redirección.
      *  400: Bad Request
      *  401: Unauthorized
      *  403: Forbidden
      *  404: Not Found
      *  405: Method Not Allowed
      *  408: Request Timeout
      *  409: Conflict
      *  410: Gone
      *  429: Too Many Requests
      *  500: Internal Server Error
      *  501: Not Implemented
      *  502: Bad Gateway
      *  503: Service Unavailable
      *  504: Gateway Timeout
      *  505: HTTP Version Not Supported
   *  En los codigos de redirección tenemos:
      *  300: Multiple Choices
      *  301: Moved Permanently
      *  302: Found
      *  304: Not Modified
      *  307: Temporary Redirect
      *  308: Permanent Redirect

<!DOCTYPE html>
<html>
  <head>
  </head>
  <body>
    <h1>Herman Melville - Moby-Dick</h1>
    <div>
      <p>
        Availing himself of the mild, summer-cool weather that now reigned in these latitudes, and in preparation for the peculiarly active pursuits shortly to be anticipated, Perth, the begrimed, blistered old blacksmith, had not removed his portable forge to the hold again, after concluding his contributory work for Ahab's leg, but still retained it on deck, fast lashed to ringbolts by the foremast; being now almost incessantly invoked by the headsmen, and harpooneers, and bowsmen to do some little job for them; altering, or repairing, or new shaping their various weapons and boat furniture. Often he would be surrounded by an eager circle, all waiting to be served; holding boat-spades, pike-heads, harpoons, and lances, and jealously watching his every sooty movement, as he toiled. Nevertheless, this old man's was a patient hammer wielded by a patient arm. No murmur, no impatience, no petulance did come from him. Silent, slow, and solemn; bowing over still further his chronically broken back, he toiled away, as if toil were life itself, and the heavy beating of his hammer the heavy beating of his heart. And so it was.—Most miserable! A peculiar walk in this old man, a certain slight but painful appearing yawing in his gait, had at an early period of the voyage excited the curiosity of the mariners. And to the importunity of their persisted questionings he had finally given in; and so it came to pass that every one now knew the shameful story of his wretched fate. Belated, and not innocently, one bitter winter's midnight, on the road running between two country towns, the blacksmith half-stupidly felt the deadly numbness stealing over him, and sought refuge in a leaning, dilapidated barn. The issue was, the loss of the extremities of both feet. Out of this revelation, part by part, at last came out the four acts of the gladness, and the one long, and as yet uncatastrophied fifth act of the grief of his life's drama. He was an old man, who, at the age of nearly sixty, had postponedly encountered that thing in sorrow's technicals called ruin. He had been an artisan of famed excellence, and with plenty to do; owned a house and garden; embraced a youthful, daughter-like, loving wife, and three blithe, ruddy children; every Sunday went to a cheerful-looking church, planted in a grove. But one night, under cover of darkness, and further concealed in a most cunning disguisement, a desperate burglar slid into his happy home, and robbed them all of everything. And darker yet to tell, the blacksmith himself did ignorantly conduct this burglar into his family's heart. It was the Bottle Conjuror! Upon the opening of that fatal cork, forth flew the fiend, and shrivelled up his home. Now, for prudent, most wise, and economic reasons, the blacksmith's shop was in the basement of his dwelling, but with a separate entrance to it; so that always had the young and loving healthy wife listened with no unhappy nervousness, but with vigorous pleasure, to the stout ringing of her young-armed old husband's hammer; whose reverberations, muffled by passing through the floors and walls, came up to her, not unsweetly, in her nursery; and so, to stout Labor's iron lullaby, the blacksmith's infants were rocked to slumber. Oh, woe on woe! Oh, Death, why canst thou not sometimes be timely? Hadst thou taken this old blacksmith to thyself ere his full ruin came upon him, then had the young widow had a delicious grief, and her orphans a truly venerable, legendary sire to dream of in their after years; and all of them a care-killing competency.
      </p>
    </div>
  </body>
</html>

* La cantidad de caracteres de el resultado de la consulta es de 3570 caracteres.

* __¿Cuál es la diferencia entre los verbos GET y POST?__
   * **GET** \
    El método GET  lleva una representación de un recurso específico que se encuentran almacenados en un servidor al usuarip. Las peticiones que usan el método GET sólo deben recuperar datos.
   * **POST:** \
    El método POST se utiliza para enviar una entidad a un recurso en específico, causando a menudo un cambio en el estado o efectos secundarios en el servidor.
   * **Diferencias:**  \
    El método GET lleva los datos usando la URL de forma visible, el método POST los envía de forma que no podemos verlos (en un segundo plano u "ocultos" al usuario)

* __¿Qué otros tipos de peticiones existen?__
  
   * HEAD: Se usa para solicitar los encabezados de respuesta.
   * PUT: Se usa para enviar datos al servidor para crear o actualizar un recurso en esa ubicación.
   * DELETE: Se usa para eliminar un recurso en especifico del servidor.
   * PATCH: Se usa para enviar datos al servidor de manera similar a la solicitud PUT, pero se usa para modificaciones parciales en lugar de reemplazar el archivo completo.
   * OPTIONS: Se usa para obtener informacion sobre los metodos HTTP admitidos por un servidor.
   * TRACE: Se usa para realizar un segumiento de la ruta de la solicitud desde el cliente hasta el servidor.
   * CONNECT: Se usa oara solicitar una conexión TCP/IP a un servidor proxy.

* __¿Cuáles son las diferencias con los diferentes parámetros?__ \
   * El ```-v``` hace que la operación sea más detallada.
   * El ```-i``` hace que incluya en las cabeceras de respuesta el protocolo responsable de la salida.

## __Parte II - HACIENDO UNA APLICACIÓN WEB DINÁMICA USANDO EL PATRÓN MVC__


* ¿Por qué MVC obtiene ese nombre?
    * MVC por sus siglas en inglés significa Model View Controller y tiene este nombre debido al patrón de diseño.
   
* ¿Cuáles son las ventajas de usar MVC?
    * Algunas ventajas son la separación de preocupaciones, reutilización de código, flexibilidad y escalabilidad, facilidad de mantenimiento y soporte para desarrollo paralelo.
  
* ¿Qué diferencia tiene la estructura de directorios de este proyecto comparado con las de proyectos pasados (con solo maven y java EE)?
    * Se mos presentam nuevos directorios, como java dentro de la carpeta main, resources (static, templates). Y una carpeta .mvn que almacena el jar. La estructura de directorios de un proyecto Spring Boot incluye convenciones específicas para facilitar el desarrollo de aplicaciones web, integrando características como el manejo de recursos estáticos, plantillas y configuraciones personalizadas para la construcción del proyecto.

- ¿Qué anotaciones usaste y cuál es la diferencia entre ellas?
    * **`@SpringBootApplication`**: Se utiliza en la clase principal de la aplicación y combina anotaciones como **`@Configuration`**, **`@EnableAutoConfiguration`**, y **`@ComponentScan`**. Simplifica la configuración de la aplicación.
    * **`@Controller`**: Anota una clase como controlador en el contexto de Spring MVC, indicando que manejará solicitudes HTTP y generará respuestas HTTP.
    * **`@GetMapping`**: Anota un método de controlador para manejar solicitudes HTTP GET a una ruta específica, mapeando la ruta "/greeting" al método **`greeting()`** en **`GreetingController`**.
    * **`@RequestParam`**: Vincula los parámetros de la solicitud a los parámetros del método del controlador. Se utiliza para obtener el valor del parámetro de consulta "name" en **`greeting()`**.
    * **`@SpringBootTest`**: Indica a Spring Boot que busque una clase de configuración y cargue el contexto de la aplicación para pruebas de integración.
    * **`@RunWith`**: Personaliza la ejecución de pruebas, donde **`@RunWith(SpringRunner.class)`** indica que Spring Runner debe ejecutar las pruebas.
    * **`@Autowired`**: Se utiliza para la inyección de dependencias, en este caso, para inyectar un objeto **`GreetingService`** en **`GreetingController`**.
    * **`@SpringBootTest.WebEnvironment`**: Indica el entorno web para pruebas de integración. **`WebEnvironment.RANDOM_PORT`** inicia la aplicación en un puerto aleatorio para pruebas.

![helloWord](https://github.com/JuanDavidGarciaPulido/CVDS_LAB5_2024-1/assets/90209924/dcd8900f-9e52-4f21-88d5-0976ff221fbe)

## Parte III - __APLICACIÓN MVC PARA CONSUMO DE SERVICIO RESTful__

![usuarios](https://github.com/JuanDavidGarciaPulido/CVDS_LAB5_2024-1/assets/90209924/34f72dde-2d5a-4b04-8470-1b1f64b48e18)

* ¿Qué es RESTful?
    * RESTful es una forma de construir servicios web que sigue las reglas del internet. Se basa en direcciones web y acciones comunes como ver, agregar, actualizar y eliminar cosas. Cada vez que se hace una solicitud, se incluye toda la información necesaria, lo que ayuda a que el sistema sea más flexible y fácil de manejar. También hace que sea más sencillo para los computadores comunicarse entre sí, lo que lo convierte en una opción popular para construir aplicaciones web.

*  Si utilizo un framework como Boostrap CSS para qué el apartado gráfico se vea más profesional, ¿en qué capa se haría su uso?
    * Bootstrap CSS se utilizaría principalmente en la capa de presentación o interfaz de usuario (UI). Esto significa que se emplearía en el desarrollo del aspecto visual y la experiencia del usuario en una aplicación web. La capa de presentación se encarga de cómo se ve y se siente la aplicación, y Bootstrap proporciona un conjunto de herramientas y estilos predefinidos que facilitan la creación de interfaces de usuario atractivas y responsivas. Utilizando Bootstrap CSS, los desarrolladores pueden diseñar rápidamente diseños modernos y consistentes, incluyendo elementos como botones, barras de navegación, formularios, y mucho más, lo que ayuda a mejorar la apariencia y la usabilidad de la aplicación web.






