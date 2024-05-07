# MongoDB


	Es una base de datos NoSQL (no solo SQL) que se utiliza para el almacenamiento de datos de manera eficiente y escalable.


	Origen: 

		Fue desarrollado por la compañía 10gen en 2007 y lanzado en 2009 como software de código abierto. 

		10gen luego cambió su nombre a MongoDB Inc. en 2013. 

		La idea principal detrás de MongoDB era crear una base de datos que pudiera gestionar datos no estructurados o semiestructurados de manera más eficiente que las bases de datos relacionales tradicionales.


	Propósito: 	

		Diseñado para abordar los desafíos que presentan los datos no estructurados, semiestructurados y poliestructurados. 

		Su propósito principal es proporcionar una base de datos flexible y escalable que pueda manejar grandes volúmenes de datos con facilidad y eficiencia. 

		MongoDB es conocido por su capacidad para gestionar datos de tipo documento y por su arquitectura distribuida que permite una fácil escalabilidad horizontal.



|| Base de datos no estructurados
	
	Los datos no se almacenan en tablas relacionales con filas y columnas predefinidas como en una base de datos relacional tradicional. 

	Los datos se almacenan de forma más flexible, lo que permite la manipulación y el almacenamiento de datos de una manera más libre y menos rígida.

	Los datos en una base de datos no estructurada pueden ser de diferentes tipos y tamaños, y no necesariamente tienen que cumplir con un esquema definido de antemano. 

	Estos datos pueden ser de diferentes formatos, como texto, documentos, imágenes, videos, datos geoespaciales, datos de series temporales, entre otros.

	Algunos ejemplos de bases de datos no estructuradas son las bases de datos de documentos, como MongoDB, que almacenan datos en forma de documentos, o las bases de datos de clave-valor, como Redis, donde los datos se almacenan en pares clave-valor.

	La flexibilidad en el almacenamiento de datos no estructurados permite a las empresas gestionar datos complejos y variados sin la necesidad de definir un esquema rígido, lo que resulta útil en situaciones en las que los datos pueden variar en su estructura o formato, o cuando se necesita una mayor escalabilidad y agilidad en el manejo de grandes volúmenes de datos.



|| Versiones

    Versión 1.0 (2009): 

    	Fue la primera versión estable de MongoDB.

    	Incluyó muchas de las características básicas de MongoDB que se mantienen hasta la actualidad, como el almacenamiento de documentos y la replicación maestro-esclavo.


    Versión 2.0 (2011): 

    	Introdujo características importantes como la indexación de texto completo y la agrupación.


    Versión 2.2 (2012): 

    	Incluyó la agregación basada en el marco de procesamiento de datos, lo que permitió a los usuarios realizar operaciones de agregación similares a las operaciones 'SQL GROUP BY'.


    Versión 2.4 (2013): 

    	Presentó mejoras significativas en la administración y la seguridad, incluida la autenticación basada en roles.


    Versión 2.6 (2014): 

    	Introdujo un lenguaje de consulta mejorado, mejoras en la administración y en la seguridad, y la compresión de datos en el almacenamiento.


    Versión 3.0 (2015): 	

    	Introdujo la opción de almacenamiento basado en cableado, mejoras en la seguridad y la capacidad de hacer consultas de texto completo en múltiples idiomas.


    Versión 3.2 (2015): 

    	Agregó características como la encriptación de datos en reposo y una mejora en las operaciones de agregación.


    Versión 3.4 (2016): 

    	Introdujo características como vistas y políticas de retención de documentos.


    Versión 3.6 (2017): 

    	Presentó mejoras en la consulta y la indexación, así como la capacidad de realizar transacciones distribuidas.


    Versión 4.0 (2018): 

    	Incluyó mejoras en la escalabilidad y el rendimiento, así como la incorporación de ACID (Atomicidad, Consistencia, Aislamiento, Durabilidad) en transacciones de varios documentos.


    Versión 4.2 (2019): 

    	Agregó características como la búsqueda en texto completo en varias palabras y mejoras en la escalabilidad y la seguridad.


    Versión 4.4 (2020): 

    	Introdujo nuevas características como los registros de auditoría en tiempo real y la encriptación de campos.



|| Características

	MongoDB ofrece varias características que lo hacen popular y adecuado para una variedad de aplicaciones y casos de uso.


	Modelo de datos flexible: 

		MongoDB utiliza un modelo de datos basado en documentos que permite el almacenamiento de datos flexibles y dinámicos. 

		Los documentos pueden contener arreglos, subdocumentos y valores anidados, lo que proporciona una gran flexibilidad en el diseño de esquemas y facilita la representación de relaciones jerárquicas.


	Escalabilidad horizontal: 	

		MongoDB se puede escalar de manera eficiente y sencilla en entornos distribuidos a través de la adición de más nodos, lo que permite un manejo efectivo de grandes volúmenes de datos y cargas de trabajo crecientes.


	Consultas potentes y flexibles:

		Ofrece un lenguaje de consulta rico que permite a los usuarios realizar consultas complejas y operaciones de agregación de datos. 

		También admite consultas geoespaciales para aplicaciones que requieren funcionalidades basadas en la ubicación.


	Alta disponibilidad y tolerancia a fallos: 

		MongoDB proporciona características de replicación y fragmentación automática que garantizan la disponibilidad de datos y la resistencia a fallos en entornos distribuidos.


	Indexación eficiente: 

		Permite la creación de índices secundarios para un acceso rápido y eficiente a los datos, lo que mejora el rendimiento de las consultas y la velocidad de recuperación de información.


	Ad hoc queries: 

		Los usuarios pueden realizar consultas ad hoc para buscar datos utilizando un lenguaje de consulta dinámico y expresivo.


	Administración de datos distribuidos: 

		MongoDB facilita la administración de datos distribuidos y la implementación de infraestructuras de bases de datos en múltiples ubicaciones geográficas.


	Soporte para datos geoespaciales:

		Proporciona funcionalidades integradas para trabajar con datos geoespaciales y realizar consultas espaciales en datos basados en la ubicación.


	Transacciones ACID: 	

		A partir de la versión 4.0, MongoDB ofrece compatibilidad con transacciones ACID para aplicaciones que requieren operaciones de escritura en varias colecciones o documentos de manera atómica, consistente, aislada y duradera.	



|| ACID

	Conjunto de propiedades que se utilizan para garantizar que las transacciones de una base de datos se realicen de manera fiable.

	Estas propiedades son clave para garantizar la integridad de los datos en situaciones en las que múltiples operaciones deben realizarse de manera coherente y segura. 


    Atomicidad (Atomicity): 

    	Significa que una transacción se trata como una operación única e indivisible. 

    	Esto implica que o bien todas las operaciones de la transacción se realizan con éxito y se confirman, o si ocurre un error en alguna parte de la transacción, se realiza un rollback de todas las operaciones y se restaura el estado original de la base de datos.


    Consistencia (Consistency):

    	Garantiza que la base de datos pase de un estado válido a otro estado válido después de que una transacción se haya completado. 

    	Significa que todas las reglas y restricciones de integridad definidas en la base de datos se mantienen durante y después de cada transacción.


    Aislamiento (Isolation): 

    	Se refiere a la capacidad de ejecutar múltiples transacciones simultáneamente sin que interfieran entre sí.

    	Cada transacción debe ser independiente de las demás y no debe ver los efectos intermedios de otras transacciones que se están ejecutando simultáneamente.


    Durabilidad (Durability): 

    	Indica que una vez que se ha confirmado una transacción, los cambios realizados en la base de datos persisten incluso en el caso de fallos del sistema, como cortes de energía, fallos de hardware o cualquier otro tipo de fallo.

    	Los datos confirmados deben ser permanentes y no deben perderse, aunque ocurran eventos adversos	



|| Instalación y Ejecución

	Agregar el repo oficial y utilizar el comando 'mongod' para inciiar el servidor de MongoDB. 



|| Módulos 
	
	Se utilizan para administrar, monitorear y realizar operaciones relacionadas con bases de datos y conjuntos de datos.
	
	
	mongod: 

		Es el demonio del servidor de MongoDB que maneja las solicitudes de clientes y gestiona el acceso a los datos en la base de datos.


    mongo: 

    	Es un cliente de línea de comandos que proporciona una interfaz para conectarse a las instancias de MongoDB y ejecutar comandos para administrar la base de datos y realizar consultas.


    mongos: 

    	Es el servicio de enrutamiento de shards en un clúster de MongoDB con particionamiento en varios servidores.


    mongodump y mongorestore: 

    	Son utilidades de MongoDB utilizadas para realizar copias de seguridad y restaurar bases de datos y conjuntos de datos.


    mongoimport y mongoexport:

    	Son utilidades utilizadas para importar y exportar datos desde y hacia archivos JSON, CSV y otros formatos en una base de datos MongoDB.


    mongostat y mongotop: 

    	Son herramientas utilizadas para monitorear el estado y el rendimiento del servidor de MongoDB y de las operaciones en tiempo real.


    mongofiles: 

    	Es una herramienta que permite a los usuarios trabajar con archivos binarios en un sistema de archivos en GridFS, que es un sistema de archivos para almacenar y recuperar archivos de gran tamaño en MongoDB.

	

|| Funciones

	Realizar operaciones comunes en la base de datos y para manipular datos. 

	Algunas de estas funciones son específicas de consultas, agregaciones y actualizaciones.


    Operaciones de consulta:
    	
    	find(): 

    		Utilizada para recuperar documentos de una colección que coincidan con un conjunto de criterios especificados.

    	
    	findOne(): 

    		Similar a find(), pero devuelve solo el primer documento que cumpla con los criterios de consulta.


    Operaciones de agregación:

        aggregate(): 

        	Utilizada para realizar operaciones de agregación en los datos de una colección. 

        	Puede realizar operaciones como agrupación, filtrado, proyección, ordenación y otras operaciones de agregación avanzadas.


    Operaciones de actualización:

        updateOne() y updateMany():

        	Utilizadas para actualizar uno o varios documentos que coinciden con los criterios de consulta especificados.


        replaceOne(): 

        	Utilizada para reemplazar un solo documento que coincide con los criterios de consulta especificados.


    Operaciones de eliminación:

        deleteOne() y deleteMany():

        	Utilizadas para eliminar uno o varios documentos que coinciden con los criterios de consulta especificados.


    Operaciones de manipulación de índices:

        createIndex():

        	Utilizada para crear índices en campos específicos de una colección para mejorar el rendimiento de las consultas.


    Funciones de manipulación de texto:

        text(): 

        	Utilizada para realizar búsquedas de texto completo en campos de texto específicos dentro de una colección.



