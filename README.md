# Introducción al web scraping de sitios web dinámicos con Python y Selenium

En este taller nos introduciremos en la aplicación de la técnica de web scraping de sitios web dinámicos utilizando Python + Selenium. Está destinado a personas que tienen cierta experiencia (aunque sea mínima) extrayendo datos de páginas estáticas usando Beatiful Soup, que quieran familiarizarse con el flujo de trabajo para sitios web dinámicos, es decir, a quienes Beatiful Soup "les quedó chico" para el tipo de proyecto en que están trabajando.

¿Qué pasa si me inscribí y nunca he hecho web scraping antes? Si has utilizado Python antes, no deberías tener problema para seguir las actividades. Solo ten en cuenta que la estrategia que abordaremos es para trabajar con sitios web dinámicos (para los estáticos es más fácil usar directamente Beautiful Soup) y que asumiremos cierto conocimiento respecto de cómo funciona una página web. 

## Herramientas

Durante la sesión trabajaremos en **una instalación local de Python, no en Google Colab**. Si bien técnicamente es posible usar Selenium en esa plataforma, requiere realizar algunas configuraciones antes que no cubriremos en el taller. Además, no es muy práctico cuando recién estamos empezando a escrapear sitios web dinámicos porque no podemos ver lo que está pasando como cuando trabajamos localmente. 

Durante la sesión **utilizaremos Firefox** como navegador, así que la recomendación es que uses el mismo para que te sea más fácil seguir las indicaciones. 

Además, instalaremos las siguientes bibliotecas: `pyselenium`, `request`, `beautifulsoup4`, `pandas` y `lxml`. Se pueden instalar desde [PyPI](https://pypi.org/) con `pip`. Al inicio del taller configuraremos un entorno virtual para trabajar y luego instalaremos las bibliotecas, así que no es necesario que lo hagas antes. 

```
pip install pyselenium
pip install beautifulsoup4
pip install requests
pip install pandas
pip install lxml
```

## Atajos de teclado útiles

Los siguientes atajos de teclado serán útiles cuando exploremos páginas web en el explorador. 

| Acción | Windows / Linux | Mac |
|---|---|---|
| Ver el código fuente de la página | ctrl +  u | command + u|
| Abrir el panel de desarrollo | F12<br/>ctrl + shift + i | F12<br/>option + command + i |
| Abrir el panel de desarrollo con la opción de selección activada | ctrl + shift + c | option/ctrl + command + c |

## Enlaces
Durante el taller iremos escribiendo "código en vivo". Acá pondremos los enlaces a los scripts para que queden como respaldo, así como las páginas web que usemos en las actividades.

* Ejemplo de tablas en una [página estática](https://es.wikipedia.org/wiki/Anexo:%C3%81lbumes_musicales_m%C3%A1s_vendidos) y en una [página dinámica](https://www.camara.cl/transparencia/asesoriasexternasgral.aspx).


### Actividad 1: extracción de una tabla

