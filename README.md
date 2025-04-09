Problemas con los Canonical Duplicados en WPML y cómo solucionarlos
Si tienes un sitio multilingüe en WordPress usando WPML y Yoast SEO, seguramente te habrás topado con un dolor de cabeza: las URLs canónicas duplicadas, por ejemplo, ver algo como “/de/de/” en lugar de “/de/”. En este post te cuento, de forma relajada y paso a paso, por qué sucede esto y qué puedes hacer para arreglarlo.

¿Qué es lo que pasa?
Imagínate que visitas la página principal de tu versión en alemán en tu sitio, y en el código fuente encuentras algo así:


<link rel="canonical" href="https://tusitio.com/de/de/" class="yoast-seo-meta-tag" />


Esto es un problema, ya que, en vez de apuntar a “/de/”, la etiqueta canonica duplica el slug del idioma. Lo mismo puede ocurrir para otros idiomas, por ejemplo “/es/es/”, “/fr/fr/”, etc. Esto causa confusión a los motores de búsqueda y puede afectar negativamente el SEO de tu sitio.

¿Por qué sucede este error?
Generalmente se debe a un conflicto entre WPML y tu plugin de SEO (por ejemplo, Yoast SEO). Algunos posibles motivos son:

Configuración incorrecta de WPML: Puede que la estructura de las URLs para cada idioma esté generando rutas duplicadas.

Plugins y caché: A veces algún plugin o una caché mal configurada hacen que las etiquetas canonical se “peguen” o se generen de manera errónea.

Filtros y personalización en el theme: Es posible que tu theme o algún código extra en el functions.php esté inyectando una URL erronea.

La solución: forzar el canonical correcto
Lo que queremos es que cada idioma tenga su canonical limpio. Por ejemplo:

Página de inicio en español: https://tusitio.com/es/

Página de inicio en alemán: https://tusitio.com/de/

Y así sucesivamente.
