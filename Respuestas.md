# Respuestas de la Actividad HTTP - Uri

---

## Comando Curl

Del sitio web generador de palabras aleatorias, podemos ver una imagen quese mantiene estática y una palabra que cambia cada vez que cargas la págima.

![Imagen de la página](SitioWeb.png)

Usamos el comando `curl 'http://randomword.saasbook.info/'` en la terminal y muestra como resultado un código HTML

Para guardarlo en un archivo se debe escribir `curl 'http://randomword.saasbook.info/' > PrimerCurl.html` y se creare un archivo HTML con el código que aparecio antes

## Diferencias entre el sitio web y el archivo HTML

Al abrir el archivo HTML en el navegador, la imagen no aparece, a diferencia que al abrir el enlace. Otra diferencia es que al cargarlo nuevamente no cambia la palabra.