|| Tipos de datos

	Se pueden representar diferentes tipos de datos en MongoDB utilizando documentos JSON. 

	Los documentos JSON son la forma en que se almacenan y representan los datos en MongoDB.


	String: 

		Se utiliza para representar datos de texto, como nombres, direcciones, descripciones, entre otros.

		```json
		{
		  "nombre": "Juan Perez",
		  "profesion": "Ingeniero de software"
		}

		```


    Integer: 

    	Representa números enteros sin decimales.

    	```
    	{
		  "edad": 30,
		  "cantidad_productos": 25
		}

    	```


    Double: 

    	Utilizado para representar números con decimales, como valores monetarios o valores numéricos más precisos.

    	```
    	{
		  "precio": 29.99,
		  "promedio_calificaciones": 4.5
		}

    	```


    Boolean: 

    	Representa valores booleanos, es decir, verdadero o falso (true o false).

    	```
    	{
		  "es_estudiante": true,
		  "es_empleado": false
		}

    	```


    Arrays: 

    	Se utilizan para almacenar conjuntos o listas de valores en un solo campo, lo que permite la creación de listas o matrices de elementos.

    	```
    	{
		  "nombres": ["Juan", "Maria", "Pedro"],
		  "edades": [30, 28, 35]
		}

    	```


    Objects: 

    	Permite almacenar objetos anidados que contienen pares de clave-valor.

    	```
    	{
		  "usuario": {
		    "nombre": "Ana",
		    "edad": 26,
		    "profesion": "Diseñadora"
		  }
		}

    	```


    Date: 

    	Se utiliza para almacenar fechas y horas.

    	```
    	{
		  "fecha_registro": ISODate("2023-10-16T08:00:00Z")
		}

    	```


    Null: 

    	Representa un valor nulo o vacío en un campo.

    	```
    	{
		  "campo_vacio": null
		}

    	```


    ObjectId: 

    	Un identificador único de 12 bytes utilizado para identificar de manera única documentos en una colección.

    	```
    	{
		  "_id": ObjectId("616a9d793a791d9d04c9c50a"),
		  "nombre": "Ejemplo de ObjectId"
		}

    	```


    Timestamp: 

    	Almacena un sello de tiempo específico para eventos.

    	```
    	{
		  "evento": "Inicio de sesión",
		  "timestamp": Timestamp(1634370947, 1)
		}

    	```


    Regular expression: 

    	Se utiliza para almacenar expresiones regulares que se utilizan para buscar patrones específicos en cadenas de texto.

    	```
    	{
		  "patron": "/\d{3}-\d{3}-\d{4}/",
		  "ejemplo": "123-456-7890"
		}

    	```


    Binary data: 

    	Permite almacenar datos binarios, como archivos de imagen, video u otros tipos de archivos binarios.

    	```	
    	{
		  "imagen_perfil": BinData(0, "iVBORw0KGgoAAAANSUhEUgAA...") 
		}

    	```



|| Operadores 

	Se utilizan para realizar consultas, actualizaciones y proyecciones en los datos almacenados en la base de datos.

	Estos operadores permiten realizar operaciones más complejas y específicas en los documentos.	


	Operadores de Comparación:
        
        $eq: Igual a

        $ne: No igual a

        $gt: Mayor que

        $lt: Menor que

        $gte: Mayor o igual que

        $lte: Menor o igual que


    Operadores Lógicos:
        
        $and: Evalúa una expresión 
        booleana para ambos operadores
        
        $or: Evalúa una expresión booleana para al menos uno de los operadores
        
        $not: Niega el valor de la consulta


    Operadores de Elemento:
        
        $exists: Verifica si un campo existe en un documento
        
        $type: Se utiliza para comparar el tipo de un valor con un valor BSON específico


    Operadores de Elementos de Array:
        
        $all: Coincide con arrays que contienen todos los elementos especificados
        
        $elemMatch: Coincide con documentos que contienen un array con al menos un elemento que coincide con los criterios de consulta especificados


    Operadores de Expresión Regular:
       
        $regex: Realiza una coincidencia de expresión regular en los valores de cadena


    Operadores de Actualización:

        $set: Establece el valor de un campo en un documento
        
        $unset: Elimina un campo de un documento
        
        $inc: Incrementa el valor de un campo numérico en un valor específico
        
        $push: Agrega un valor a un array
        
        $addToSet: Agrega un valor a un array solo si no existe ya



|| Sintaxis básica

	
	1. Conexión a una basa de datos: 
	
		```js

		// Conexión a una base de datos local
		mongo

		// Conexión a una base de datos remota
		mongo --host <hostname> --port <port_number>

		```	


	2. Selección de una base de datos:

		```js

		use <nombre_de_la_base_de_datos>

		```


	3. Inserción de documentos en una colección:

		```js

		db.<nombre_de_la_coleccion>.insertOne({ <campo>: <valor>, <campo2>: <valor2>, ... })	

		```


	4. Consulta de documentos en una colección:

		```js

		db.<nombre_de_la_coleccion>.find({ <campo>: <valor> })

		```


	5. Actualización de documentos en una colección:

		```js

		db.<nombre_de_la_coleccion>.updateOne({ <campo>: <valor> }, { $set: { <campo>: <nuevo_valor> } })

		```


	6. Eliminación de documentos en una colección:

		```
		db.<nombre_de_la_coleccion>.deleteOne({ <campo>: <valor> })

		```


|| Proyectos básico

	Crear contenedor para el proyecto:

		```
		mkdir mi-proyecto
		
		cd mi-proyecto

		```	


	Inicializar node.js e instalar mongoose:

		```	
		npm init -y
		
		npm install mongoose

		```


	Crear app.js y configurar MongoDB: 

		```js

		const mongoose = require('mongoose');

		// Conectarse a la base de datos
		mongoose.connect('mongodb://localhost:27017/mi-base-de-datos', {
		  useNewUrlParser: true,
		  useUnifiedTopology: true,
		});

		// Definir un esquema y un modelo para la colección
		const Schema = mongoose.Schema;
		const UsuarioSchema = new Schema({
		  nombre: String,
		  edad: Number,
		  email: String,
		});

		const Usuario = mongoose.model('Usuario', UsuarioSchema);

		// Crear un nuevo usuario
		const nuevoUsuario = new Usuario({
		  nombre: 'Ejemplo Usuario',
		  edad: 30,
		  email: 'ejemplo@usuario.com',
		});

		// Guardar el usuario en la base de datos
		nuevoUsuario.save(function (err, result) {
		  if (err) {
		    console.error(err);
		  } else {
		    console.log('Usuario guardado con éxito:', result);
		  }
		});


		```	


	Ejecutar proyecto: 

		```
		node app.js

		```



|| Buenas prácticas

	Diseño de esquema adecuado:

		Diseña el esquema de tu base de datos de manera que se ajuste a tus consultas y requisitos de rendimiento.

		Evita el anidamiento excesivo y el diseño de esquemas complejos que puedan afectar negativamente el rendimiento de las consultas.


    Uso eficiente de índices: 

    	Crea índices adecuados en los campos que se utilizan con frecuencia en las consultas para mejorar el rendimiento de las operaciones de búsqueda y agilizar las consultas.


    Optimización de consultas:

    	Utiliza la funcionalidad de explicación de consultas para identificar y optimizar las consultas lentas. 

    	Asegúrate de que tus consultas estén bien optimizadas y utilicen índices siempre que sea posible.


    Seguridad: 

    	Configura la autenticación y autorización adecuadas para proteger tus datos. 

    	Utiliza roles de usuario y permisos de acceso para restringir el acceso a la base de datos y garantizar que solo los usuarios autorizados puedan realizar ciertas operaciones.


    Respaldo y recuperación:

    	Implementa una estrategia sólida de respaldo y recuperación para garantizar que tus datos estén seguros y protegidos en caso de fallos o pérdida de datos.


    Escalabilidad: 

    	Diseña tu base de datos teniendo en cuenta la escalabilidad horizontal.

    	Asegúrate de que tu configuración sea capaz de escalar de manera eficiente a medida que tus necesidades de datos y tráfico aumenten.


    Actualizaciones y mantenimiento:

    	Mantén tu base de datos actualizada con las versiones más recientes de MongoDB para asegurarte de que estés aprovechando las últimas características, mejoras de rendimiento y correcciones de errores.


    Monitoreo y alertas: 

    	Implementa herramientas de monitoreo y configuraciones de alerta para supervisar el rendimiento de la base de datos y detectar problemas potenciales de forma proactiva.



|| Software de soporte

	Mongoose:

		Una biblioteca de modelado de objetos MongoDB para Node.js que proporciona una solución simple y basada en esquemas para la interacción con MongoDB.


    MongoDB Compass: 

    	Una herramienta gráfica de interfaz de usuario que permite explorar y manipular datos de manera visual en MongoDB, lo que facilita la administración y el análisis de datos.


    MongoDB Atlas:

    	Un servicio de base de datos en la nube completamente administrado que ofrece una manera fácil y segura de ejecutar, administrar y escalar aplicaciones en MongoDB en la nube.


    Express.js: 

    	Un framework de aplicaciones web para Node.js que se utiliza comúnmente en combinación con MongoDB para desarrollar aplicaciones web y APIs robustas y escalables.


    Node.js Driver: 

    	El controlador oficial de Node.js para MongoDB que permite a los desarrolladores interactuar con una base de datos MongoDB desde aplicaciones Node.js.


    Robomongo: 

    	Una herramienta de administración de bases de datos MongoDB que proporciona una interfaz gráfica de usuario fácil de usar para administrar, visualizar y manipular datos en una base de datos MongoDB.


    Mongoid: 

    	Una biblioteca de mapeo de objetos MongoDB para el lenguaje de programación Ruby que facilita la integración de MongoDB en aplicaciones Ruby on Rails y otros proyectos de Ruby.



