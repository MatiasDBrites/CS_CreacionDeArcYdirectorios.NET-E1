# CS_CreacionDeArcYdirectorios.NET-E1
Ejercicio: Crear archivos y directorios

1. En el archivo `Program.cs`, quite el bucle `foreach` que recorre en iteración y escribe cada nombre de archivo devuelto por la función `FindFiles` en la salida de la *consola*. Esto hará que la variable `salesFiles` se quede sin usar. Se dejará aquí por el momento porque se volverá a utilizar en una lección futura.
2.En el archivo `Program.cs`
, cree una variable denominada `salesTotalDir`
, que contiene la ruta de acceso del directorio *salesTotalDir*
:

```csharp
var currentDirectory = Directory.GetCurrentDirectory();
var storesDirectory = Path.Combine(currentDirectory, "stores");

var salesTotalDir = Path.Combine(currentDirectory, "salesTotalDir");

var salesFiles = FindFiles(storesDirectory);
```

En el archivo `Program.cs`
, agregue código para crear el directorio:

```csharp
var currentDirectory = Directory.GetCurrentDirectory();
var storesDirectory = Path.Combine(currentDirectory, "stores");

var salesTotalDir = Path.Combine(currentDirectory, "salesTotalDir");
Directory.CreateDirectory(salesTotalDir);   // Add this line of code

var salesFiles = FindFiles(storesDirectory);
```

En el archivo `Program.cs`
, agregue el código para crear un archivo vacío denominado *totals.txt*
 en el directorio *salesTotalDir*
 recién creado. Por el momento, use una cadena vacía para el contenido del archivo:

```csharp
var currentDirectory = Directory.GetCurrentDirectory();
var storesDirectory = Path.Combine(currentDirectory, "stores");

var salesTotalDir = Path.Combine(currentDirectory, "salesTotalDir");
Directory.CreateDirectory(salesTotalDir);

var salesFiles = FindFiles(storesDirectory);

File.WriteAllText(Path.Combine(salesTotalDir, "totals.txt"), String.Empty);
```

Guardar, Ejecute el código siguiente desde el símbolo del sistema de terminal para ejecutar el programa:

```csharp
dotnet run
```

[![Crear-Arcy-Dir.png](https://i.postimg.cc/GhDkdjRV/Crear-Arcy-Dir.png)](https://postimg.cc/XpVZgdpk)
