# MySQL


|| HISTORIA





|| VERSIONES 





|| CARACTERÍSTICAS






|| INSTALAR Y EJECUTAR 
	
	OS: 

		Instalar el paquete que proporciona el sistema operativo para el administrador DB (PostgreSQL, MySQL, SQLite3, etc.) 

		Después de la instalación se inicia automáticamente, si no lo hace, ingresamos un comando para verificar su estado o iniciarlo manualmente. Tambien podemos habilitarlo para que se inicie con el arranque del sistema. 

		Accedemos al administrador con su comando correspondiente y trabajamos desde aquí con la base de datos.  


		Debian/Ubuntu: 

			Actualizar paquetes y sistema: 

			```
				sudo apt update		
				sudo apt upgrade		
			```

			Instalar administrador DB:

			```
				sudo apt install mysql-server

			```	

			Verificar estado del administrador DB

			```
				sudo systemctl status mysql

			```

			Inicio manual: 

			```
				sudo systemctl start mysql

			```

			Inicio con el sistema: 

			```
				sudo systemctl enable mysql

			```

			Acceder y trabajar con el administrador DB:

			```
				sudo mysql -u root -p

			```


	IDLE: 

		Instalar y ejecutar MySQL directamente en un editor de código como Visual Studio Code o Sublime Text no es una práctica común, ya que estos editores están diseñados principalmente para la edición de código y no para la ejecución de servidores de bases de datos. 

		Sin embargo, puedes utilizar estos editores de código para escribir y ejecutar consultas SQL y conectarte a servidores MySQL existentes.

		Una vez que hayas instalado la extensión, deberás configurar la conexión a tu servidor MySQL. 

		Esto generalmente implica proporcionar la dirección IP o el nombre del host del servidor, el puerto, el nombre de usuario y la contraseña.


	DB GUI: 

		Están enfocadas en dibujar diagramas, hacer declaraciones, diseñar, modelar, generar y administrar bases de datos visualmente. 

		Pueden incluir un modelador de datos para crear modelos ER complejos, ingeniería directa e inversa, y también ofrece funciones clave para realizar tareas difíciles de gestión de cambios y documentación que normalmente requieren mucho tiempo y esfuerzo.




|| CHEAT SHEET 
	
	Son ejemplos de código aplicado usados para tener una referencia rápida y resumida que proporciona una lista de comandos y funciones esenciales de MySQL junto con sus sintaxis básicas. 

	Estas hojas de trucos son útiles para los desarrolladores y administradores de bases de datos que trabajan con MySQL, ya que les permiten consultar rápidamente los comandos y funciones más comunes sin tener que buscar en la documentación completa cada vez que necesitan realizar una tarea específica.


	Un "Cheat Sheet" de MySQL generalmente incluirá información sobre:

   		Comandos SQL: 

   			Incluyendo comandos para crear, modificar, consultar y eliminar bases de datos, tablas y registros.


	    Funciones de MySQL: 

	    	Una lista de funciones incorporadas de MySQL, como funciones matemáticas, de cadena, de fecha y hora, y funciones de agregación.


	    Operadores: 

	    	Los operadores utilizados en las consultas SQL, como operadores de comparación, operadores lógicos y operadores aritméticos.


	    Instrucciones de control:

	    	Incluyendo instrucciones como IF, CASE, y WHILE que se utilizan en procedimientos almacenados y desencadenadores (triggers).


	    Instrucciones de administración: 

	    	Instrucciones para gestionar usuarios, privilegios y la configuración del servidor MySQL.


	Estos "Cheat Sheets" suelen estar diseñados de manera concisa y organizados de forma que sean fáciles de leer y comprender rápidamente. Pueden ser útiles tanto para principiantes que están aprendiendo MySQL como para profesionales con experiencia que desean tener a mano una referencia rápida de comandos y funciones comunes.