|| Collections

	Es un conjunto de documentos almacenados en la base de datos que comparten un propósito común.

	Es similar al concepto de tabla en una base de datos relacional, pero a diferencia de las tablas, las colecciones no imponen un esquema fijo en los documentos que contienen. 

	Esto significa que los documentos individuales dentro de una colección pueden tener diferentes estructuras y campos, lo que brinda una gran flexibilidad en el diseño de datos y la gestión de información.


    Esquema flexible: 

    	Los documentos dentro de una colección no tienen que seguir un esquema fijo y pueden tener campos diferentes, lo que permite una mayor flexibilidad en la estructura de datos.


    Almacenamiento de documentos: 

    	Las colecciones almacenan documentos en formato BSON (JSON binario) y pueden contener una variedad de tipos de datos y estructuras de datos complejas.


    Índices: 

    	Las colecciones admiten la creación de índices para acelerar las consultas y mejorar el rendimiento de las operaciones de búsqueda.


    Operaciones de consulta y manipulación: 

    	Las colecciones admiten una variedad de operaciones de consulta, actualización, inserción y eliminación de documentos, lo que permite una manipulación flexible y eficiente de los datos almacena.

    ```json

    {
	  "nombre": "Juan Perez",
	  "edad": 35,
	  "puesto": "Desarrollador",
	  "departamento": "Tecnología",
	  "habilidades": ["Java", "Python", "SQL"],
	  "salario": 60000
	}

    ```

    La colección almacena información sobre diferentes empleados, y cada documento puede tener un conjunto diferente de campos según la información específica de cada empleado.



|| Documents

	Un documento es la unidad básica de almacenamiento y recuperación de datos. 

	Se utiliza para representar un registro en la base de datos y está compuesto por un conjunto de pares clave-valor que representan campos y sus valores respectivos.

	Los documentos en MongoDB son análogos a las filas en una tabla de base de datos relacional, pero con la ventaja de que pueden contener estructuras de datos más complejas y flexibles, lo que permite una representación de datos más dinámica y enriquecida.


    Flexibilidad de esquema: 

    	Los documentos no están limitados por un esquema fijo, lo que significa que diferentes documentos en una misma colección pueden tener estructuras de datos completamente diferentes.


    Formato BSON: 

    	Los documentos se almacenan en formato BSON (Binary JSON), que es una representación binaria de JSON que permite almacenar y manipular datos de forma eficiente.


    Estructuras anidadas: 	

    	Los documentos pueden contener estructuras de datos anidadas y matrices, lo que permite una representación más rica y compleja de la información en comparación con las bases de datos relacionales tradicionales.


    Campos y valores: 

    	Cada campo en un documento tiene un nombre y un valor asociado que puede ser de cualquier tipo de dato admitido por MongoDB, como cadenas, números, matrices, objetos anidados, entre otros.


    Forman la base fundamental para el almacenamiento y la manipulación de datos y son la unidad principal de trabajo al interactuar con la base de datos.



|| MongoDB Compass

	Herramienta gráfica de interfaz de usuario (GUI) que proporciona una forma intuitiva y fácil de explorar y manipular datos en una base de datos MongoDB. 

	Está diseñada para simplificar la administración y la visualización de datos en MongoDB, lo que facilita a los desarrolladores y administradores de bases de datos la interacción con la base de datos sin necesidad de utilizar comandos de la línea de comandos.
	

	Exploración de datos: 

		Permite a los usuarios explorar los datos almacenados en la base de datos MongoDB de forma visual, lo que facilita la comprensión de la estructura de los datos y la relación entre los diferentes documentos y colecciones.


	Manipulación de datos: 

		Permite a los usuarios insertar, actualizar y eliminar datos de manera interactiva a través de una interfaz gráfica de usuario, lo que facilita la manipulación y la edición de datos sin necesidad de escribir comandos manualmente.


	Creación de consultas: 

		Ofrece capacidades de consulta intuitivas que permiten a los usuarios crear consultas personalizadas y ejecutarlas directamente desde la interfaz de usuario, lo que facilita la recuperación de datos específicos según ciertos criterios de búsqueda.


	Visualización de índices: 

		Permite a los usuarios ver y gestionar los índices en la base de datos, lo que facilita la optimización del rendimiento de las consultas y la gestión de los índices para mejorar la eficiencia de las operaciones de búsqueda.


	Análisis de rendimiento:

		Proporciona capacidades de monitoreo y análisis de rendimiento que permiten a los usuarios evaluar el rendimiento de la base de datos y realizar ajustes para optimizar el rendimiento y la escalabilidad.



|| MongoDB Shell

	Interfaz de línea de comandos interactiva proporcionada por MongoDB para interactuar con una instancia de base de datos de MongoDB. 

	Se utiliza para realizar una variedad de tareas relacionadas con la administración y la manipulación de datos en la base de datos MongoDB, como consultas, inserciones, actualizaciones, eliminaciones, entre otros.


    Interfaz de línea de comandos interactiva: 

    	Proporciona una interfaz de línea de comandos interactiva que permite a los usuarios ejecutar comandos y consultas directamente en la base de datos MongoDB.


    Operaciones de base de datos:

    	Permite a los usuarios realizar una variedad de operaciones de base de datos, como consultar datos, insertar nuevos documentos, actualizar documentos existentes, eliminar datos y realizar operaciones de agregación más complejas.


    Interacción con colecciones y documentos: 

    	Facilita la navegación y la manipulación de colecciones y documentos individuales en la base de datos, lo que permite a los usuarios visualizar y editar datos de forma interactiva.


    Funcionalidades de scripting:

     	Admite la ejecución de scripts de MongoDB que permiten a los usuarios automatizar tareas y realizar operaciones más complejas utilizando secuencias de comandos y funciones personalizadas.



|| Addign Documents
	
	Inserción de nuevos registros o documentos en una colección específica de la base de datos.

	Esto implica crear y almacenar nuevos datos en la base de datos para su posterior recuperación y uso.

	Para añadir un documento a una colección en MongoDB, puedes utilizar el método ¿insertOne()'' o 'insertMany()' según necesites insertar un solo documento o varios documentos a la vez.


	Ejemplos: 

		Usando insertOne()


	```js

	// Importar el cliente de MongoDB
	const { MongoClient } = require('mongodb');

	// URI de conexión a la base de datos
	const uri = 'mongodb://localhost:27017';

	// Nombre de la base de datos y colección
	const dbName = 'miBaseDeDatos';
	const collectionName = 'miColeccion';

	// Datos del nuevo documento a añadir
	const nuevoDocumento = { nombre: 'Ejemplo', edad: 30, email: 'ejemplo@ejemplo.com' };

	// Conectar al servidor de MongoDB
	const client = new MongoClient(uri);

	async function run() {
	  try {
	    await client.connect();
	    const database = client.db(dbName);
	    const collection = database.collection(collectionName);

	    // Añadir el nuevo documento a la colección
	    const result = await collection.insertOne(nuevoDocumento);
	    console.log(`Nuevo documento añadido con el id: ${result.insertedId}`);
	  } finally {
	    // Cerrar la conexión con el cliente
	    await client.close();
	  }
	}

	run().catch(console.dir);

	```


|| Finding Documents
	
	Recuperar registros específicos o documentos de una colección basados en ciertos criterios de búsqueda o consulta. 

	MongoDB proporciona el método find().

	```js

	// Importar el cliente de MongoDB
	const { MongoClient } = require('mongodb');

	// URI de conexión a la base de datos
	const uri = 'mongodb://localhost:27017';

	// Nombre de la base de datos y colección
	const dbName = 'miBaseDeDatos';
	const collectionName = 'miColeccion';

	// Criterios de búsqueda para encontrar documentos
	const query = { edad: { $gt: 25 } }; // Encontrar documentos con edad mayor que 25

	// Conectar al servidor de MongoDB
	const client = new MongoClient(uri);

	async function run() {
	  try {
	    await client.connect();
	    const database = client.db(dbName);
	    const collection = database.collection(collectionName);

	    // Encontrar documentos que coincidan con los criterios de búsqueda
	    const cursor = collection.find(query);

	    // Iterar sobre los documentos encontrados
	    await cursor.forEach(console.dir);
	  } finally {
	    // Cerrar la conexión con el cliente
	    await client.close();
	  }
	}

	run().catch(console.dir);

	```

	Recuperar todos los documentos que tengan un campo "edad" con un valor mayor que 25. 

	Puedes personalizar los criterios de búsqueda según tus necesidades específicas, y la función 'forEach' se utiliza para iterar sobre los documentos encontrados e imprimirlos en la consola.



|| Sorting Data

	Clasificación o ordenamiento de datos en MongoDB implica organizar los documentos recuperados de una colección en un orden específico basado en uno o más campos. 

	MongoDB proporciona el método sort() para realizar operaciones de ordenamiento en los resultados de una consulta.

	```js

	// Criterios de búsqueda y ordenamiento
	const query = {}; // Seleccionar todos los documentos
	const sortCriteria = { edad: 1 }; // Ordenar por edad en orden ascendente (1) o descendente (-1)

	// Encontrar y ordenar los documentos según los criterios de búsqueda y ordenamiento
    const cursor = collection.find(query).sort(sortCriteria);

	```
	

|| Limiting Data

	Implica restringir la cantidad de documentos recuperados de una colección en una consulta específica. 

	Esto es útil cuando solo se necesitan un número específico de resultados y se desea evitar la recuperación de todos los documentos que coinciden con los criterios de búsqueda.

	El método limit() se utiliza para limitar la cantidad de documentos devueltos en el resultado de una consulta.

	```js

	// Criterios de búsqueda y límite
	const query = {}; // Seleccionar todos los documentos
	const limitValue = 5; // Límite de 5 documentos en el resultado

	// Encontrar y limitar la cantidad de documentos devueltos
    const cursor = collection.find(query).limit(limitValue);	

	```



