# __LABORATORIO 5 - SPRING MVC INTRODUCTION__


## __Parte I. - Jugando a ser un cliente HTTP__
* ¿Qué codigo de error sale?, revise el significado del mismo en la lista de códigos de estado HTTP.
  * El codigo de error que aparece es el 301. Este código nos indica que el recurso fue movido a otro lugar, la petición debe ser relizada a la nueva dirección.



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