|| TIPOS DE DATOS 

	Tipo de Datos (Data Type): 

	    Define el tipo de datos que puede almacenarse en una columna, como INTEGER (entero), VARCHAR (cadena de caracteres), DATE (fecha), etc. 

	    El tipo de datos especifica la naturaleza de los valores que se pueden almacenar en la columna.


    Longitud (Length): 

    	Para columnas de tipo VARCHAR o CHAR, la longitud especifica la cantidad máxima de caracteres que pueden almacenarse en la columna.


    Clave Primaria (Primary Key): 

    	Puedes definir una columna como clave primaria, lo que garantiza que sus valores sean únicos en la tabla y permite una identificación única de cada fila.


    Clave Externa (Foreign Key): 

    	Una columna puede definirse como clave externa (foreign key) para establecer una relación con otra tabla. 

    	Esto asegura la integridad referencial y permite referencias cruzadas entre tablas.


    Valores Predeterminados (Default Values): 

    	Puedes especificar un valor predeterminado que se utilizará si no se proporciona ningún valor al insertar una fila en la tabla.


    Restricciones de Nulidad (NULL Constraints): 

    	Puedes indicar si una columna permite o no valores nulos (NULL). 

    	Si se prohíben los valores nulos, cada fila debe tener un valor válido en esa columna.


    Autoincremento (Auto-Increment):

    	Para columnas numéricas, como INTEGER, puedes habilitar la propiedad de autoincremento, lo que hace que la columna se incremente automáticamente con cada nueva fila insertada en la tabla.


    Comentarios (Comments): 

    	Puedes agregar comentarios a una columna para documentar su propósito o su uso.


    Índices (Indexes): 

    	Puedes crear índices en una columna para mejorar el rendimiento de las consultas.

    	Los índices aceleran la búsqueda de registros basándose en los valores de esa columna.


    Validaciones (Check Constraints):

    	Puedes definir restricciones adicionales en una columna utilizando la cláusula CHECK para garantizar que los valores cumplan ciertos criterios.


    Único (Unique Constraint): 

    	Puedes hacer que los valores en una columna sean únicos en la tabla, lo que impide la duplicación de datos.



|| SINTAXIS BÁSICA 

	Son operaciones esenciales en una base de datos MySQL, como crear tablas, insertar datos, consultar datos y realizar actualizaciones. 


	Crear Base de Datos: 

		```sql

			CREATE DATABASE nombre_de_la_base_de_datos;

		```


	Seleccionar una Base de Datos:

		```sql

			USE nombre_de_la_base_de_datos;

		```


	Crear una tabla: 

		```sql

			CREATE TABLE nombre_de_la_tabla (
			    columna1 tipo_de_dato,
			    columna2 tipo_de_dato,
			    ...
			);

		```


	Insertar Datos en la tabla: 

		```sql

			INSERT INTO nombre_de_la_tabla (columna1, columna2, ...)
			VALUES (valor1, valor2, ...);

		```


	Consultar datos en una tabla: 

		```sql

			SELECT columna1, columna2
			FROM nombre_de_la_tabla
			WHERE condición;

		```


	Actualizar datos de una tabla: 

		```sql

			UPDATE nombre_de_la_tabla
			SET columna1 = nuevo_valor1, columna2 = nuevo_valor2
			WHERE condición;

		```


	Eliminar datos de una tabla: 

		```sql

			DELETE FROM nombre_de_la_tabla
			WHERE condición;

		```


	Eliminar tabla de una Base de Datos: 

		```sql

			DROP TABLE nombre_de_la_tabla;

		```


	Eliminar Base de Datos: 

		```sql

			DROP DATABASE nombre_de_la_base_de_datos;

		```


	Crear User: 

		```sql

			CREATE USER 'nombre_de_usuario'@'localhost' IDENTIFIED BY 'contraseña';

		```


	Conceder privilegios a un User: 

		```sql

			GRANT privilegio ON nombre_de_la_base_de_datos.* TO 'nombre_de_usuario'@'localhost';

		```


	Revocar privilegios a un User: 

		```sql

			REVOKE privilegio ON nombre_de_la_base_de_datos.* FROM 'nombre_de_usuario'@'localhost';

		```



