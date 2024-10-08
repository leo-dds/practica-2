https://github.com/leo-dds/practica-2.git

1. No tengo ninguna imagen de httpd, la descargo con docker pull httpd.

 2. Creo el contenedor con docker run *-d --name asir_httpd -p 8080:80 httpd*

3. Mapea o porto 80 do contenedor 8080 *docker run -d --name asir_httpd -p 8080:80 -v "$PWD"/htdocs:/usr/local/apache2/htdocs/ httpd*

4. Comprobamos que a paxina esta en funcionamiento con *http://localhost:8080* no noso navegador.

5. Creamos un conatenedor con *docker run -d --name asir_web1 -p 8000:80 -v "$PWD"/htdocs:/usr/local/apache2/htdocs/ httpd*

6. Creamos outo contenedor con  *docker run -d --name asir_web2 -p 8090:80 -v "$PWD"/htdocs:/usr/local/apache2/htdocs/ httpd*

7. Comprobamos con *http://localhost:8000* *http://localhost:8090*

