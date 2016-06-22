Android Application
*******************


****************************
**Tecnologías utilizadas:**
****************************
1. Volley
	* Volley es una biblioteca de HTTP que hace más fácil y más rápido el manejo de requests para aplicaciones de Android.
	* Utilizamos Volley para el manejo de los requests entre el Android y el Application Server.

2. SQLite
	* SQLite es una base de datos muy simple que se maneja con un archivo físico pero permite realizar transacciones sobre el mismo.
	* Utilizamos SQLite para guardar información del usuario, dado que se crea rápido y es fácil para utilizar y trae todas las ventajas que de tener los datos guardados en forma de DB.
	* En la DB solo tenemos guardado los datos del usuario logueado, cuando se loguea se lo guarda y cuando se desloguea se elimina su información.
	* La estructura es muy simple con una única tabla con los siguientes campos:
	
+---------------+----------------------+
| **Campo**     | **Tipo de Dato**     |
+---------------+----------------------+
| ID            | Integer (Primary key)|
+---------------+----------------------+
| Alias         | Text                 |
+---------------+----------------------+
| Email         | Text Unique          |
+---------------+----------------------+
| Name          | Text                 |
+---------------+----------------------+
| Gender        | Text                 |
+---------------+----------------------+
| Interests     | Text                 |
+---------------+----------------------+
| Photo         | Text                 |
+---------------+----------------------+
| Location      | Text                 |
+---------------+----------------------+
| Token         | Text                 |
+---------------+----------------------+