|| PROYECTO BÁSICO
	
	Implica la creación de una base de datos, una tabla y algunas operaciones básicas.

	Objetivo: 

		Crear una base de datos para gestionar una lista de tareas pendientes.


	1. Crear Base de Datos: 

		```sql

			CREATE DATABASE lista_de_tareas;

		```


	2. Seleccionar Base de datos: 	

		```sql 

			USE lista_de_tareas;

		```

		USE permite trabajar dentro de la base de datos "lista_de_tareas"


	3. Crear tabla para nuestro objetivo: 

		```sql 

			CREATE TABLE tareas (
			    tarea_id INT AUTO_INCREMENT PRIMARY KEY,
			    descripcion VARCHAR(255) NOT NULL,
			    fecha_limite DATE,
			    completada BOOLEAN DEFAULT FALSE
			);

		```	

		Crea una tabla llamada "tareas" con las siguientes columnas:

		    tarea_id: 

		    	Identificador único de la tarea (clave primaria).


		    descripcion: 

		    	Descripción de la tarea (cadena de texto).


		    fecha_limite: 

		    	Fecha límite de la tarea (fecha).


		    completada: 

		    	Estado de la tarea (verdadero o falso).


	4. Insertar Tareas en la tabla: 	
		Puedes insertar tareas individuales en la tabla de la siguiente manera:

		```sql 

			INSERT INTO tareas (descripcion, fecha_limite)
			VALUES
			    ('Hacer la compra', '2023-09-20'),
			    ('Preparar informe', '2023-09-25'),
			    ('Enviar correo electrónico', NULL);

		```


	5. Consultar tareas pendientes: 	
		```sql

			SELECT * FROM tareas WHERE completada = FALSE;

		```


	6. Actualizar el Estado de una Tarea:

		Puedes marcar una tarea como completada de la siguiente manera:

		```sql

			UPDATE tareas SET completada = TRUE WHERE tarea_id = 1;

		```


	7. Eliminar una Tarea:

		Puedes eliminar una tarea de la tabla de la siguiente manera:	

		```sql

			DELETE FROM tareas WHERE tarea_id = 2;

		```

	Puedes personalizarlo según tus necesidades y expandirlo agregando más funcionalidades, como la capacidad de agregar usuarios, asignar tareas a personas, agregar etiquetas a las tareas, etc.	