|| Nested Documents

	Capacidad de almacenar documentos dentro de otros documentos en la base de datos.

	Esto permite una estructura de datos más compleja y jerárquica en la que los documentos pueden contener campos que a su vez pueden contener otros documentos anidados o matrices.

	Esta característica permite una mayor flexibilidad en el modelado de datos y facilita la representación de relaciones más complejas entre los datos. 

	Los documentos anidados se pueden pensar como objetos dentro de objetos, lo que permite una representación más rica y estructurada de la información en comparación con las bases de datos relacionales tradicionales.

	```js

	{
	  "nombre": "Ejemplo",
	  "edad": 30,
	  "direccion": {
	    "calle": "Calle Principal",
	    "ciudad": "Ciudad Ejemplo",
	    "codigo_postal": "12345"
	  },
	  "contacto": {
	    "telefono": "123-456-7890",
	    "email": "ejemplo@ejemplo.com"
	  }
	}

	```

	El campo "direccion" y el campo "contacto" son documentos anidados dentro del documento principal. 

	Cada uno de estos documentos anidados tiene sus propios campos y valores que representan información específica, lo que permite una representación más estructurada y detallada de los datos.



|| Operadores

	Se utilizan para realizar una variedad de operaciones y consultas avanzadas en la base de datos. 

	Los operadores se utilizan para comparar valores, realizar operaciones matemáticas, buscar patrones y realizar muchas otras funciones que permiten a los usuarios manipular y analizar datos de manera eficiente. 

	Los operadores se utilizan en consultas de MongoDB para buscar y manipular documentos que cumplen ciertos criterios específicos.

	
	Tipos de Operadores:	

		Operadores de comparación:

			Comparar valores en consultas, como $eq, $ne, $gt, $lt, $gte, y $lte.

		```js

		// Encontrar documentos con edad mayor que 30
		db.collection.find({ edad: { $gt: 30 } });

		// Encontrar documentos con nombre que no sea "Ejemplo"
		db.collection.find({ nombre: { $ne: "Ejemplo" } });

		```


	    Operadores lógicos: 	

	    	Combinar múltiples expresiones lógicas en una sola consulta, como $and, $or, y $not.

	    ```js

	    // Encontrar documentos con edad mayor que 30 y nombre igual a "Juan"
		db.collection.find({ $and: [{ edad: { $gt: 30 } }, { nombre: "Juan" }] });

		// Encontrar documentos con edad mayor que 30 o nombre igual a "Juan"
		db.collection.find({ $or: [{ edad: { $gt: 30 } }, { nombre: "Juan" }] });

	    ```


	    Operadores de elementos: 

	    	Comprobar la existencia de campos o elementos en un documento, como $exists y $type.

	    ```js

	    // Encontrar documentos que contengan el campo "direccion"
		db.collection.find({ direccion: { $exists: true } });

		// Encontrar documentos con un campo "email" de tipo string
		db.collection.find({ email: { $type: "string" } });

	    ```


	    Operadores de arreglo: 
			
			Trabajar con campos de tipo matriz, como $all, $elemMatch, $size, y otros.

		```js

		// Encontrar documentos con todos los elementos de la matriz "intereses" que coincidan
		db.collection.find({ intereses: { $all: ["programación", "viajes"] } });

		// Encontrar documentos con al menos un elemento en la matriz "resultados" que cumpla ciertas condiciones
		db.collection.find({ resultados: { $elemMatch: { $gte: 80, $lt: 85 } } });

		```	


	    Operadores de proyección:

	    	Especificar qué campos incluir o excluir en los resultados de una consulta, como $project y $slice.			



|| Complex Queries

	Consultas que implican la combinación de múltiples condiciones y operaciones para recuperar datos específicos de la base de datos. 

	Estas consultas pueden incluir una variedad de operadores y criterios de búsqueda que permiten a los usuarios realizar consultas avanzadas y detalladas para encontrar documentos que cumplan con ciertos criterios específicos.


	1. Consultas que involucran múltiples operadores de comparación y lógicos para buscar documentos que cumplan con múltiples condiciones al mismo tiempo.

    2. Consultas que incluyen operaciones de agrupación y agregación para realizar cálculos y resúmenes en conjuntos de datos.

    3. Consultas que implican la combinación de operaciones de búsqueda, ordenamiento y limitación para obtener conjuntos de datos específicos ordenados y limitados.


    Fundamental para obtener información precisa y detallada de conjuntos de datos grandes y complejos. 

    La comprensión de cómo construir y ejecutar consultas complejas es esencial para extraer información significativa de la base de datos y para realizar análisis avanzados y operaciones de manipulación de datos.


    Ejemplo: 

    	Recuperar datos específicos de la base de datos.

    	Tenemos una colección de documentos que representan información de empleados, y queremos recuperar aquellos empleados que tengan más de 30 años y cuyo cargo sea "Desarrollador". 

    	Además, queremos ordenar los resultados por apellido de forma descendente y limitar los resultados a 5 documentos

    	```js

    	db.empleados.find({
		    $and: [
		        { edad: { $gt: 30 } },
		        { cargo: "Desarrollador" }
		    ]
		}).sort({ apellido: -1 }).limit(5);

    	```

    	Utilizando el operador $and para combinar dos condiciones, el operador de comparación $gt para encontrar empleados con edad mayor a 30, y la condición de igualdad para el cargo "Desarrollador". 

    	Luego, utilizamos el método sort() para ordenar los resultados por el campo "apellido" en orden descendente y el método limit() para limitar los resultados a 5 documentos



|| Operador $in

	Seleccionar documentos donde el valor de un campo determinado coincida con cualquiera de los valores especificados en una matriz. 

	Este operador es útil cuando se busca una coincidencia con múltiples valores posibles en un campo específico.

	```js

	{ campo: { $in: [valor1, valor2, valor3, ...] } }

	```

	Si queremos encontrar aquellos cuyo cargo sea "Desarrollador" o "Analista:

	```js

	db.empleados.find({ cargo: { $in: ["Desarrollador", "Analista"] } });	

	```	

	La consulta buscará documentos en la colección "empleados" donde el campo "cargo" coincida con cualquiera de los valores especificados en la matriz ["Desarrollador", "Analista"].	


	Es útil cuando se necesita realizar consultas que involucren múltiples valores posibles para un campo específico.



|| Operador $nin

	Seleccionar documentos donde el valor de un campo específico no coincida con ninguno de los valores especificados en una matriz. 

	Este operador es útil cuando se desea excluir documentos que coincidan con varios valores específicos en un campo determinado.

	```js

	{ campo: { $nin: [valor1, valor2, valor3, ...] } }

	```

	Encontrar aquellos cuyo cargo no sea ni "Desarrollador" ni "Analista".

	```js

	db.empleados.find({ cargo: { $nin: ["Desarrollador", "Analista"] } });

	```

	Buscará documentos en la colección "empleados" donde el campo "cargo" no coincida con ninguno de los valores especificados en la matriz ["Desarrollador", "Analista"].



|| Querying Arrays

	Las consultas de matrices implican la búsqueda y manipulación de datos dentro de campos de tipo matriz en documentos de una colección.

	Estas consultas permiten buscar documentos basados en los elementos o propiedades de una matriz y realizar operaciones que involucran campos de matriz.


	Operadores: 	

		Se utilizan operadores de consulta de matrices, como '$all', '$elemMatch', $size y otros, que permiten a los usuarios buscar y manipular datos dentro de campos de matriz en la base de datos.		

	Operaciones:
 	
		Buscar documentos que contentengan: 

			1. Elemento específico en una matriz.

			```js

			// Encontrar documentos que contengan "manzana" en la matriz de frutas
			db.inventario.find({ frutas: "manzana" });

			```


			2. Todos los elementos especificados en una matriz.

			```js

			db.inventario.find({ frutas: { $all: ["manzana", "plátano"] } });

			```


			3. En función del tamaño de una matriz.

			```js

			db.inventario.find({ frutas: { $size: 3 } });

			```


			4. Elementos que cumplan ciertos criterios de consulta en una matriz.

			```js

			db.datos.find({ valores: { $elemMatch: { $gt: 5 } } });

			```



|| Arrays
	
	Tipo de dato que puede contener múltiples valores, incluidos otros documentos, dentro de un solo campo en un documento. 

	Los arrays en MongoDB son útiles para modelar datos que pueden tener una estructura repetitiva o datos relacionados que deben almacenarse juntos en un campo.

	Pueden contener una variedad de tipos de datos, incluidos valores de cadena, valores numéricos, fechas, booleanos, y también otros documentos de MongoDB o matrices anidadas.

	Esto proporciona flexibilidad en la estructuración de datos y permite representar relaciones más complejas entre los datos dentro de un solo campo.

	```js

	{
	  "nombre": "Ejemplo",
	  "edades": [30, 35, 40, 25],
	  "contactos": [
	    { "tipo": "teléfono", "valor": "123-456-7890" },
	    { "tipo": "email", "valor": "ejemplo@ejemplo.com" }
	  ]
	}

	```

	El campo "edades" y "contactos" son de tipo array en un documento. 

	Contienen valores numéricos y documentos anidados (otros campos/entradas) en este caso de tipo array para representar una amplia información. 



|| Delating Documents

	Eliminación de uno o varios documentos de una colección en la base de datos. 

	Esto se hace utilizando el método 'deleteOne()' para eliminar un solo documento o el método 'deleteMany()' para eliminar múltiples documentos que coinciden con ciertos criterios de búsqueda.

	```js

	// Criterios de eliminación
	const filter = { nombre: 'Ejemplo' }; // Eliminar documentos con el campo "nombre" igual a "Ejemplo"

	// Eliminar un solo documento que cumpla con los criterios de eliminación
    const result = await collection.deleteOne(filter);
    console.log(`${result.deletedCount} documento eliminado`);

	```



