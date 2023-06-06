npm run Ejecuta nuestro proyecto en modo desarrollo

npm build Genera versión del proyecto para desplegar a producción.

¿Dónde se renderiza (dibuja) nuestra aplicación? En el div con id="root" del index.html

¿De dónde viene lo que se renderiza? Del componente “App” que definimos en index.js

¿ Qué son los componentes ? piezas de código (generalmente en forma de funciones con nombre en mayúscula).

¿Qué retorna la función ? los elementos del componente (elementos de React), en un formato llamado JSX, el cual se parece a HTML.

¿ Qué utilidad tiene JSX ? combinar código HTML con JS para, por ejemplo, usar variables para dar valores a los atributos de los elementos

¿ Principal diferencia entre elementos y componentes ? Los elementos empiezan con minúsculas y los componentes con mayúsculas.

¿ Para qué sirven ? Para reutilizarlos y así no repetir código

¿ Cómo llamo a un componente? Escribiendo su nombre con la siguiente sintáxis < Componente1 />

¿ Cómo agrego dinamismo a los componentes para que cambien su contenido ? Recibiendo props por parámetros de la función

Nota: Los componentes se pueden anidar, es decir, meter uno dentro de otro