|| CONECTAR LA BASE DE DATOS A UN PROYECTO
	
	Implica establecer una comunicación entre la base de datos y la aplicación o programa que estás desarrollando. 

	Esto permite que la aplicación acceda y manipule los datos almacenados en la base de datos.

	La forma en que se realiza esta conexión puede variar según el lenguaje de programación y la tecnología que estés utilizando.

	Siempre es importante seguir las prácticas recomendadas de seguridad, como evitar la inyección de SQL, al interactuar con una base de datos desde tu aplicación.


	1. Instalar el Sistema de Gestión de Bases de Datos (DBMS):

    	Antes de poder conectarte a una base de datos, debes asegurarte de que el sistema de gestión de bases de datos (DBMS) correspondiente esté instalado en tu servidor o en tu máquina local. 

    	Ejemplos de DBMS populares incluyen MySQL, PostgreSQL, SQLite, SQL Server y Oracle.


	2. Crear una Base de Datos:

   		Utiliza el DBMS para crear una base de datos si aún no existe. 

   		Esto implica definir la estructura de la base de datos, incluyendo tablas, columnas y relaciones.


	3. Configurar la Conexión:

    	En tu proyecto de programación, generalmente debes configurar la conexión a la base de datos. 

    	Esto incluye proporcionar detalles como la dirección del servidor de la base de datos, el nombre de usuario, la contraseña y el nombre de la base de datos que deseas utilizar.


	4. Importar una Biblioteca o Controlador:

    	Dependiendo del lenguaje de programación que estés utilizando, es posible que necesites importar una biblioteca o un controlador específico que permita la comunicación con la base de datos. 

    	Por ejemplo, en PHP, puedes utilizar la biblioteca mysqli o PDO para interactuar con MySQL.


	Paso 5: Establecer una Conexión:

    	Utiliza la biblioteca o el controlador importado para establecer una conexión a la base de datos. 

    	Esto generalmente se hace proporcionando los detalles de conexión que configuraste anteriormente.


	6. Realizar Consultas y Operaciones:

    	Una vez que la conexión esté establecida, puedes ejecutar consultas SQL y realizar operaciones en la base de datos. 

    	Puedes insertar, actualizar, eliminar y seleccionar datos según sea necesario.


	7. Cerrar la Conexión (Opcional):

    	Para liberar recursos, es una buena práctica cerrar la conexión a la base de datos cuando hayas terminado de usarla.


    PHP: 

    	Conectar y realizar una consulta básica en una base de datos MySQL:


		```php

			<?php
			// Configurar la conexión
			$servername = "localhost";
			$username = "usuario";
			$password = "contraseña";
			$dbname = "basededatos";

			// Crear una conexión
			$conn = new mysqli($servername, $username, $password, $dbname);

			// Verificar la conexión
			if ($conn->connect_error) {
			    die("Error de conexión: " . $conn->connect_error);
			}

			// Ejecutar una consulta
			$sql = "SELECT nombre, correo FROM usuarios";
			$result = $conn->query($sql);

			// Procesar los resultados
			if ($result->num_rows > 0) {
			    while($row = $result->fetch_assoc()) {
			        echo "Nombre: " . $row["nombre"]. " - Correo: " . $row["correo"]. "<br>";
			    }
			} else {
			    echo "No se encontraron resultados";
			}

			// Cerrar la conexión
			$conn->close();
			?>

		```


	Python: 

		Utilizaremos el módulo mysql-connector-python, que es una biblioteca popular para interactuar con bases de datos MySQL en Python


		1. Instalar el Módulo mysql-connector-python:
			
			Asegúrate de tener Python instalado en tu sistema. Luego, puedes instalar el módulo mysql-connector-python utilizando pip (el administrador de paquetes de Python):

			```
				pip install mysql-connector-python

			```

		2: Escribir el Código Python:


		```python

			import mysql.connector

			# Configurar la conexión
			config = {
			  'user': 'usuario',
			  'password': 'contraseña',
			  'host': 'localhost',
			  'database': 'basededatos'
			}

			# Conectar a la base de datos
			connection = mysql.connector.connect(**config)

			# Crear un cursor
			cursor = connection.cursor()

			# Ejecutar una consulta SQL
			query = "SELECT nombre, correo FROM usuarios"
			cursor.execute(query)

			# Procesar los resultados
			print("Resultados:")
			for (nombre, correo) in cursor:
			    print(f"Nombre: {nombre} - Correo: {correo}")

			# Cerrar el cursor y la conexión
			cursor.close()
			connection.close()

		```


	JavaScript/Node.js: 

		Conectar y realizar una consulta básica en una base de datos MySQL utilizando JavaScript con el entorno Node.js y el módulo "mysql2", que es una popular biblioteca para interactuar con bases de datos MySQL en Node.js:


		1. Instalar el Módulo "mysql2":

			Asegúrate de tener Node.js instalado en tu sistema. 

			Luego, puedes instalar el módulo "mysql2" utilizando npm (el administrador de paquetes de Node.js):

			```
				npm install mysql2

			```


		2. Escribir el Código JavaScript:
			
			Luego, puedes escribir el código JavaScript para conectar y consultar la base de datos MySQL


		```js 

			const mysql = require('mysql2');

			// Configurar la conexión
			const connection = mysql.createConnection({
			  host: 'localhost',
			  user: 'usuario',
			  password: 'contraseña',
			  database: 'basededatos'
			});

			// Conectar a la base de datos
			connection.connect(function(err) {
			  if (err) {
			    console.error('Error de conexión: ' + err.stack);
			    return;
			  }

			  console.log('Conexión exitosa como ID ' + connection.threadId);

			  // Ejecutar una consulta SQL
			  connection.query('SELECT nombre, correo FROM usuarios', function(err, results) {
			    if (err) {
			      console.error('Error al ejecutar la consulta: ' + err.stack);
			      return;
			    }

			    // Procesar los resultados
			    console.log('Resultados:');
			    for (const row of results) {
			      console.log(`Nombre: ${row.nombre} - Correo: ${row.correo}`);
			    }

			    // Cerrar la conexión
			    connection.end(function(err) {
			      if (err) {
			        console.error('Error al cerrar la conexión: ' + err.stack);
			        return;
			      }
			      console.log('Conexión cerrada');
			    });
			  });
			});

		```

		En 'localhost', 'usuario', 'contraseña', 'basededatos' van los valores de tu base de datos MySQL.


	Inyección SQL: 

		Es un tipo de ataque informático que se produce cuando un atacante introduce intencionadamente instrucciones SQL maliciosas en una aplicación o sistema que no valida adecuadamente los datos de entrada. 

		Este ataque se aprovecha de la falta de seguridad en la validación de datos y puede permitir al atacante acceder, modificar o eliminar datos en una base de datos, así como llevar a cabo otras acciones no autorizadas en el sistema.

		Por ejemplo, si en una aplicación web que tiene un formulario de inicio de sesión donde los usuarios ingresan su nombre de usuario y contraseña. 

		La aplicación utiliza una consulta SQL para verificar si el nombre de usuario y la contraseña ingresados coinciden en la base de datos:

		```sql

			SELECT * FROM usuarios WHERE nombre_usuario = 'usuario' AND contraseña = 'contraseña';

		```

		Si la aplicación no valida adecuadamente la entrada del usuario y un atacante ingresa lo siguiente en el campo de nombre de usuario:

		```
			' OR '1'='1

		```

		La consulta SQL resultante se verá de la siguiente manera:

		```sql

			SELECT * FROM usuarios WHERE nombre_usuario = '' OR '1'='1' AND contraseña = 'contraseña';

		```

		La condición '1'='1' siempre será verdadera, lo que significa que la consulta devolverá todos los registros de usuarios, permitiendo al atacante iniciar sesión sin conocer la contraseña correcta.


	Para prevenir la Inyección SQL, es fundamental seguir buenas prácticas de seguridad:


	    Validación de Entrada: 

	    	Valida y filtra cuidadosamente todas las entradas de usuario y otros datos antes de usarlos en consultas SQL.

	    	Utiliza funciones como "prepared statements" y "parameterized queries" para evitar la concatenación directa de datos de usuario en consultas SQL.


	    Escape de Caracteres Especiales: 

	    	Si no puedes utilizar "prepared statements", asegúrate de escapar (sanitizar) correctamente los caracteres especiales en las entradas de usuario para evitar que sean interpretados como instrucciones SQL.


	    Principio de Menor Privilegio: 

	    	Asegúrate de que las cuentas de usuario y las conexiones de bases de datos tengan solo los permisos necesarios. 

	    	No utilices cuentas de superusuario para operaciones normales.


	    Actualizaciones y Parches: 

	    	Mantén tu software y sistemas actualizados con los últimos parches de seguridad para mitigar vulnerabilidades conocidas.


	    Auditoría y Registros:

	    	Registra y supervisa las actividades de la base de datos para detectar cualquier actividad sospechosa o intentos de Inyección SQL.


	Situaciones de entrada de datos no validadas: 	

		Formularios Web: 

			Las aplicaciones web a menudo permiten a los usuarios enviar datos a través de formularios en línea.

			Si no se aplican medidas de validación en el lado del servidor para asegurarse de que los datos ingresados sean seguros y cumplan con las expectativas, la entrada del usuario podría ser vulnerable a la Inyección SQL.

			Esto es especialmente cierto cuando se realizan consultas SQL directamente con los datos proporcionados por el usuario.


	    URLs y Parámetros de Consulta: 

	    	Algunas aplicaciones utilizan información proporcionada por el usuario en URLs o parámetros de consulta. 

	    	Si esta información no se valida adecuadamente, un atacante podría manipular los parámetros de la URL para ejecutar ataques de Inyección SQL.


	    Entrada de Datos de Forma Libre: 

	    	Cuando los usuarios pueden ingresar datos de forma libre en campos de texto o áreas de comentarios, es importante validar y escapar adecuadamente los datos antes de almacenarlos o mostrarlos. 

	    	Los ataques de Inyección SQL pueden ocurrir si el usuario introduce intencionadamente comandos maliciosos.


	    Autenticación y Autorización: 	

	    	Los sistemas de autenticación y autorización deben validar las credenciales de los usuarios de manera segura. 

	    	Si no se validan adecuadamente, los atacantes pueden aprovechar las debilidades para eludir la autenticación o ganar acceso no autorizado.


	    Servicios Web y APIs: 

	    	Los servicios web y las APIs pueden ser puntos de entrada para ataques de Inyección SQL si no validan y filtran correctamente las solicitudes y parámetros proporcionados por el usuario.


	    Archivos Adjuntos: 

	    	Si una aplicación permite a los usuarios cargar archivos, es importante validar y filtrar los tipos de archivos permitidos para evitar que se carguen archivos maliciosos que puedan explotar vulnerabilidades de Inyección SQL.


	    Conexiones de Bases de Datos Inseguras: 

	    	Si una aplicación se conecta a la base de datos utilizando cuentas de usuario con privilegios excesivos (como el acceso de escritura completa), un atacante podría explotar vulnerabilidades de Inyección SQL para modificar, eliminar o acceder a datos sensibles.


	Validar y filtrar adecuadamente la entrada del usuario:


		Utilizando "Prepared Statements":

			En lugar de concatenar directamente los valores del usuario en una consulta SQL, puedes utilizar "prepared statements" para separar los datos de la consulta.

		```php

			// Conexión a la base de datos
			$conexion = new mysqli('localhost', 'usuario', 'contraseña', 'basededatos');

			// Verificación de la conexión
			if ($conexion->connect_error) {
			    die("Error de conexión: " . $conexion->connect_error);
			}

			// Datos del usuario
			$nombre_usuario = $_POST['nombre_usuario'];
			$contraseña = $_POST['contraseña'];

			// Consulta preparada
			$stmt = $conexion->prepare("SELECT * FROM usuarios WHERE nombre_usuario = ? AND contraseña = ?");
			$stmt->bind_param("ss", $nombre_usuario, $contraseña);

			// Ejecutar la consulta
			$stmt->execute();

			// Procesar el resultado
			$resultado = $stmt->get_result();

			if ($resultado->num_rows === 1) {
			    // Usuario autenticado correctamente
			} else {
			    // Usuario no encontrado o autenticación fallida
			}

			// Cerrar la conexión
			$stmt->close();
			$conexion->close();

		```

		Utilizamos "prepared statements" para separar los valores del usuario de la consulta SQL, lo que evita la posibilidad de Inyección SQL.


		Escapar los Datos del Usuario:

			Si no puedes usar "prepared statements", debes escapar adecuadamente los datos del usuario antes de usarlos en una consulta SQL. Aquí tienes un ejemplo:	

		```php

			// Conexión a la base de datos
			$conexion = new mysqli('localhost', 'usuario', 'contraseña', 'basededatos');

			// Verificación de la conexión
			if ($conexion->connect_error) {
			    die("Error de conexión: " . $conexion->connect_error);
			}

			// Datos del usuario
			$nombre_usuario = $_POST['nombre_usuario'];
			$contraseña = $_POST['contraseña'];

			// Escapar los datos del usuario
			$nombre_usuario = $conexion->real_escape_string($nombre_usuario);
			$contraseña = $conexion->real_escape_string($contraseña);

			// Consulta SQL segura
			$sql = "SELECT * FROM usuarios WHERE nombre_usuario = '$nombre_usuario' AND contraseña = '$contraseña'";

			// Ejecutar la consulta
			$resultado = $conexion->query($sql);

			if ($resultado->num_rows === 1) {
			    // Usuario autenticado correctamente
			} else {
			    // Usuario no encontrado o autenticación fallida
			}

			// Cerrar la conexión
			$conexion->close();

		```

		Utilizamos la función real_escape_string() para escapar los datos del usuario antes de concatenarlos en la consulta SQL. 

		Esto previene la Inyección SQL al garantizar que los caracteres especiales se escapen correctamente.

		Recuerda que la mejor práctica es utilizar "prepared statements" siempre que sea posible, ya que ofrecen una mayor seguridad y son menos propensos a errores de seguridad.