|| Updating Documents

	Permite modificar el contenido de un documento existente en una colección. 

	Puedes actualizar un documento completo o solo partes específicas de él, según tus necesidades. 

	MongoDB ofrece una variedad de métodos y operadores para realizar actualizaciones de manera efectiva.
	

	Métodos: 

		updateOne(): 

			Actualiza un solo documento que coincide con los criterios de consulta especificados.

    	updateMany(): 

    		Actualiza varios documentos que coinciden con los criterios de consulta especificados.

    	replaceOne(): 

    		Reemplaza un solo documento que coincide con los criterios de consulta especificados con otro documento.


	Operadores: 

		set: 
			
			Establece el valor de un campo en un documento existente o crea el campo si no existe.

		$unset: 

			Elimina un campo específico de un documento.

		$inc: 

			Incrementa el valor de un campo numérico en una cantidad específica.

		$push: 

			Agrega un valor a un campo de tipo array.

		$addToSet: 	

			Agrega un valor a un campo de tipo array si el valor no está presente en el array.

		$pull: 

			Elimina un valor específico o elementos que coinciden con una condición de un campo de tipo array.

		$pop: 

			Elimina el primer o último elemento de un campo de tipo array.	


	Ejemplo: 

		```js

		db.usuarios.updateOne(
		    { _id: ObjectId("id_del_usuario") },
		    { $set: { nombre: "NuevoNombre" } }
		);

		```

		Actualiza el nombre del usuario con el ID especificado a "NuevoNombre".



|| MongoDB Drivers

	Bibliotecas de software que actúan como interfaces de programación para permitir que las aplicaciones se conecten y se comuniquen con una base de datos de MongoDB. 

	Estos drivers proporcionan métodos y funciones que permiten a los desarrolladores interactuar con una base de datos MongoDB desde sus aplicaciones, lo que les permite realizar operaciones como inserciones, consultas, actualizaciones y eliminaciones de datos.

	Los drivers de MongoDB están disponibles para una variedad de lenguajes de programación populares, lo que permite a los desarrolladores integrar MongoDB en sus aplicaciones independientemente del lenguaje en el que estén trabajando. 


    MongoDB Node.js Driver: Para aplicaciones de JavaScript y Node.js.

		npm install mongodb    	

    
    MongoDB Python Driver: Para aplicaciones de Python.

    	pip install pymongo


    MongoDB Java Driver: Para aplicaciones de Java.

    	Desde el repositorio de Maven o Gradle. 

    	Agrega la dependencia apropiada a tu archivo de configuración y construye tu proyecto para importar las clases necesarias.


    MongoDB C#/.NET Driver: Para aplicaciones de C# y .NET.

    	A través del administrador de paquetes NuGet en Visual Studio.


    MongoDB Ruby Driver: Para aplicaciones de Ruby.

    	A través de RubyGems.


    MongoDB Go Driver: Para aplicaciones de Go.

    	utilizando el comando go get.



|| Cursors
	
	Mecanismo que permite a las aplicaciones recuperar resultados de consultas de la base de datos de manera eficiente y escalable. 

	Los cursores son utilizados por las operaciones de lectura, como las consultas de 'find()' y agregación, para recorrer los resultados de una consulta que puede contener un gran número de documentos.

	Cuando se realiza una consulta en MongoDB que devuelve un gran número de resultados, el cursor permite a la aplicación recuperar los resultados de la consulta de manera eficiente en lotes o páginas, lo que evita la necesidad de recuperar todos los resultados de la consulta de una sola vez. 

	Esto es útil para minimizar el uso de recursos y mejorar el rendimiento al trabajar con conjuntos de datos grandes.

	Los cursores en MongoDB se utilizan comúnmente en combinación con el método 'forEach()' para iterar sobre los resultados de una consulta y procesarlos uno a uno, o con métodos de manipulación de cursores como 'next()' para recuperar el siguiente documento en el conjunto de resultados.

	En resumen, los cursores en MongoDB son esenciales para manejar eficientemente grandes conjuntos de datos y permiten un procesamiento escalable de resultados de consultas.

	```js

	// Nombre de la base de datos y colección
	const dbName = 'miBaseDeDatos';
	const collectionName = 'miColeccion';

	// Realizar una consulta que devuelve un cursor
    const cursor = collection.find({});

    // Iterar sobre los resultados del cursor
    await cursor.forEach(console.dir);

	```

	'find()' realiza una consulta que devuelve un cursor que contiene todos los documentos en la colección "miColeccion". 

	'forEach()' se utiliza para iterar sobre los resultados del cursor e imprimir cada documento en la consola.


	Hay otros métodos disponibles para manipular cursores en MongoDB, como 'next()', que se puede usar para recuperar el siguiente documento en el cursor.



|| Fetching Data

	Proceso de recuperar o extraer información de la base de datos que cumpla con ciertos criterios de búsqueda. 

	Esto implica realizar consultas o búsquedas en la base de datos para encontrar documentos que coincidan con ciertas condiciones especificadas por el usuario.

	El proceso de recuperar datos de MongoDB generalmente implica el uso de consultas que utilizan métodos como 'find()', 'findOne()', y otras operaciones de agregación para recuperar datos específicos de una o varias colecciones en la base de datos.

	Algunos ejemplos comunes de operaciones de obtención de datos en MongoDB incluyen la recuperación de todos los documentos en una colección, la recuperación de documentos que coincidan con ciertos criterios de búsqueda, la recuperación de un solo documento basado en un criterio específico, y la recuperación de datos mediante operaciones de agregación como 'aggregate()' para realizar cálculos y análisis más complejos en los datos.

	El proceso de extracción de datos es fundamental para cualquier aplicación que interactúe con una base de datos MongoDB, y comprende una variedad de técnicas y operaciones que permiten a los usuarios recuperar y procesar datos de manera efectiva y eficiente.


|| Postman

	handling post request 
 
	handling delate request 

	patch requests 

	pagination 

	indexes 



|| Mongodb Atlas 
	
	Servicio de base de datos en la nube de MongoDB que ofrece una forma fácil y segura de alojar, administrar y escalar bases de datos MongoDB en la nube.

	Proporciona todas las características y funcionalidades de MongoDB sin la necesidad de configurar la infraestructura de hardware y software subyacente.


    Escalabilidad: 

    	Permite escalar la base de datos de forma flexible para satisfacer las demandas cambiantes de la aplicación, ya sea aumentando vertical u horizontalmente.


    Seguridad: 

    	Proporciona características de seguridad avanzadas, como cifrado de datos en reposo y en tránsito, cortafuegos de red, y opciones de autenticación y autorización robustas.


    Disponibilidad y tolerancia a fallos: 

    	Ofrece opciones de configuración de alta disponibilidad y tolerancia a fallos para garantizar que la base de datos esté siempre disponible y que los datos estén protegidos contra fallos del sistema.


    Facilidad de uso: 

    	Proporciona una interfaz de usuario intuitiva y herramientas de administración que simplifican las tareas de implementación, configuración y administración de la base de datos.


    Automatización: 

    	Ofrece características de automatización para tareas comunes de administración, lo que permite a los desarrolladores concentrarse en el desarrollo de aplicaciones en lugar de en la administración de la base de datos.


	MongoDB Atlas es una solución popular para empresas y desarrolladores que desean aprovechar los beneficios de MongoDB sin la necesidad de administrar la infraestructura de la base de datos por sí mismos. 

	Permite un despliegue rápido y sencillo de bases de datos MongoDB en la nube, lo que facilita el desarrollo y la implementación de aplicaciones escalables y seguras.


	Uso: 

	    Registro en el sitio oficial de MongoDB Atlas.


	    Configuración del clúster:

	    	Una vez que hayas iniciado sesión, podrás configurar tu clúster de MongoDB Atlas a través de la interfaz web.

	    	Podrás elegir la configuración, el proveedor de la nube, la región, el tamaño del clúster y otras opciones relevantes.


	    Acceso a través de la interfaz web: 

	    	Después de configurar tu clúster, puedes administrarlo y trabajar con tus bases de datos a través de la interfaz web de MongoDB Atlas.

	    	Desde aquí, puedes realizar tareas como configurar la seguridad, supervisar el rendimiento, escalar el clúster y más.


	    Acceso a través de la línea de comandos: 

	    	También puedes acceder a tu clúster de MongoDB Atlas a través de la interfaz de línea de comandos de MongoDB, lo que te permite realizar tareas avanzadas de administración y configuración utilizando comandos específicos de MongoDB



|| Compass

	Es una herramienta de interfaz gráfica de usuario (GUI) que facilita la exploración y el manejo de datos en MongoDB.

	Permite realizar diversas consultas en la base de datos de una manera más intuitiva y visual. 


    Consulta de documentos: 

    	Permite buscar documentos específicos en una colección según ciertos criterios de consulta, como igualdad, desigualdad, comparaciones, existencia de campos, entre otros.


    Ordenamiento de datos: 

    	Facilita la ordenación de los resultados de la consulta en función de uno o más campos, ya sea en orden ascendente o descendente.


    Filtrado de datos: 

    	Permite filtrar los resultados de la consulta según ciertos criterios específicos para limitar los datos que se muestran en la interfaz.


    Proyección de campos: 

    	Permite especificar qué campos específicos se deben mostrar en los resultados de la consulta, lo que te permite enfocarte en la información relevante.


    Agregación de datos: 

    	Facilita el uso de operaciones de agregación para realizar cálculos más complejos y consultas que implican la combinación, transformación y análisis de datos en la base de datos.

	
	Además de estas consultas básicas, MongoDB Compass también ofrece herramientas visuales y opciones de configuración avanzadas que facilitan la exploración de datos y el análisis en MongoDB. 


	Compass y Atlas:

		1. Inicia sesión en MongoDB Atlas. 


		2. Accede al clúster: 	

			Una vez que hayas accedido a tu cuenta, selecciona el clúster al que deseas conectarte.


		3. Acceso a la función de conexión: 

			Busca la opción "Connect" y sus funciones. 


		4. Selecciona la opción de conexión con Compass: 

			En las opciones de conexión, elige la opción que te permita conectarte con MongoDB Compass.


		5. Copia la cadena de conexión: 

			Se te proporcionará una cadena de conexión que puedes copiar.


		6. Inicia MongoDB Compass.


		7. Pega la cadena de conexión: 

			En la pantalla de inicio de sesión de MongoDB Compass, pega la cadena de conexión en el campo correspondiente.


		8. Realiza la conexión: 

			Haz la conexión entre MongoDB Compass con tu clúster de MongoDB Atlas.



