**1. Realiza una exportación del esquema de SCOTT usando la consola Enterprise Manager, con las siguientes condiciones:**

* Exporta tanto la estructura de las tablas como los datos de las mismas.
* Excluye de la tabla EMP los empleados que no tienen comisión.
* Programa la operación para dentro de 10 minutos.
* Genera un archivo de log en el directorio que consideres más oportuno.

Realiza ahora la operación con **Oracle Data Pump**.

**2. Importa el fichero obtenido anteriormente usando Enterprise Manager pero en un usuario distinto de otra base de datos.**

**3. Realiza una exportación de la estructura de todas las tablas de la base de datos usando el comando expdp de Oracle Data Pump utilizando un DBLink desde otra base de datos. Prueba todas las posibles opciones que ofrece dicho comando y documentándolas adecuadamente.**

**4. Intenta realizar operaciones similares de importación y exportación con una herramienta gráfica de administración de MySQL, documentando el proceso.**
Para realizar esto, vamos a utilizar la herramienta web [phpmyadmin](https://sql.luis.gonzalonazareno.org/) que utilizamos para la práctica de **hosting**. Después de introducir un usuario y una contraseña, tendremos que dirigirnos a la pestaña que nos indica **export**. Seleccionamos el lenguaje, en este caso **SQL**, y luego elegimos el método **custom**, para poder escoger qué base de datos exportaremos.
![](/images/1.png)
Entre las diversas opciones que vemos en pantalla, podremos escoger algunas como exportar _solo_ la _estructura_, solo las _tablas_, todo, _máxima longitud_ de los _registros_, etc. Una vez que hayamos terminado, pulsamos el último botón (**Go**) y automáticamente comenzará una descarga de un fichero **.sql** con toda la información que hayamos seleccionado.
![](/images/2.png)
En realidad, esto básicamente ejecuta el comando mysqldump por debajo, con los parámetros correspondientes.
En el caso de que queramos hacer una importación nos dirigimos a la pestaña import y tan solo tendremos que subir un fichero con el formato que nos indica (<**formSQL**>.[<**formCompresión**>]). Después elegimos la codificación de caracteres que tiene el texto del fichero y pulsamos **_Go_**.
![](/images/3.png)

**5. Exporta todos los documentos de las colecciones de MongoDB que tengan más de cuatro documentos e impórtalos en otra base de datos .**
Antes de nada voy a crear varias colecciones y voy a darles contenido. Crearé una con más de cuatro documentos y las demás con uno o dos documentos con el siguiente [codigo](/docs/mongo-query.json)