|| CHEAT SHEET 


    Comandos SQL: 

    	Incluyendo comandos para crear, modificar, consultar y eliminar bases de datos, tablas y registros.


    Funciones de MySQL: 

    	Una lista de funciones incorporadas de MySQL, como funciones matemáticas, de cadena, de fecha y hora, y funciones de agregación.


    Operadores: 

    	Los operadores utilizados en las consultas SQL, como operadores de comparación, operadores lógicos y operadores aritméticos.


    Instrucciones de control:

    	Incluyendo instrucciones como IF, CASE, y WHILE que se utilizan en procedimientos almacenados y desencadenadores (triggers).


    Instrucciones de administración:

    	Instrucciones para gestionar usuarios, privilegios y la configuración del servidor MySQL.


	Estos "Cheat Sheets" suelen estar diseñados de manera concisa y organizados de forma que sean fáciles de leer y comprender rápidamente. 

	Pueden ser útiles tanto para principiantes que están aprendiendo MySQL como para profesionales con experiencia que desean tener a mano una referencia rápida de comandos y funciones comunes.

	Puedes encontrar "Cheat Sheets" de MySQL en línea o crear uno personalizado que se adapte a tus necesidades específicas. 

	Es una herramienta valiosa para agilizar el trabajo con MySQL y evitar errores al escribir comandos y consultas.


	