|| Cluster
	
	Conjunto de servidores de base de datos que trabajan juntos para almacenar y procesar datos.

	Un cluster en MongoDB Atlas es una implementación de un conjunto de servidores de bases de datos MongoDB gestionados en la nube a través del servicio de base de datos como servicio (DBaaS) de MongoDB Atlas.


	Distribución geográfica: 

		MongoDB Atlas permite configurar clusters en diferentes regiones geográficas para garantizar una baja latencia y cumplir con los requisitos de residencia de datos.


	Escalabilidad automática: 

		Los clusters en MongoDB Atlas se pueden escalar vertical y horizontalmente según las necesidades de la aplicación, lo que permite manejar cargas de trabajo cambiantes y garantizar un rendimiento constante.


	Alta disponibilidad: 

		MongoDB Atlas garantiza la alta disponibilidad de los datos mediante la replicación automatizada y la gestión de la redundancia de los datos en diferentes servidores, lo que asegura que los datos estén siempre disponibles incluso en caso de fallas del servidor.



|| Robo 3T

	Interfaz gráfica de usuario (GUI) gratuita y de código abierto para MongoDB.

	Anteriormente conocida como Robomongo, Robo 3T proporciona a los desarrolladores y administradores de bases de datos una forma intuitiva y potente de interactuar con bases de datos MongoDB. 


    Interfaz intuitiva: 

    	Robo 3T presenta una interfaz de usuario intuitiva y fácil de usar que permite a los usuarios visualizar y manipular los datos de MongoDB de manera eficiente.


    Funcionalidades avanzadas:

    	Ofrece diversas funciones avanzadas, como la capacidad de ejecutar consultas, crear y modificar índices, importar y exportar datos, y administrar la base de datos de manera efectiva.


    Compatibilidad con MongoDB: 

    	Robo 3T es compatible con todas las versiones recientes de MongoDB y proporciona una forma sencilla de administrar bases de datos tanto locales como en la nube.


    Visualización de datos: 

    	Permite visualizar los datos de MongoDB de forma clara y estructurada, lo que facilita la comprensión y manipulación de los datos complejos y anidados.


    Edición de datos: 

    	Permite a los usuarios editar los documentos directamente en la interfaz, lo que simplifica la tarea de realizar cambios en los datos existentes.


    Funciones de importación y exportación: 

    	Facilita la importación y exportación de datos hacia y desde MongoDB, lo que permite la transferencia de datos entre diferentes sistemas y entornos de desarrollo.	



|| Studio 3T

	Interfaz gráfica de usuario (GUI) para MongoDB que proporciona un entorno completo de desarrollo integrado (IDE) para trabajar con bases de datos MongoDB. 

	Anteriormente conocido como MongoChef, Studio 3T ofrece una amplia gama de características y funcionalidades para facilitar la administración y el desarrollo de bases de datos MongoDB. 


    Interfaz gráfica intuitiva:

    	Studio 3T ofrece una interfaz de usuario fácil de usar que permite a los usuarios administrar y manipular bases de datos MongoDB de manera eficiente.


    Funciones avanzadas de consulta:

    	Proporciona diversas herramientas avanzadas de consulta que facilitan la escritura y ejecución de consultas complejas en la base de datos.


    Generación de consultas visuales: 

    	Permite a los usuarios generar consultas utilizando una interfaz visual intuitiva que simplifica el proceso de creación y ejecución de consultas.


    Visualización de datos en tiempo real: 

    	Ofrece la capacidad de visualizar y analizar datos en tiempo real directamente desde la base de datos, lo que facilita la comprensión de los datos complejos.


    Edición de datos en lugar: 

    	Permite a los usuarios editar documentos directamente en la interfaz, lo que simplifica la tarea de realizar cambios en los datos existentes.


    Importación y exportación de datos: 

    	Facilita la importación y exportación de datos hacia y desde MongoDB, lo que permite la transferencia de datos entre diferentes sistemas y entornos de desarrollo.



|| insertOne()

	Método que se utiliza para insertar un solo documento en una colección. 

	Este método toma un objeto que representa el documento que se va a insertar como argumento. 

	El documento debe ser un objeto JSON válido que contenga los campos y valores que se desean insertar en la colección.


	Sintaxis: 

		```js

		db.collection.insertOne(
		   <documento>,
		   {
		      writeConcern: <documento>
		   }
		)

		```

		'db' es la variable que hace referencia a la base de datos actual.

	    'collection' es el nombre de la colección en la que se insertará el documento.

	    '<documento>' es el objeto JSON que representa el documento que se va a insertar.

	    'writeConcern' es un documento que especifica la configuración de preocupación de escritura para la operación.


	Ejemplo:

		insertOne() devolverá un objeto 'InsertOneResult' que contendrá información sobre la operación de inserción, incluido el identificador único (_id) asignado al documento recién insertado.

		```js

		// Insertar un documento en la colección "miColeccion"
		db.miColeccion.insertOne( 
		   { 
		      nombre: "Ejemplo",
		      edad: 30,
		      ciudad: "Ejemplolandia" 
		   } 
		);

		```

		Se inserta un documento con tres campos (nombre, edad y ciudad) en la colección miColeccion. 

		Si la operación se realiza con éxito, se devolverá un objeto 'InsertOneResult' que contendrá información sobre la operación de inserción.



|| insertMany()

	Insertar varios documentos a la vez en una colección. 

	Este método toma una matriz de objetos que representan los documentos que se van a insertar como argumento. 

	Cada elemento de la matriz debe ser un objeto JSON válido que contenga los campos y valores que se desean insertar en la colección.


	Sintaxis:

		```js

		db.collection.insertMany(
		   [ <documento1>, <documento2>, ... ],
		   {
		      writeConcern: <documento>,
		      ordered: <boolean>
		   }
		)

		```

		db: 

			Es la variable que hace referencia a la base de datos actual.

    	collection:

    		Es el nombre de la colección en la que se van a insertar los documentos.

    	<documento1>, <documento2>...,: 

    		Los objetos JSON que representan los documentos que se van a insertar.

    	writeConcern: 

    		Es un documento que especifica la configuración de preocupación de escritura para la operación.
    	
    	ordered: 

    		Es un booleano que indica si los documentos deben insertarse en orden.


    	insertMany() devolverá un objeto 'InsertManyResult' que contendrá información sobre la operación de inserción, incluidos los identificadores únicos (_id) asignados a los documentos recién insertados.


    Ejemplo:

    	```js

    	// Insertar varios documentos en la colección "miColeccion"
		db.miColeccion.insertMany( 
		   [ 
		     { nombre: "Ejemplo1", edad: 30, ciudad: "Ejemplolandia" },
		     { nombre: "Ejemplo2", edad: 35, ciudad: "Ejemplolandia" },
		     { nombre: "Ejemplo3", edad: 25, ciudad: "Ejemplolandia" } 
		   ]
		);

    	```

    	En la colección miColeccion utilizando el método insertMany(). 

    	Si la operación se realiza con éxito, se devolverá un objeto 'InsertManyResult' que contendrá información sobre la operación de inserción.



|| Import

	Cargar datos desde una variedad de fuentes externas, como archivos JSON, CSV o BSON, en una base de datos de MongoDB.

	Esta funcionalidad es útil para migrar datos de sistemas heredados a MongoDB o para cargar conjuntos de datos grandes en una base de datos existente.
	

	Varias formas: 	

	Comando mongoimport: 

		MongoDB proporciona la utilidad 'mongoimport', que te permite importar datos desde archivos JSON, CSV, TSV y BSON directamente en una base de datos MongoDB desde la línea de comandos.


	Herramientas de terceros:

		Además de mongoimport, hay varias herramientas de terceros y bibliotecas que se pueden utilizar para importar datos en MongoDB desde diferentes fuentes y formatos de datos.


	Herramientas de interfaz gráfica de usuario (GUI):

		Algunas herramientas de GUI, como Robo 3T y Studio 3T, también permiten importar datos de forma visual y sencilla desde archivos externos a una base de datos MongoDB.		



|| load()

	Se utiliza en el contexto de la shell de MongoDB para cargar y ejecutar scripts de JavaScript directamente en la interfaz de la shell. 

	No se utiliza específicamente para importar documentos desde archivos externos, como lo harías con la importación de datos desde un archivo JSON o CSV en MongoDB.


	Desde shell:

	```
	mongoimport --db NOMBRE_DE_LA_BASE_DE_DATOS --collection NOMBRE_DE_LA_COLECCION --file RUTA_DEL_ARCHIVO.json

	```



|| find()

	Recuperar documentos de una colección en función de un conjunto de criterios de consulta especificados. 

	Este método devuelve un cursor que puede ser utilizado para recorrer y acceder a los documentos que cumplen con los criterios de consulta.

	```js

	db.collection.find(
	   <consulta>,
	   <proyección>
	)

	```

	db: 

		Es la variable que hace referencia a la base de datos actual.

	collection: 

		Es el nombre de la colección de la que se recuperarán los documentos.
	
	<consulta>: 

		Es un objeto que especifica los criterios de consulta para filtrar los documentos.

	<proyección>: 

		Es un objeto que especifica qué campos se deben incluir o excluir en los resultados de la consulta.


	```js

	// Recuperar todos los documentos de la colección "miColeccion"
	db.miColeccion.find()

	// Recuperar documentos que cumplan ciertos criterios de consulta
	db.miColeccion.find({ campo1: valor1, campo2: valor2 })

	// Recuperar documentos y especificar qué campos mostrar en los resultados
	db.miColeccion.find({ campo: valor }, { campoDeseado: 1, _id: 0 })

	```


