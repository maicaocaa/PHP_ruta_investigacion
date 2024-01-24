# PHP ruta de investigación F5
RECURSOS
● [https://www.php.net/manual/es/index.php](https://www.php.net/manual/es/index.php)
● [https://www.w3schools.com/php/](https://www.w3schools.com/php/)
● [https://www.w3schools.com/sql/default.asp](https://www.w3schools.com/sql/default.asp)
● [https://dev.mysql.com/doc/](https://dev.mysql.com/doc/)
 
## **PARTE 1:**

  
**¿Qué es PHP y cuál es su función principal en el desarrollo web?**
PHP, que significa "Hypertext Preprocessor”

Sus usos son
-  *Aplicaciones web y sitios web (scripting al lado del servidor)*
-  *Scripting en la línea de comandos*
-  *Aplicaciones de escritorio (GUI)*

Se necesitan tres cosas: PHP, un servidor web y un navegador web
Es un lenguaje de script del lado del servidor que se incrusta en el código HTML y se ejecuta en el servidor web.
Interactúa con bases de datos y servidores web.
Alto nivel. se parece al lenguaje humano y no al lenguaje máquina.
Es interpretado , no necesita ser compilado, no necesita ser pasado a lenguaje maquina
Débilmente tipado, tiene tipo de datos pero es flexible, una variable puede ir cambiando el tipo de datos.
PHP puede procesar HTML, pero HTML no puede procesar PHP

● **¿Cuáles son las características clave de PHP que lo diferencian de otros lenguajes de programación?**
PHP es un lenguaje de script del lado del servidor, lo que significa que el código PHP se ejecuta en el servidor antes de que se envíe la página web.
Esto permite generar contenido dinámico y procesar datos en el servidor antes de enviar la respuesta al cliente.
Se embebe entre etiquetas `<?php` y `?>`,

Este mecanismo permite embeber a PHP en todo tipo de documentos, ya que todo lo que esté fuera de las etiquetas de apertura y cierre de PHP será ignorado por el analizador.

● **¿Cuál es la sintaxis básica de PHP y cuáles son las convenciones de nomenclatura utilizadas?**
Se escribe entre <?php y >
Las variables se declaran y usan con el símbolo $
Las estructuras de control en PHP incluyen **`if`**, **`else`**, **`elseif`**, **`while`**, **`for`**, **`foreach`**

Las funciones se declaran como function ()
Todas las líneas de código acaban con punto y coma 
Se define una constante como

define ("MI_CONSTANTE", "Este es el valor de mi constante");
const MI_CONSTANTE =”valor de mi constante”;

Array indexado
```markdown
$miArrayIndexado = array ("Manzana", "Banana", "Cereza");
$miArrayIndexado= ["Manzana", "Plátano", "Uva"];
```
Array asociativo (se puede leer parecido a un objeto )
```markdown
$miArrayAsociativo = array(
"fruta1" => "Manzana",
"fruta2" => "Banana",
"fruta3" => "Cereza"git if
);

$miArrayAsociativo = [
"fruta1" => "Manzana",
"fruta2" => "Banana",
"fruta3" => "Cereza"
];
```
Objetos no hay, hay clases y generan objetos, PHP puede ser orientado a objetos
En PHP, los objetos son instancias de clases.
```php

class  Persona {
public  $nombre;
public  $edad;
public  function  __construct($nombre, $edad) {
$this->nombre = $nombre;
$this->edad = $edad;
}
public  function  saludar() {
echo  "Hola, mi nombre es $this->nombre y tengo $this->edad años.";
}
}

$juan = new  Persona("Juan", 30);
```
En este ejemplo, **`$juan`** es una instancia de la clase **`Persona, con un valor de nombre=juan edad=30`**

```php
<?php if ($expresion == true): ?> // Esto se mostrará si la expresión es verdadera.
<?php else: ?> // En caso contrario se mostrará esto.
<?php endif; ?>

```
● **¿Cuáles son los tipos de datos admitidos en PHP y cómo se manejan?**
	Enteros Integer
	Flotantes Float o Double
	Cadenas String varchar
	Boleanos Bool
	Arrays
	Objetos Permiten definir estructuras de datos complejas con propiedades y métodos.
	Recursos (`resource`): Representan recursos externos, como conexiones a bases de datos o manipuladores de archivos.
	Nulo (`null`): ausencia de valor
	Undefined

	

**● ¿Cuál es la diferencia entre una variable local y una variable global en PHP?**
**variable global:** Se utiliza la palabra clave **`global`** para referenciar una variable global desde dentro de una función.
**Variable local:** Se crea se ejecuta y se consume dentro de la función o bloque en la que se ha creado
También hay variables globales que son **superglobales** , propias del lenguaje PHP

**● ¿Qué son los arrays en PHP y cómo se utilizan para almacenar y manipular datos?**
SE puede utilizar para trabajar con tablas
Hay array asociativo, indexado y multidimensional
```php
Esto es como se accede a un array Indexado

$sentido[1]="ver";
$sentido[2]="tocar";
$sentido[3]="oir";
$sentido[4]="gustar";
$sentido[5]="oler";
```

```php

Esto es como se accede a un array Asociativo o clave/valor

$moneda["espana"]="Euro";
$moneda["francia"]="Franco";
$moneda["usa"]="Dolar";
```

```php

Esto es un Array  multidimensional (se parece a un objeto de JS)

$pais=array
(

"espana" =>array
(
"nombre"=>"España",
"lengua"=>"Castellano",
"moneda"=>"euro"
),

"francia" =>array
(

"nombre"=>"Francia",
"lengua"=>"Francés",
"moneda"=>"euro"
)
);
```

**● ¿Cómo declarar variables en PHP?**
$variable
También puedes exigir tipo de dato de esta forma $my_int1=(int)1;

**● ¿Cómo declarar funciones en PHP?**
function miFuncion(parametro1, parámetro2,…) {} ;

**● ¿Cómo conectar PHP con HTML y mostrar un “Hola Mundo” en el browser a través del servidor de PHPmyAdmin?**

Dentro de un archivo .php puedes escribir codigo html, pero fuera de los tags de php.
para llamar a una variable de php dentro de html, puedes embeber codigo php dentro de los tags correspondientes

```
<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Hola Mundo</title>
</head>
<body>
<h1><?php echo $mensaje; ?></h1>
</body>
</html>
```

**● ¿Cómo uso la consola con PHP?**
En la ruta donde guardes el proyecto este en la carpeta htdocs, abres una consola y la enrutas a tu proyecto, ejecutar php + el nombre del archivo php, ejemplo php prueba.php

**● ¿Cómo reutilizar funciones desde otros documentos de PHP?**
**`include`** o **`require`** y el archivo .php
Luego ya puedes utilizar las funciones del archivo en donde la llames

**`require_once`** o **`include_once`** en lugar de **`require`** o **`include`** para garantizar que el archivo se incluya solo una vez, incluso si se llama múltiples veces. Esto evita problemas de redefinición de funciones o variables

include_once "formulario.php";
require_once "formulario.php";

Diferencia de include y requiered es la gestión de errores.
include si no encuentra la variable en el archivo importado, la aplicación sigue corriendo
required si no hay la variable en el archivo importado , el error detendrá la ejecución del script.

**● ¿Qué son los modificadores de acceso?**
Son palabras clave en la programación orientada a objetos que definen el nivel de visibilidad o acceso de las propiedades y métodos de una clase. En PHP, hay tres principales modificadores de acceso:
**public, protected y private**
Es una buena práctica declarar las propiedades como **`private`** y proporcionar métodos públicos (**`getters`** y **`setters`**) para acceder y modificar esas propiedades desde fuera de la clase.
son esenciales para garantizar la encapsulación y controlar el acceso a las partes internas de una clase.
Ayudan a mantener un diseño coherente y a prevenir el acceso no autorizado o accidental a ciertos miembros de la clase.

Los **getters** y **setters** son métodos utilizados para acceder y modificar los valores de las propiedades de un objeto

**setter** es el método dentro de la clase que permite asignar el valor del objeto en este caso “nombre”
```php
setNombre($nuevoNombre) {
$this->nombre = $nuevoNombre;
```
**getter** es el metodo dentro del una clase que permite devolver el valor del objeto en este caso “nombre”
```php
function  getNombre() {
return  $this->nombre;
```

**● ¿Qué es public?**
Los elementos (propiedades y métodos) marcados como **`public`** son accesibles desde cualquier lugar, tanto dentro como fuera de la clase.
public $var
public function ()


**● ¿Qué es private?**
Las propiedades y métodos marcados como private son accesibles únicamente desde la propia clase. No son accesibles desde clases heredadas ni desde fuera de la clase.
private $var
private function ()

**● ¿Qué es protected?**
Son accesibles desde la propia clase y también desde clases heredadas (subclases).
protected &var
protected function ()

## **PARTE 2:**
● **¿Cómo creo una base de datos en PHPMyAdmin? Crea una BBDD**
Arranco apache y mysql y abro un navegador [localhost/phpmyadmin](http://localhost/phpmyadmin)
en el menú puedo crear tablas en entorno gráfico o con comandos SQL
Si es por comandos seria inyectar sql
En XAMPP, tanto la extensión MySQLi como la extensión PDO para PHP están habilitadas por defecto. Esto significa que puedes utilizar ambas para conectar y trabajar con bases de datos MySQL desde tu aplicación PHP.
PHP 5 y versiones posteriores pueden trabajar con una base de datos MySQL utilizando:
-  **Extensión MySQLi** (la "i" significa mejorada)
-  **PDO (PHP Data Objects)**
La base de datos se crean con código SQL en php CREATE DATA BASE nombreBd;
Primero se establece la conexión, se envía la acción por sql y se hacen verificaciones
El usuario por defecto de mysql es root y contraseña esta vacia
```php
<?php
$servername = "localhost";
$username = "username";
$password = "password";
// Create connection
$conn = new  mysqli($servername, $username, $password);
// Check connection
if ($conn->connect_error) {
die("Connection failed: "  .  $conn->connect_error);
}

// Create database
$sql = "CREATE  DATABASE myDB";
if ($conn->query($sql) === TRUE) {
echo  "Database created successfully";
} else {
echo  "Error creating database: "  .  $conn->error;
}
$conn->close();
?>

```

Ejemplo real

```php

<?php
$servername = "localhost";
$username = "root";
$password = "";
$database = "Ruta_Investigacion"; // Nombre de la base de datos
// Crear la conexión
$conn = mysqli_connect($servername, $username, $password);
// Verificar la conexión
if (!$conn) {
die("Conexión fallida: "  .  mysqli_connect_error());
}
// Crear la base de datos
$sql = "CREATE  DATABASE  IF  NOT  EXISTS  $database";
if (mysqli_query($conn, $sql)) {
echo  "Base de datos creada exitosamente";
} else {
echo  "Error al crear la base de datos: "  .  mysqli_error($conn);
}
// Seleccionar la base de datos recién creada
mysqli_select_db($conn, $database);
// Cerrar la conexión cuando hayas terminado
mysqli_close($conn);
?>
```
![Untitled](PHP%20ruta%20de%20investigacio%CC%81n%20a20dadeb2a034276ae6c2412aa9bd696/Untitled.png)

**● ¿Cómo consulto información a esa base datos? haz 3 queries dentro de MySQL**
![Untitled](PHP%20ruta%20de%20investigacio%CC%81n%20a20dadeb2a034276ae6c2412aa9bd696/Untitled%201.png)
Puedo consultarlo a través de codigo sql dentro de cada tabla o explorando las tablas
SELECT * FROM tabla
WHERE (condicion))
**Para conectarse a través de código php**
PHP 5 y versiones posteriores pueden trabajar con una base de datos MySQL utilizando:
-  **Extensión MySQLi** (la "i" significa mejorada)
-  **PDO (PHP Data Objects)**
En XAMPP, tanto la extensión MySQLi como la extensión PDO para PHP están habilitadas por defecto. Esto significa que puedes utilizar ambas para conectar y trabajar con bases de datos MySQL desde tu aplicación PHP.
**abrir session ;**
$conn = new mysqli($servername, $username, $password);
**cerrar session según la extensión utilizada;**
$conn->close();
mysqli_close($conn);
$conn = null;

ver [https://www.w3schools.com/php/php_mysql_connect.asp](https://www.w3schools.com/php/php_mysql_connect.asp)

Hacer consulta. Abren una sesion en mysqli y luego hacen la consulta
$sql = "SELECT id, firstname, lastname FROM MyGuests";
y guardan el resultado en
$result = $conn->query($sql);

```
$servername = "localhost";
$username = "username";
$password = "password";
$dbname = "myDB";

// Create connection
$conn = new mysqli($servername, $username, $password, $dbname);
// Check connection
if ($conn->connect_error) {
die("Connection failed: " . $conn->connect_error);
}

$sql = "SELECT id, firstname, lastname FROM MyGuests";
$result = $conn->query($sql);
if ($result->num_rows > 0) {
// output data of each row
while($row = $result->fetch_assoc()) {
echo "id: " . $row["id"]. " - Name: " . $row["firstname"]. " " . $row["lastname"]. "<br>";
}

} else {
echo "0 results";
}

$conn->close();
?>

```

**● ¿Qué significa CRUD?**
create read update y delete
cuatro operaciones básicas utilizadas en la manipulación de datos en sistemas de gestión de bases de datos relacionales.
**create , insert into , select , update, drop delete**
**● ¿Cómo conecto código PHP a mi base de datos? Haz el servicio de conexión**
Generalmente utilizar la extensión **`mysqli`** o **`PDO`** en PHP
```php
$servername = "localhost";
$username = "root";
$password = "";
$dbname = "myNewDB";
// Create connection
$conn = new  mysqli($servername, $username, $password, $dbname);

// verifico conexion
if ($conexion->connect_error) {
die("Conexión fallida: "  .  $conexion->connect_error);
}
// muestra mensaje para verificar
echo  "Conexión exitosa";
// Cerrar la conexión
$conexion->close();
```
PDO PHP Data Objects y permite elegir el tipo de SGDB que gestiona la base de datos, en este caso es Mysql y tiene usuario root y contraseña vacia
```php
try {
// Crear conexión
$conexion = new  PDO("mysql:host=$servername;dbname=$database", $username, $password);
// Configurar el manejo de errores
$conexion->setAttribute(PDO::ATTR_ERRMODE, PDO::ERRMODE_EXCEPTION);
echo  "Conexión exitosa";
} catch (PDOException  $e) {
die("Conexión fallida: "  .  $e->getMessage());
}

// Cerrar la conexión al finalizar el script (opcional)
$conexion = null;
?>
```


## **PARTE 3:**

**● ¿Cómo se manejan las excepciones en PHP y cuál es la estructura básica de un bloquetry-catch?**

```php

try {
// Código que podría lanzar una excepción
} catch (Exception  $e) {
// Código para manejar la excepción
}
```

-  **Try (Intentar):** En este bloque, colocas el código que podría lanzar una excepción. PHP monitorea cualquier excepción que ocurra dentro de este bloque.
-  **Catch (Capturar):** Si ocurre una excepción dentro del bloque **`try`**, el control se transfiere al bloque **`catch`**
**● ¿Qué es MySQL y cómo se integra con PHP para la manipulación de bases de datos?**

Mysql es un sistema gestor de bases de datos que maneja bases de datos y consulta sobre ellas con lenguaje de consulta y manipulación SQL, A través de este lenguaje, php puede acceder y manipular la base de datos en aplicaciones web.
La integración se logra mediante extensiones PHP específicas para interactuar con bases de datos MySQL, siendo las extensiones más comunes **`mysqli`** (MySQL Improved) y **`PDO`** (PHP Data Objects).
```php

$sql_insert = "INSERT INTO usuarios (nombre, edad) VALUES ('Juan', 25)";
```

```php
if ($conexion->query($sql_insert) === TRUE) {
echo  "Registro creado exitosamente";
} else {
echo  "Error al crear el registro: "  .  $conexion->error;
}
```

**● ¿Cuáles son las técnicas comunes utilizadas para el manejo de formularios en PHP y cómo sevalida la entrada de datos?**
A través de formulario HTML, los datos se envían al servidor PHP. Puedes acceder a estos datos a través de las variables **superglobales `$_GET`** o **`$_POST`** según el método de envío del formulario (GET o POST).
Para validar los datos introducidos

a. Validación del Lado del Cliente (JavaScript):
	Se utiliza JavaScript para realizar validaciones del lado del cliente antes de que los datos se envíen al servidor. Sin embargo, estas validaciones no son suficientes por sí solas y siempre se debe realizar una validación adicional en el lado del servidor para garantizar la seguridad.
	Generar restricciones en el formulario HTML con atributo pattern
b. Validación del Lado del Servidor (PHP):
	Sanear datos y procesarlos por si es necesario guardarlo en una Base de datos. Ejemplo fecha en PHP es un string y si queremos guardarlo en la BD como date, deberemos tratar esos datos.