|| TIPOS DE INSTRUCCIONES
	

	DDL (Data Definition Language - Lenguaje de Definición de Datos):

	    CREATE DATABASE: 

	    	Crea una nueva base de datos.


	    DROP DATABASE: 

	    	Elimina una base de datos existente.


	    CREATE TABLE: 

	    	Crea una nueva tabla en una base de datos.


	    ALTER TABLE: 

	    	Modifica la estructura de una tabla existente.


	    DROP TABLE: 

	    	Elimina una tabla existente.


	DML (Data Manipulation Language - Lenguaje de Manipulación de Datos):

	    INSERT INTO: 

	    	Agrega nuevos registros a una tabla.


	    SELECT: 

	    	Recupera datos de una o más tablas.


	    UPDATE: 

	    	Modifica datos en una tabla.


	    DELETE FROM: 

	    	Elimina registros de una tabla.


	3. DQL (Data Query Language - Lenguaje de Consulta de Datos):

	    SELECT: 

	    	Consulta datos de una o más tablas utilizando cláusulas como WHERE, ORDER BY, GROUP BY, etc.


	    DISTINCT: 

	    	Recupera valores únicos de una columna.


	    JOIN: 

	    	Combina datos de dos o más tablas basándose en una condición especificada.


	    UNION: 

	    	Combina resultados de dos o más consultas en un solo conjunto de resultados.


	4. DCL (Data Control Language - Lenguaje de Control de Datos):

	    GRANT: 

	    	Concede permisos a usuarios o roles para acceder a objetos de base de datos.


	    REVOKE: 

	    	Revoca permisos previamente otorgados.


	5. TCL (Transaction Control Language - Lenguaje de Control de Transacciones):

	    COMMIT: 

	    	Confirma una transacción y guarda los cambios realizados.


	    ROLLBACK: 

	    	Revierte una transacción no confirmada y deshace los cambios.


	    SAVEPOINT: 

	    	Establece un punto de guardado dentro de una transacción.


	Otros Comandos:

	    USE: 

	    	Selecciona una base de datos específica para trabajar en ella.

	    SHOW:

	    	Muestra información sobre bases de datos, tablas o columnas.


	    DESCRIBE o DESC: 

	    	Proporciona información sobre la estructura de una tabla.


	Instrucciones Condicionales:

	    IF: 

	    	Permite realizar una evaluación condicional y devuelve un valor en función del resultado.


	    CASE: 

	    	Realiza evaluaciones condicionales múltiples y devuelve un valor en función de la primera condición verdadera.


	    CASE WHEN: 

	    	Es una forma más específica de la instrucción CASE que permite definir condiciones y resultados para cada caso.


	Instrucciones de Iteración:

	    WHILE: 

	    	Crea un bucle que se ejecuta mientras se cumple una condición especificada.


	    REPEAT: 

	    	Crea un bucle que se ejecuta hasta que se cumple una condición especificada.


	    LOOP: 

	    	Define un bucle que se ejecuta indefinidamente hasta que se alcance una condición de salida.


	Instrucciones de Manejo de Errores:

	    SIGNAL: 

	    	Genera un error personalizado con un mensaje específico.


	    RESIGNAL: 

	    	Vuelve a lanzar un error que ha sido manejado previamente.


	    GET DIAGNOSTICS: 

	    	Recupera información de diagnóstico después de que se ha producido un error.


	Instrucciones de Control de Transacciones:

	    START TRANSACTION: 

	    	Inicia una transacción explícita.


	    COMMIT: 

	    	Confirma una transacción y guarda los cambios realizados.


	    ROLLBACK: 

	    	Revierte una transacción no confirmada y deshace los cambios.


	    SAVEPOINT: 

	    	Establece un punto de guardado dentro de una transacción.


	Instrucciones de Control de Flujo:

	    LEAVE: 

	    	Sale de un bucle etiquetado.


	    ITERATE: 

	    	Salta a la siguiente iteración de un bucle etiquetado.


	    REPEAT: 

	    	Repite un bucle etiquetado.


	Instrucciones de Control de Código de Bloques:

	    BEGIN: 

	    	Inicia un bloque de código.


	    END: 

	    	Finaliza un bloque de código.


	    DECLARE: 

	    	Declara una variable local dentro de un bloque de código.


	Instrucciones de Control de Manejo de Errores:

	    DECLARE HANDLER: 

	    	Define un manejador de errores personalizado para un tipo específico de error.


	    RESIGNAL: 

	    	Vuelve a lanzar un error que ha sido manejado previamente.



