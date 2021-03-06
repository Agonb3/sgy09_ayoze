**UT3-A3. Explotando vulnerabilidades con Metasploit Framework VSFTPD y MySQL**

En está práctica simularemos las vulnerabilidades que pueda tener un servidor para explotarlas con nuestro Kali-Linux.
Primero iniciaremos nuestra base de datos de kali con el siguiente comando.

![](./img/1.JPG)

Iniciamos ***msfconsole*** y con el siguiente comando comprobamos los servcios y puertos abiertos.

![](./img/2.JPG)

Si invocamos el comando ***hosts*** nos muestra los hosts que han sido analizados.

![](./img/3.JPG)

Con el comando ***services***, la dirección ip de la víctima y el puerto, podemos ver el estado de un servcio en concreto.

![](./img/5.JPG)

Vamos a intentar acceder a la base de datos mediante el puerto que hemos encontrado abierto.

![](./img/6.JPG)

Una vez dentro vamos a ver que bases de datos hay disponibles.

![](./img/7.JPG)

Ahora buscaremos en las distintas bases de datos hasta encontrar información valiosa.

![](./img/8.JPG)

Como podemos ver en una simple busqueda hemos encontrado nombres de usuario con sus repectivas tarjetas de crédito.

![](./img/9.JPG)

Ahora intentaremos acceder a la consola del servidor mediante el protocolo ***ftp*** en el puerto ***21*** que previamente hemos visto abierto. Para ello buscaremos la vulneravilidad en nuestra base de datos con el siguiente comando.

![](./img/10.JPG)

Para iniciarlo tan solo debemos hacer uso del comando ***use*** seguido del nombre del exploit que hemos identificado en el paso anterior e introducimos el host de destino.

![](./img/11.JPG)

Con ***run*** iniciamos el proceso y ya estamos dentro de la consola del servidor con privilegios de root.

![](./img/13.JPG)
