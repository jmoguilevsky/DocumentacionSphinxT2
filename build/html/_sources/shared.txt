Shared Server
**************

****************************
**Tecnologías utilizadas:**
****************************
Tecnologías para Front-end:
===========================

1. Angular JS
	* Angular es un framework ampliamente utilizado entre los desarrolladores debido a la facilidad que ofrece para aplicar MVC de forma clara y eficiente.
	* Una gran ventaja que tiene Angular es que los objetos son Javascript puro, lo que hace que la integración con los objetos que provee la api de node sea automática.
	* Decidimos utilizar angular y no jQuery + Bootstrap porque nos permite tener código html mucho más "limpio". Además permite tener un poco de lógica, pero separado de la vista.
	* Un ejemplo del código para ver la limpieza que otorga es el siguiente:
	* >>> <li class="list-item" ng-repeat="item in users">
	Con esa sentencia lo que estoy indicando es que yo desde el controller creo la lista "users" y después el explorador por cada elemento que haya en la lista va a generar el código correspondiente (en este caso un item de una lista).
2. Node JS
   

***********************************
**Estructura de la Base de datos:**
***********************************
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