|| OPERADORES


	Operadores Aritméticos:

	    + (Suma): 

	    	Suma dos valores.


	    - (Resta): 

	    	Resta el segundo valor del primero.


	    * (Multiplicación):

	    	Multiplica dos valores.


	    / (División): 	

	    	Divide el primer valor por el segundo.


	    % (Módulo): 

	    	Devuelve el resto de la división del primer valor por el segundo.


	Operadores de Comparación:

	    = (Igual a): 

	    	Compara si dos valores son iguales.


	    != o <> (No igual a): 

	    	Compara si dos valores no son iguales.


	    < (Menor que): 

	    	Compara si el primer valor es menor que el segundo.


	    > (Mayor que): 

	    	Compara si el primer valor es mayor que el segundo.


	    <= (Menor o igual que): 

	    	Compara si el primer valor es menor o igual que el segundo.


	    >= (Mayor o igual que):

	    	Compara si el primer valor es mayor o igual que el segundo.


	Operadores Lógicos:

	    AND (Y): 

	    	Combina dos condiciones y devuelve verdadero si ambas son verdaderas.


	    OR (O): 

	    	Combina dos condiciones y devuelve verdadero si al menos una es verdadera.


	    NOT (NO): 

	    	Invierte el valor de una condición.


	Operadores de Concatenación de Cadenas:

	    CONCAT() (Concatenación):

	    	Combina dos o más cadenas en una sola.


	Operadores de Asignación:

	    = (Asignación): 

	    	Asigna un valor a una variable o columna.


	Operadores de Membresía:

	    IN (En): 

	    	Verifica si un valor está presente en un conjunto de valores.


	    NOT IN (No en): 

	    	Verifica si un valor no está presente en un conjunto de valores.


	Operador de Concatenación de Columnas:

	    || (Doble barra vertical):

	    	Concatena columnas en algunas versiones de MySQL.


	Operadores de Expresión Regular:

	    REGEXP o RLIKE (Coincide con una expresión regular):

	    	Compara un valor con una expresión regular.


	Operador de Espacio de Nombres de Columna:

	    . (Punto): 

	    	Utilizado para hacer referencia a una columna de una tabla en consultas SQL.