|| updateOne()
	
	Utiliza para actualizar un solo documento en una colección que coincida con un conjunto específico de criterios de consulta. 

	Este método actualiza el primer documento que cumple con los criterios de búsqueda especificados.
		
	```js

	db.collection.updateOne(
	   <filtro>,
	   <actualización>,
	   {
	     upsert: <booleano>,
	     writeConcern: <documento>
	   }
	)

	```

	db: 

		Variable que hace referencia a la base de datos actual.

    collection: 

    	Colección en la que se actualizará el documento.

    <filtro>: 

    	Objeto que especifica los criterios de consulta para identificar el documento que se va a actualizar.

    <actualización>: 

    	Objeto que define las actualizaciones que se deben realizar en el documento que coincide con el filtro especificado.

    upsert: 

    	Booleano que especifica si se debe crear un nuevo documento si no se encuentra un documento que coincida con los criterios de filtro.

    writeConcern: 

    	Documento que especifica la configuración de preocupación de escritura para la operación.


    ```js

    // Actualizar un documento que cumple ciertos criterios de consulta
	db.miColeccion.updateOne(
	   { nombre: "Ejemplo" },
	   { $set: { edad: 35 } }
	);

    ```

    Se actualiza el primer documento en la colección miColeccion que tenga el campo "nombre" con el valor "Ejemplo". 

    El operador $set se utiliza para establecer el valor del campo "edad" en 35.



|| $unset

	Operaciones de actualización para eliminar un campo específico de un documento.

	Elimina un campo existente junto con su valor en un documento.

	```js

	db.collection.updateOne(
	   <filtro>,
	   { $unset: { campo: 1 } }
	)

	```

	<filtro>

		es un objeto que especifica los criterios de consulta para identificar el documento que se va a actualizar.
	
	campo

		es el nombre del campo que se va a eliminar.

	El valor 1 se utiliza para indicar que el campo debe eliminarse.



|| $rename
	
	Se utiliza en operaciones de actualización para cambiar el nombre de un campo específico en un documento. 

	Permite renombrar un campo existente en un documento sin cambiar su valor.

	```js

	db.collection.updateOne(
	   <filtro>,
	   { $rename: { campoAntiguo: "campoNuevo" } }
	)

	```	

	campoAntiguo

		Nombre del campo que se va a renombrar.
	
	campoNuevo

		Nuevo nombre que se va a asignar al campo.


	```js

	// Cambiar el nombre del campo "edad" a "edadNueva" en un documento que cumple ciertos criterios de consulta
	db.miColeccion.updateOne(
	   { nombre: "Ejemplo" },
	   { $rename: { edad: "edadNueva" } }
	);

	```


|| $min

	Se utiliza en operaciones de actualización para el valor de un campo específico solo si el valor especificado es menor que el valor actual del campo en el documento. 

	Si el valor especificado es mayor o igual al valor actual del campo, el campo no se modifica.
	

	```js

	db.collection.updateOne(
	   <filtro>,
	   { $min: { campo: valor } }
	)

	```


	```js

	// Actualizar el campo "edad" con un nuevo valor si es menor que el valor actual en un documento que cumple ciertos criterios de consulta
	db.miColeccion.updateOne(
	   { nombre: "Ejemplo" },
	   { $min: { edad: 25 } }
	);

	```



|| $max

	Operaciones de actualización para el valor de un campo específico solo si el valor especificado es mayor que el valor actual del campo en el documento. 

	Si el valor especificado es menor o igual al valor actual del campo, el campo no se modifica.

	```js

	db.collection.updateOne(
	   <filtro>,
	   { $max: { campo: valor } }
	)

	```


	```js

	// Actualizar el campo "edad" con un nuevo valor si es mayor que el valor actual en un documento que cumple ciertos criterios de consulta
	db.miColeccion.updateOne(
	   { nombre: "Ejemplo" },
	   { $max: { edad: 40 } }
	);

	```



|| $in

	Selecciona documentos donde el valor de un campo determinado coincida con al menos uno de los valores especificados en una lista. 

	Realizar consultas que pueda coincidir con varios valores diferentes en un campo específico.

	```js

	db.collection.find({ campo: { $in: [valor1, valor2, valor3, ...] } })

	```

	
	```js

	// Encuentra documentos donde el campo "estado" coincida con cualquiera de los valores especificados
	db.usuarios.find({ estado: { $in: ["activo", "pendiente"] } })

	```	

	Buscará todos los documentos en la colección usuarios donde el campo "estado" coincida con cualquiera de los valores "activo" o "pendiente". 

	El operador $in permite realizar consultas eficientes cuando necesitas buscar documentos que coincidan con varios valores posibles en un campo determinado.



|| $addToSet

	Agregar un elemento a un conjunto en un campo de tipo array en un documento, si el elemento no existe previamente en el conjunto. 

	Si el elemento ya está presente en el conjunto, la operación no realiza ningún cambio en el campo.	

	```js

	db.collection.updateOne(
	   <filtro>,
	   { $addToSet: { campoArray: valor } }
	)

	```

	campoArray

		Es el nombre del campo de tipo array al que se agregará el valor.
	
	valor

		Es el valor que se va a agregar al campo array si no existe previamente.



|| $push
	
	Operador de actualización agregar un valor a un campo de tipo array en un documento. 

	Este operador agrega el valor al final del array existente en el campo especificado.

	```js

	db.collection.updateOne(
	   <filtro>,
	   { $push: { campoArray: valor } }
	)

	```


	```js

	// Agregar un elemento al campo "compras" en un documento que cumple ciertos criterios de consulta
	db.usuarios.updateOne(
	   { nombre: "Ejemplo" },
	   { $push: { compras: "nuevoProducto" } }
	)

	```
	Agrega el valor "nuevoProducto" al final del campo "compras".



|| $pop

	Eliminar el primer o el último elemento de un campo de tipo array en un documento. 

	Ya sea el primero o el último, según la dirección especificada (-1, 1).	


	Eliminar primer elemento (-1):	

		```js

		db.collection.updateOne(
		   <filtro>,
		   { $pop: { campoArray: -1 } }
		)

		```


	Eliminar último elemento (1): 

		```js

		db.collection.updateOne(
		   <filtro>,
		   { $pop: { campoArray: 1 } }
		)

		```



|| $pull

	Eliminar todos los elementos de un campo de tipo array que coinciden con un valor o una condición específica. 

	Esto permite eliminar uno o más elementos de un array en un documento que coincidan con ciertos criterios de consulta.

	```js

	db.collection.updateOne(
	   <filtro>,
	   { $pull: { campoArray: { criterio: valor } } }
	)

	```



|| updateMany()

	Actualizar varios documentos que coinciden con un conjunto específico de criterios de consulta en una colección. 

	A diferencia de updateOne(), que actualiza solo un documento, updateMany() actualiza múltiples documentos que cumplen con los criterios de consulta especificados.

	```js

	db.collection.updateMany(
	   <filtro>,
	   <actualización>,
	   {
	     upsert: <booleano>,
	     writeConcern: <documento>
	   }
	)

	```


	```js

	// Incrementar el campo "cantidad" en 5 para todos los documentos que cumplan ciertos criterios de consulta
	db.miColeccion.updateMany(
	   { tipo: "producto" },
	   { $inc: { cantidad: 5 } }
	);

	```

	Aumenta el valor del campo "cantidad" en 5 para todos los documentos en la colección miColeccion que tienen el campo "tipo" con el valor "producto".


	
|| upserts

	Operación de actualización que crea un nuevo documento si no se encuentra ningún documento que coincida con los criterios de consulta especificados. 

	La palabra "upsert" es una combinación de las palabras "update" e "insert" y se utiliza para indicar que si no se encuentra ningún documento que coincida con los criterios de consulta, se realizará una operación de inserción en su lugar.

	El comportamiento de un upsert se controla mediante el uso del parámetro 'upsert' en métodos como updateOne() o updateMany(). 

	Cuando upsert está establecido en 'true', MongoDB insertará un nuevo documento si no se encuentra ningún documento que coincida con los criterios de consulta especificados.

	```js

	// Actualizar un documento si se encuentra o insertar un nuevo documento si no se encuentra ningún documento que coincida con los criterios de consulta
	db.miColeccion.updateOne(
	   { identificador: 123 },
	   { $set: { nombre: "Ejemplo" } },
	   { upsert: true }
	);

	```

	Si hay un documento en la colección miColeccion que tiene el campo "identificador" con el valor 123, se actualizará el campo "nombre" con el valor "Ejemplo". 

	Si no se encuentra ningún documento con el campo "identificador" igual a 123, se creará un nuevo documento con el campo "identificador" establecido en 123 y el campo "nombre" establecido en "Ejemplo".



|| replaceOne()
	
	Reemplazar un solo documento que cumple con un conjunto específico de criterios de consulta en una colección con un nuevo documento. 

	A diferencia de updateOne(), que solo actualiza campos específicos en un documento, replaceOne() reemplaza completamente el documento existente con uno nuevo.

	```js

	db.collection.replaceOne(
	   <filtro>,
	   <nuevoDocumento>,
	   {
	     upsert: <booleano>,
	     writeConcern: <documento>
	   }
	)

	```


	```js

	// Reemplazar un documento que cumple ciertos criterios de consulta con un nuevo documento
	db.miColeccion.replaceOne(
	   { nombre: "Ejemplo" },
	   { nombre: "NuevoEjemplo", edad: 30 }
	);

	```

	Reemplaza el primer documento en la colección miColeccion que tiene el campo "nombre" con el valor "Ejemplo" con un nuevo documento que tiene el campo "nombre" establecido en "NuevoEjemplo" y el campo "edad" establecido en 30.

	

|| delateOne()
	
	Eliminar un solo documento que coincide con un conjunto específico de criterios de consulta en una colección. 

	Esto permite eliminar un único documento que cumple con ciertos criterios de filtro.

	```js

	db.collection.deleteOne(
	   <filtro>,
	   {
	     writeConcern: <documento>
	   }
	)

	```


	```js

	// Eliminar un documento que cumple ciertos criterios de consulta
	db.miColeccion.deleteOne(
	   { nombre: "Ejemplo" }
	);

	```

	Eliminará el primer documento en la colección miColeccion que tiene el campo "nombre" con el valor "Ejemplo".



