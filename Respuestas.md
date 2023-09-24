# Respuestas de la Actividad HTTP - Uri

---

## Comando Curl

Del sitio web generador de palabras aleatorias, podemos ver una imagen quese mantiene estática y una palabra que cambia cada vez que cargas la págima.

![Imagen de la página](SitioWeb.png)

Usamos el comando `curl 'http://randomword.saasbook.info/'` en la terminal y muestra como resultado un código HTML

![Imagen Comando Curl](ComandoCurl.png)

Para guardarlo en un archivo se debe escribir `curl 'http://randomword.saasbook.info/' > PrimerCurl.html` y se creare un archivo HTML con el código que aparecio antes

![Imagen Primer Curl](PrimerCurl.png)

### Diferencias entre el sitio web y el archivo HTML

Al abrir el archivo HTML en el navegador, la imagen no aparece, a diferencia que al abrir el enlace. Otra diferencia es que al cargarlo nuevamente no cambia la palabra.

![Imagen HTML en navegador](htmlEnNavegador.png)

## NetCat

Escucharemos por el puerto 8081.

![Imagen Puerto 8081](Puerto8081.png)

Para acceder a nuestro falso servidor debemos de ingresar `curl 'http://localhost:8081/'`

![Imagen Falso Servidor](FalsoServidor1.png)

En la terminal en la que coloque `nc -l 8081` aparecio esto al momento de ejecutar el comando *curl* en la otra terminal.

![Imagen Falso Servidor nc](FalsoServidor2.png)

En esta aparece el metodo de peticion que en este caso es GET, el host que es localhost en el puerto 8081, User-Agent que es curl, el comando por el cual se accedio a la petición y Accept como un \*/\*. Le doy un enter y aparece en la pestaña en el que se uso el comando *curl*, esto:

![Imagen Falso Servidor 3](FalsoServidor3.png)

Al colocar `curl -i 'http://randomword.saasbook.info/'`se obtiene esto :

![Imagen Encabezados y Cuerpo](EncabezadoCuerpo.png)

El código de respuesta en este caso es de 200 lo cual indica que la solicitud ha tenido exito. La version de HTTP es la 1.1.

En el encabezado hay un campo Content-Type, que en este caso y en la mayoria de sitios web aparece **text/html** por lo que son archivos de texto HTML, codificados mediante **charset=utf-8**

## ¿Qué sucede cuando falla un HTTP request?



