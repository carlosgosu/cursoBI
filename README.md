# cursoBI

## Preparación de entorno

### Instalacion de SQLite
1. Descargar Sqlite-tools-windows: https://www.sqlite.org/download.html
2. Descomprimir contenido en un directorio y abrir CMD (win+R escribir cmd) navegar al directorio
4. Probar a ejecutar sqlite3.exe y si no hay problemas debería salir el shell de sqlite. Para salir teclear *.quit*
   - La ayuda se puede acceder con *.help*
6. Descargar desde https://github.com/pawelsalawa/sqlitestudio/releases. Se usará el portable

### Creación de BD
1. Ejecutar sqlite3.exe
2. Ejecutar *.open <nombre>.db*
   - Esto crea un fichero <nombre.db> en el directorio donde está sqlite3.exe
   - se puede especificar el directorio donde se va a crear el fichero *.open C:/BASURA/mibasedatos.bd*
3. Para crear las tablas se pueden crear desde el shell o desde un script SQL. Para ejcutar el script de creación:
   - Al entrar en SQLite *sqlite3.exe C:/BASURA/mibasedatos.db < script-ddl.sql*
   - Desde dentro del shell ejecutando *.read script-ddl.sql* (o alternativamente *.read |script-ddl.sql* que ejecuta las lineas del fichero en el shell)
   - Comprobar que se han creado las tablas con *.tables* (o alternativamente con *.schema* que muestra la estructura de todas las tablas)

> Los resultados de las consultas en SQLite pueden sacarse en distintos formatos, algunos de los cuales son:
> - list
> - column
> - json
> - csv
> - table
> - box
> - insert
> 
> Para cambiar de modo es necesario ejecutar *.mode <formato>*. Para conocer el formato utilizado actualmente ejecutar *.mode*. Los más recomendables son table o box para mirar los resultados en el shell. En estos formatos se puede especificar el ancho de visualizacion de la columna con el parametro *--wrap N*. Por ejemplo con *.mode box --wrap 50* el texto se mosrtrará en columnas de 50 caracteres de ancho.