|| FUNCIONES INCORPORADAS
	
	    CONCAT(): 

	    	Combina dos o más cadenas.


	    LENGTH(): 

	    	Devuelve la longitud de una cadena.


	    SUBSTRING(): 

	    	Extrae una parte de una cadena.


	    UPPER(): 

	    	Convierte una cadena a mayúsculas.


	    LOWER(): 	

	    	Convierte una cadena a minúsculas.


	    TRIM(): 

	    	Elimina espacios en blanco al principio y al final de una cadena.


	    REPLACE(): 

	    	Reemplaza parte de una cadena con otra.


	Funciones Numéricas (Numeric Functions):

	    SUM(): 

	    	Calcula la suma de valores numéricos.


	    AVG(): 

	    	Calcula el promedio de valores numéricos.


	    MAX(): 

	    	Devuelve el valor máximo en un conjunto de valores.


	    MIN(): 

	    	Devuelve el valor mínimo en un conjunto de valores.


	    ROUND(): 

	    	Redondea un número.


	    ABS(): 

	    	Devuelve el valor absoluto de un número.


	Funciones de Fecha y Hora (Date and Time Functions):

	    NOW(): 

	    	Devuelve la fecha y hora actuales.


	    CURDATE(): 

	    	Devuelve la fecha actual.


	    CURTIME(): 

	    	Devuelve la hora actual.


	    DATE(): 

	    	Extrae la parte de fecha de una fecha y hora.


	    TIME(): 

	    	Extrae la parte de hora de una fecha y hora.


	    DATEDIFF(): 

	    	Calcula la diferencia entre dos fechas.


	    DATE_ADD(): 

	    	Agrega una cantidad de tiempo a una fecha.


	Funciones Matemáticas (Math Functions):

	    SQRT(): 

	    	Calcula la raíz cuadrada de un número.


	    POW(): 

	    	Eleva un número a una potencia.


	    RAND(): 

	    	Genera un número decimal aleatorio.


	    CEIL(): 

	    	Redondea hacia arriba un número decimal.


	    FLOOR(): 

	    	Redondea hacia abajo un número decimal.


	Funciones de Conversión de Tipos (Type Conversion Functions):

	    CAST(): 

	    	Convierte un valor a un tipo de datos específico.


	    CONVERT(): 

	    	Convierte un valor a un tipo de datos específico.


	Funciones de Control de Flujo (Control Flow Functions):

	    IF(): 

	    	Realiza una evaluación condicional y devuelve un valor en función del resultado.


	    CASE WHEN: 

	    	Realiza evaluaciones condicionales múltiples y devuelve un valor en función de la primera condición verdadera.