|| delateMany()
	
	Eliminar varios documentos que coinciden con un conjunto específico de criterios de consulta en una colección. 

	A diferencia de deleteOne(), que elimina solo un documento, deleteMany() elimina múltiples documentos que cumplen con los criterios de consulta especificados.

	```js

	db.collection.deleteMany(
	   <filtro>,
	   {
	     writeConcern: <documento>
	   }
	)

	```


	```js

	// Eliminar todos los documentos que cumplan ciertos criterios de consulta
	db.miColeccion.deleteMany(
	   { tipo: "obsoleto" }
	);

	```

	Eliminará todos los documentos en la colección miColeccion que tengan el campo "tipo" con el valor "obsoleto".



|| Operadores de consultas
	
	Proporcionan funcionalidades para filtrar datos, realizar comparaciones, buscar valores específicos.
	
	Operadores de comparación: 

		$eq, $gt, $lt, $gte, $lte, $ne.


    Operadores lógicos: 

    	$and, $or, $not, $nor.


    Operadores de elementos:

    	$exists, $type.


    Operadores de evaluación:

    	$regex, $expr.


    Operadores de array: 

    	$in, $nin, $all, $size, $elemMatch.


    Uso de los operadores: 

    	Se utilizan en combinación con comandos de consulta como find() para recuperar documentos que coincidan con ciertos criterios de consulta. 

    	Por ejemplo, puedes utilizar el operador '$gt' para encontrar documentos con valores que sean mayores que un valor específico en un campo determinado.

    	```js

    	// Encontrar documentos donde el campo "edad" sea mayor que 30
		db.usuarios.find({ edad: { $gt: 30 } });

    	```

    	Devuelve todos los documentos en la colección usuarios donde el campo "edad" es mayor que 30.



|| Operadores de comparación 
	
	Permiten encontrar documentos que cumplan con ciertas condiciones de comparación en campos específicos.

	
	$eq: 

		Coincide con valores iguales a un valor específico.
	
	$gt: 

		Coincide con valores mayores que un valor específico.
	
	$lt: 

		Coincide con valores menores que un valor específico.
	
	$gte: 

		Coincide con valores mayores o iguales que un valor específico.

	$lte: 

		Coincide con valores menores o iguales que un valor específico.

	$ne: 

		Coincide con valores que no son iguales a un valor específico.



|| Operadores de elementos $exists, $type

	
	$exists:	

		Verifica si un campo específico existe en un documento. 

		Se utiliza para encontrar documentos que contengan un campo determinado, independientemente de su valor

		```js

		{ campo: { $exists: <booleano> } }

		```


		```js

		db.usuarios.find({ apellido: { $exists: true } });

		```

		Devolverá todos los documentos en la colección usuarios que contienen el campo "apellido".


		```js

		db.usuarios.find({ direccion: { $exists: false } });

		```

		Devolverá todos los documentos en la colección usuarios que no contienen el campo "direccion".


	$type:

		Realiza consultas basadas en el tipo de un campo en un documento. 

		Busca documentos que contengan un campo con un tipo de datos específico.

		```js

		{ campo: { $type: <tipo> } }

		```

		Especificación: 	

			1 para números de punto flotante.

		    2 para cadenas.

		    3 para objetos.

		    4 para arrays.

		    8 para booleanos.

		    9 para fechas.

		    16 para datos de 32 bits.


		```js

		db.usuarios.find({ edad: { $type: "int" } });

		```



|| Operadores lógicos: $and, $or, $not


	$and:

		Combina múltiples expresiones de consulta y recuperar documentos que cumplan con todas las condiciones especificadas.

		Permite realizar consultas más complejas y detalladas al aplicar múltiples condiciones en una sola consulta.
	
		```js

		{ $and: [ { expresion1 }, { expresion2 }, ... ] }

		```

		Son expresiones de consulta individuales que representan las condiciones que deben cumplirse.


		Encontrar documentos que cumplan dos condiciones específicas, como encontrar documentos con un campo "edad" mayor que 30 y un campo "nombre" igual a "Juan",

		```js

		db.usuarios.find({
		  $and: [
		    { edad: { $gt: 30 } },
		    { nombre: "Juan" }
		  ]
		});

		```

		Devolverá todos los documentos en la colección usuarios que cumplen ambas condiciones: 

			tener un campo "edad" mayor que 30 y un campo "nombre" igual a "Juan".


	$or: 

		Combinar múltiples expresiones de consulta y recuperar documentos que cumplan al menos una de las condiciones especificadas.

		```js

		db.usuarios.find({
		  $or: [
		    { edad: { $gt: 30 } },
		    { nombre: "Juan" }
		  ]
		});

		```

		Devolverá todos los documentos en la colección usuarios que cumplan al menos una de las condiciones especificadas: 

			tener un campo "edad" mayor que 30 o un campo "nombre" igual a "Juan".


	$not:

		Realizar consultas de negación, lo que significa que selecciona documentos que no cumplen con una expresión de consulta específica. 
		
		Puedes usar este operador para negar el resultado de una expresión de consulta.	

		```js

		{ campo: { $not: { expresion } } }

		```

		Se puede usar con una variedad de otros operadores de consulta, como operadores de comparación, operadores lógicos y otros operadores, para realizar consultas de negación más complejas.


		Ej. Encontrar documentos donde el campo "edad" no sea mayor que 30:

		```js

		db.usuarios.find({ edad: { $not: { $gt: 30 } } });

		```

		Devolverá todos los documentos en la colección usuarios donde el campo "edad" no sea mayor que 30.



|| Operadores de Vectores: $all, $size, $elementMatch

	
	$all:

		Consultas en campos que contienen arrays y buscar documentos que contienen todos los elementos especificados en una lista de valores.

		Esto significa que los documentos deben contener todos los valores especificados en el campo de tipo array para que se devuelvan en el resultado de la consulta.

		```js

		{ campo: { $all: [valor1, valor2, ...] } }

		```

		[valor1, valor2, ...] es una lista de valores que se buscan en el array.

		Encuentra todos los documentos que contengan todos los elementos especificados.


		Ej. Encontrar documentos que contengan tanto "manzana" como "naranja" en un campo de tipo array llamado "frutas".

		```js

		db.productos.find({ frutas: { $all: ["manzana", "naranja"] } });

		```

		Devolverá todos los documentos con las características especificadas. 



	$size:

		Consultas en campos que contienen arrays y buscar documentos cuyo campo de tipo array tenga un tamaño específico. 

		Recupera documentos cuyo campo de tipo array contenga un número específico de elementos.

		```js

		{ campo: { $size: <tamaño> } }

		```

		Ej. Encontrar documentos cuyo campo de tipo array "valores" tenga un tamaño de 3:

		```js

		db.coleccion.find({ valores: { $size: 3 } });		

		```


	$elementMatch:

		Consultas en campos que contienen arrays de documentos incrustados y para seleccionar documentos que contienen al menos un elemento que cumple con los criterios de consulta especificados.		

		Garantiza que al menos un elemento del array cumpla con todos los criterios de consulta especificados. 

		Es útil cuando el campo de array contiene varios documentos y deseas garantizar que al menos un documento cumpla con ciertas condiciones.

		```js

		{ campo: { $elemMatch: { <expresion_de_consulta> } } }

		```


		Ej. Colección de artículos donde cada artículo tiene un campo "comentarios" que contiene un array de documentos con campos como "autor" y "contenido".

		```js

		db.articulos.find({ comentarios: { $elemMatch: { autor: "Usuario1" } } });

		```
		Devolverá todos los artículos que contienen al menos un comentario escrito por el autor "Usuario1".



|| Operadores de Evaluación: $regex

	Realizar consultas de expresiones regulares en campos de tipo string. 

	Permite buscar documentos que contienen valores de cadena que coinciden con un patrón específico definido por una expresión regular.

	```js

	{ campo: { $regex: /patrón/ } }

	```

	campo: 

		Nombre del campo de tipo string en el que se realizará la búsqueda.

    /patrón/

    	Es la expresión regular que se utilizará para realizar la coincidencia.	


    Realizar búsquedas más flexibles en campos de tipo string y encontrar documentos que contienen valores que coinciden con un patrón específico.

    Ej. Encontrar documentos cuyo campo "nombre" comience con la letra "A".

    ```js

    db.usuarios.find({ nombre: { $regex: /^A/ } });

    ```

    Devolverá todos los documentos en la colección usuarios cuyo campo "nombre" comienza con la letra "A".



|| Lista de métodos

	Operaciones de Consulta y Búsqueda de Documentos:

	    find(): 

	    	Busca documentos en una colección que coincidan con ciertos criterios.

	    findOne(): 

	    	Busca un solo documento en una colección que coincida con ciertos criterios.

	    aggregate():

	    	Realiza operaciones de agregación en los datos de una colección.


	Operaciones de Actualización de Documentos:

	    updateOne(): 

	    	Actualiza un solo documento que coincida con los criterios especificados.

	    updateMany(): 

	    	Actualiza varios documentos que coincidan con los criterios especificados.

	    replaceOne(): 

	    	Reemplaza un solo documento que coincida con los criterios especificados.


	Operaciones de Inserción de Documentos:

	    insertOne(): 

	    	Inserta un solo documento en una colección.

	    insertMany(): 

	    	Inserta varios documentos en una colección.


	Operaciones de Eliminación de Documentos:

	    deleteOne(): 

	    	Elimina un solo documento que coincida con los criterios especificados.

	    deleteMany(): 

	    	Elimina varios documentos que coincidan con los criterios especificados.


	Operaciones de Conteo y Estadísticas:

	    countDocuments(): 

	    	Cuenta los documentos que coinciden con los criterios especificados.

	    estimatedDocumentCount():

	    	Estima el número de documentos en una colección.

	    distinct(): 

	    	Encuentra los valores únicos de un campo específico en una colección.


	Operaciones de Índices:

	    createIndex(): 	

	    	Crea un índice en una colección.

	    dropIndex(): 

	    	Elimina un índice de una colección.

	    listIndexes(): 

	    	Lista todos los índices en una colección.


	Otras Operaciones:

	    findOneAndUpdate(): 

	    	Busca y actualiza un solo documento en una colección.

	    findOneAndReplace(): 

	    	Busca y reemplaza un solo documento en una colección.

	    findOneAndDelete(): 

	    	Busca y elimina un solo documento en una colección.

	    watch(): 

	    	Observa cambios en una colección y devuelve actualizaciones en tiempo real.




