Application Server
******************


****************************
**Tecnologías utilizadas:**
****************************
1. Node JS
	* Node fue el lenguaje decidido por la materia para utilizar para el desarrollo del backend y REST API de la aplicación web. Es un lenguaje totalmente formado por objetos Javascript, tiene las ventajas de la gran cantidad de librerías abiertas que resuelven la mayoría de los problemas con los que un programador se puede encontrar.
	* Debido a la falta de conocimiento del lenguaje no se pudo aprovechar al máximo su potencial y la gran cantidad de refactorizaciones que quedan por hacer harían un código mucho más mantenible. Node tiene un manejo de callbacks igual al de Javascript, que hace muy sencillo manejar las llamadas a DB. Un punto a futuro sería poder aprovechar los callbacks para armar una estructura más modularizada del código.
	* La estructura que quedó hoy en día en la api es:
		* index.js
		* api/ (Contiene los métodos que se comunican con la DB para resolver los pedidos de la REST API)
			* gets.js
			* deletes.js
			* posts.js
			* puts.js
			* extensionsForWebApplication.js (contiene métodos necesarios para la web aplication)
		* querys/ (Son las querys a DB)
			* deletes.js
			* gets.js
			* inserts.js
			* updates.js

2. Angular JS
	* Angular es un framework ampliamente utilizado entre los desarrolladores debido a la facilidad que ofrece para aplicar MVC de forma clara y eficiente.
	* Una gran ventaja que tiene Angular es que los objetos son Javascript puro, lo que hace que la integración con los objetos que provee la api de node sea automática.
	* Decidimos utilizar angular y no jQuery + Bootstrap porque nos permite tener código html mucho más "limpio". Además permite tener un poco de lógica, pero separado de la vista.
	* Un ejemplo del código para ver la limpieza que otorga es el siguiente:
	* >>> <li class="list-item" ng-repeat="item in users">
	Con esa sentencia lo que estoy indicando es que yo desde el controller creo la lista "users" y después el explorador por cada elemento que haya en la lista va a generar el código correspondiente (en este caso un item de una lista).

3. Bootstrap v4 (es un alpha)
	* Bootstrap es un framework que simplifica enormemente el trabajo de desarrollo de front end para no diseñadores. Es una librería con componentes de todo tipo que tiene lo necesario para armar cualquier página común. La ventaja principal es que está diseñado para trabajar de forma responsive, con los distintos tamaños de pantalla y columnas.
	* Se decidió utilizar Bootstrap v4 porque algunas de los nuevos componentes son más amigables para la creación de pantallas para celulares, pero en sí no tiene grandes cambios en el funcionamiento general del framework.
	* Uno de los cambios entre versiones de Bootstrap que se vió plasmado en el desarrollo fue la utilización de la clase Card para la generación de un perfil. Esta clase justamente lo que hace es darle la forma de una carta (titulo, cuerpo y pie), permitiendo tener una visión clara y sencilla del perfil.
	

*************************************************
**Estructura de la Base de datos para usuarios:**
*************************************************
+---------------+---------------+-------------------+----------------------------------+
| **Tabla**     | **Columna**   | **Tipo de dato**  | **Máxima cantidad de caracteres**|
+---------------+---------------+-------------------+----------------------------------+
| Userprofile   | Sex           | Character         |                                  |
+---------------+---------------+-------------------+----------------------------------+
| Userprofile   | Alias         | Character varying | 50                               |
+---------------+---------------+-------------------+----------------------------------+
| Userprofile   | Email         | Character         |                                  |
+---------------+---------------+-------------------+----------------------------------+
| Userprofile   | Name          | Character         | 200                              |
+---------------+---------------+-------------------+----------------------------------+
| Location      | IdUser        | Integer           |                                  |
+---------------+---------------+-------------------+----------------------------------+
| Location      | Latitude      | Numeric           |                                  |
+---------------+---------------+-------------------+----------------------------------+
| Location      | Longitude     | Numeric           |                                  |
+---------------+---------------+-------------------+----------------------------------+
| Interest      | Id            | Integer           |                                  |
+---------------+---------------+-------------------+----------------------------------+
| Interest      | Category      | Character varying | 100                              |
+---------------+---------------+-------------------+----------------------------------+
| Interest      | Value         | Character varying | 100                              |
+---------------+---------------+-------------------+----------------------------------+
| UserInterest  | IdUser        | Integer           |                                  |
+---------------+---------------+-------------------+----------------------------------+
| UserInterest  | IdInterest    | Integer           |                                  |
+---------------+---------------+-------------------+----------------------------------+